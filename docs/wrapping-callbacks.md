# 包装回调

> 原文：<https://simpleprogrammer.com/wrapping-callbacks/>

我最近遇到了一个问题，当执行一个异步操作时，我试图显示一个进度对话框，当操作完成时，我试图关闭这个进度对话框。

我想构建一种对我的应用程序通用的方法来实现这一点，这样它就可以与任何异步操作一起工作，以减少代码中处处重复编写进度对话框逻辑。



![11-290x300](img/7e6ea4a98b89a2ab170f0c8e4e25d9a0.png "11-290x300")



## 看问题

这是问题的一些基本伪代码。

现在，这段代码的问题是，它必须在我想进行异步调用和显示进度对话框的任何地方重复。

如果我想在应用程序中每次进行异步调用时都这样做，我必须在应用程序的许多地方放置这种代码。

您还可以在这里看到责任的混合。我们正在处理与 UI 相关的进度对话框显示，该对话框分为初始调用和回调两部分。这样做似乎有点卑鄙。

## 打破它

那么如何才能解决这个问题呢？

去想办法解决这个问题吧。

…

我发现解决这类问题的最好方法之一就是逆向工作。

让我们假设我们能想到的任何语法都是可能的，然后只在它被证明是不可能的时候才改变理想的语法。

我这么说是什么意思？

很简单，让我们想出我们希望这个代码看起来是什么样子，然后我们再考虑实现它。

如果能够执行异步方法并使用一行程序显示进度对话框就好了，如下所示:

如果我们可以在任何想要进行异步调用的地方这样做，并且自动显示和关闭进度对话框，生活将会非常美好。

## 解决问题

为了解决这个问题，我们可以做一些非常类似于[装饰模式](http://en.wikipedia.org/wiki/Decorator_pattern)的事情。

我们基本上可以用一个新的回调来包装我们的回调方法，这个新的回调增加了关闭进度对话框的功能。

因此，我们将在我们的 ***ExecuteAsync*** 方法中执行以下步骤:

1.  显示进度对话框
2.  用一个关闭我们的对话框然后执行回调的函数来包装我们的回调。
3.  执行我们的异步操作，传递新包装的回调作为参数。



![gift-wrap-nature-lovers-easy-style-fabric-wrapping-1211-l](img/9c6682cd8ea6c502749f87cffa3f256c.png "gift-wrap-nature-lovers-easy-style-fabric-wrapping-1211-l")



代码如下所示:

这段代码实际上看起来比实际更复杂。

你需要理解行动是如何运作的。如果你不知道，看看我写的这篇文章[解释动作和功能](https://simpleprogrammer.com/2010/09/24/explaining-what-action-and-func-are/)。

## 了解解决方案

想要理解*类型的*动作*和*类型的*结果可能有点困难。*

让我翻译一下，让它简单一点。

***ExecuteAsync*** 的第一个参数是一个以另一个方法作为参数的方法(回调，)，这个方法以一个结果对象作为参数。

继续读下去，直到你明白为止。

因此，这里的想法是，我们把将要进行回调的方法作为第一个参数传递给你的 ***ExecuteAsync*** 方法。

然后我们将实际的回调作为第二个参数传递给 ***ExecuteAsync* 。**

我们的想法是将方法和它所需要的回调分开，这样我们就可以在需要的地方插入代码来处理对话框。

现在我们只需调用 ***ExecuteAsync*** 并传递给它我们的方法，它的回调和进度对话框代码将自动为我们处理。

## 基于这个想法

我们可以用几种方法来扩展这个概念。

我们可以做的一件事是将错误处理逻辑应用于回调包装方法。在将结果传递给回调之前，我们可以用某种方式对其进行预处理。这将允许我们在执行回调之前显示一条错误消息，甚至重试多次。

我们可以做的另一件事是改变 ***ExecuteAsync*** 方法的签名，以便它接受 T 类型而不是*结果；这将允许我们处理任何类型的返回类型和方法，并且 ExecuteAsync 方法将适用于任何异步方法调用。*