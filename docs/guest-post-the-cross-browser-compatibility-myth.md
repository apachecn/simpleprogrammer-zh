# 客座博文:跨浏览器兼容性的神话

> 原文:[https://simple programmer . com/guest-post-the-cross-browser-compatibility-myth/](https://simpleprogrammer.com/guest-post-the-cross-browser-compatibility-myth/)

*This post is a special guest post from my wife, Heather Sonmez, who is an expert on the subject of blackbox automated tests and designing frameworks for them.  She has designed successful automation frameworks for several companies.  She deals with software automation and framework design issues on a daily basis, so I thought she might be able to offer some good insight on the topic.*

John 让我根据我编写自动化测试的经验写一篇文章。在过去的三年半时间里，我一直是一名 QA 自动化工程师。在此期间，我有机会使用 Ruby/Watir、C#/Watin 和 Java/Selenium RC。在思考一个话题时，我决定没有时间像现在这样谈论我目前面临的问题，我想分享一些我今天发现自己目前所处的困境的见解:

## 声称支持多种浏览器的自动化工具在撒谎

目前，我正在让 400 个在 Firefox 上运行的自动化测试在 Internet Explorer 和 Chrome 上运行。虽然测试使用的是 Selenium RC，一个声称可以在所有三种浏览器平台上工作的工具，但实际上，许多测试都失败了，而且不是因为好的原因(错误)。

以下是这些过于雄心勃勃的工具没有告诉你的内容:

*   浏览器 A 中的 Xpath 在浏览器 B 中并不总是受支持
*   浏览器 A 中的 Dom 可能与浏览器 B 中的 Dom 不同
*   浏览器 B 可能有干扰测试的内置安全设置
*   自动化工具本身的错误可能会导致特定浏览器出现问题

**The XPath Issue**

谈到 XPath，我完全期望任何给定的表达式要么有效，要么无效。但是，在 Internet Explorer 中运行一次以上的测试之后，我突然发现自己的测试声称某些元素并不存在。当 Firefox 接受并使用提供的表达式成功返回我的元素时，IE 声称表达式本身是无效的。在这个特殊的例子中，我发现了 Selenium 剥离 xpath 语句结尾的问题，从而使它无效。

但最终，是浏览器还是工具并不重要，因为相同的表达在两种浏览器中不会不一样。

## ******Dom 问题******

****我马上遇到的下一个问题是浏览器之间的 Dom 差异问题。在这个例子中，我有一个元素在 Firefox 中出现了一次，但在 IE 中出现了两次。我的测试需要元素的一个实例，但失败了。虽然我不能告诉你为什么存在这种差异(目前正在由一些客户端工程师进行调查)，但我有相当程度的信心说这不会是我最后一次遇到这个问题。****

****在寻求支持许多不同的浏览器的过程中，人们必然会遇到有条件的浏览器逻辑，特别是如果一个公司正在努力支持多个浏览器版本(例如 6、7、8、9)。如果开发人员不得不偶尔编写特定于浏览器的条件语句，那么我们必须做同样的事情来测试特定的浏览器是有意义的。****

## ********安全问题********

****如果看起来我在挑 IE 的毛病，那只是因为我不能在 Chrome 上运行我们的测试。Chrome 有特殊的安全设置，如果您的测试中途更改了域，就会导致 Selenium 异常。这可以通过向 Chrome 传递一个参数来轻松解决，当测试运行时，Chrome 将禁用该安全特性，诀窍是计算出何时/何地/如何传递该参数。****

## ********工具问题中的 Bug********

****最后，我在多浏览器测试中遇到的最后一个障碍:工具本身。任何工具，不管它有多棒，都会有缺陷。Selenium RC 有一个问题，它的 select 方法(负责在下拉菜单中选择一个值)不能触发附属的事件处理程序——在 Internet Explorer 中。要解决这个问题，可以使用 Selenium 的 runscript()手动调用事件处理程序，但是这样做会失去一定程度的测试信心(如果您在自动化中手动强制事件，您如何知道事件是否真的是为了响应特定的用户操作而触发的呢？)****

****另一个问题存在于多个浏览器窗口周围；如果您的测试需要打开多个窗口，Selenium 无法选择您打开的第二个窗口——这是另一个尚未解决的 IE 问题。****

## ********总结********

****平心而论，其中一些问题更多的是与浏览器本身有关，而不是自动化工具。然而，这使得认识到当一个自动化工具说它支持多种浏览器时，它不是没有一些创造性、故障排除、跑腿和维护变得更加重要。****

****了解这些问题的存在对于决定是否要自动化浏览器兼容性测试以及自动化程度非常重要。仅仅因为工具声称支持其他浏览器，在决定使用该工具之前就必须意识到这一点。****

****正如编写一个可以在所有浏览器上运行的 web 应用程序没有灵丹妙药一样，自动化也没有灵丹妙药。****