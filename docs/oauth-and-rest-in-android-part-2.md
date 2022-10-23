# Android 中的 OAuth 和 REST:第 2 部分

> 原文：<https://simpleprogrammer.com/oauth-and-rest-in-android-part-2/>

在我的[上一篇文章](https://simpleprogrammer.com/2011/05/25/oauth-and-rest-in-android-part-1/)中，我们大致介绍了 OAuth，并且我们看了如何使用一个叫做陈峰的 Java 库来认证一个提供 OAuth 2 实现的服务。

既然我们能够用 OAuth 认证服务，我们需要能够实际使用该服务来做一些有用的事情。

许多流行的 web 服务 API，如脸书和 Twitter，都提供了基于 REST 的实现。

在这篇文章中，我将向你展示如何轻松地从 Android 连接到这些 web 服务之一，并解析你得到的任何响应。



![AndroidREst](img/cb9e5cb709b81f79477adf9378882ecf.png "AndroidREst")



## 我应该使用 REST 库吗？

在进入细节之前，这是一个我们应该解决的有效问题。

我对这个问题的回答基本是“不”

我首先尝试了使用 REST 库的方法，以便更容易地与基于 REST 的 web 服务通信，但是很快发现库的开销超过了它提供的好处。

如果您有调用基于 XML 和 SOAP 的 web 服务的背景，您可能会对这个答案感到惊讶。对于基于 SOAP 的 web 服务，使用一个库来生成一个代理来调用 web 服务，让您不必担心解析 XML 和 SOAP 头，这是一个巨大的好处。

有了休息就完全不同了。转移到基于 REST 的 web 服务的全部目的是简化调用 web 服务的过程。

大多数基于 REST 的 web 服务接口使用起来非常简单。这个想法是，URL 本身包含尽可能多的数据，附加数据包含在 POST 主体中。

通过增加学习 REST 库和实现使其无缝工作所需的适当接口的复杂性，我们可以很容易地增加更多的复杂性和开销，而不仅仅是自己创建一个 HTTP 请求并解析响应。

对于这种方法，我将向您展示如何做到这一点。

## 调用 REST 服务

为了在 Android 中调用 REST 服务，我们必须首先发现并理解提供给我们的 REST API，然后使用我们通过身份验证获得的 OAuth 令牌进行适当的调用。最后，我们将解析调用的结果并返回我们的响应。

**发现 API**

因为 REST 不是真正的标准，而是一种理想，所以 REST APIs 的实现没有一个标准的方法。

您必须看一看您想要调用的 REST API 的文档，以准确地确定调用应该是什么样子。

不过一般来说，REST API 会涉及到发出某种 HTTP GET、POST、PUT 或 DELETE 请求，并通过 URL 或在请求体中传递数据。

这里有一个 Dailymile.com API 的例子，我最近集成了我的应用程序来使用。

你可以在这里看到完整的 [API 文档。](http://www.dailymile.com/api/documentation)

对于这个 API，我将向您展示我如何使用帖子创建锻炼条目。

**拨打剩余电话**

为了在 Android 中进行 REST 调用，我们将使用一个 *HttpClient* 对象和适当的 http 请求类。

在这个例子中，我们将使用 JSONObject 类来创建一些 JSON 格式的数据，我们可以通过将这些数据嵌入 post 来传递给 REST 调用。

我查看了用于将锻炼记录发布到 Dailymile 的 API，请求的格式应该如下所示:

[https://api.dailymile.com/entries.json?oauth_token=](https://api.dailymile.com/entries.json?oauth_token "https://api.dailymile.com/entries.json?oauth_token=")T2【令牌】T3】

该 API 还指出，它希望 post 主体包含一些 JSON，并给我们一个需要包含在该 JSON 对象中的必需和可选条目的列表。

让我们看一下我是如何打这个电话的，然后我们将对它进行细分。

您可以看到，我首先创建了一个 *HttpClient* 对象和一个 *HttpPost* 对象。 *HttpPost* 将其 URL 设置为 API 调用的 URL，我添加了一个查询字符串参数，以提供在我的[上一篇文章](https://simpleprogrammer.com/2011/05/25/oauth-and-rest-in-android-part-1/)中进行身份验证时获得的 OAuth 令牌。

我将内容类型设置为 JSON，这样我们就可以从 API 调用中获得一个 JSON 对象，这样它就知道我们正在传递 JSON 数据。

然后，我按照 API 指定的格式构造一个 JSON 对象。构造 JSON 对象的方法基本上是创建一组由您调用的 API 指定的键和值。在这个实例中，我有一个“message”键，我将消息数据放入其中。

唯一棘手的部分是 JSON 对象可以嵌套。因此，如果您查看上面示例中的键“workout ”,我将创建一个全新的 JSON 对象作为该键的值，该键有自己的子键，可以包含更多的 JSON 对象。

这样做比试图自己构造字符串要简单得多。我们最终构建的字符串看起来会像这样:

Finally, I put the JSON data into a *StringEntity* class and set it as the entity on the HTTP Post. Then we can call execute on the *HttpClient* to execute the HTTP POST.

**处理响应**

Now that we have actually made the call to the REST service method we can handle the response by creating another JSONObject from the HttpResponse that is returned.Let’s look at that code and then we can go over what is happening.

在这种情况下，我们所做的就是从对 *HttpClient* 对象的执行调用中获取响应，然后使用 *EntityUtils.toString* 将响应的实体转换为字符串表示。最后，我们从这个字符串中构造了一个新的 *JSONObject* 。

然后，我们可以通过使用 JSON 对象上的方法轻松地从 JSON 对象中提取任何数据，这些方法允许我们从 JSON 对象中获取类型化值。对于这个例子，我知道我得到了一个 JSON，它有一个键“id ”,是我用我的帖子创建的锻炼的 id。

## 真的就这么简单

我在这里展示的例子是调用基于 REST 的 API 的更复杂的例子之一，因为我们必须提交和解析 JSON 数据。

在许多 API 调用中，您可以只使用一个 HTTP GET 或 POST 而不使用任何数据来完成您在 API 中需要做的事情。

一些基于 REST 的 API 将允许或要求数据以不同的格式传递，但大多数使用 JSON 符号，我发现这是最容易使用的。

希望通过这一系列的文章，你现在可以验证一个基于 OAuth 2 的服务，并调用 API 来获取和操作 Android 中的数据。

如果你有任何问题，请随时给我留言或在下面的评论中发表。