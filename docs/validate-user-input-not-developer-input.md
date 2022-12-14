# 验证用户输入，而不是开发人员输入

> 原文：<https://simpleprogrammer.com/validate-user-input-not-developer-input/>

我有一个非常简单的规则，我喜欢遵循它来简化我的代码。

> “不验证开发人员的输入”

这条规则仅仅意味着我们不应该尝试和验证来自非用户或外部系统的输入。

换句话说，不要验证你在自己的代码中传递的参数。

**(了解你自己)**

**[](https://simpleprogrammer.com/wp-content/uploads/2012/04/knowthyself.jpg)**

**![knowthyself](img/e41ccd5387b774fbfc67d4cc42fc4fed.png "knowthyself")**

**

虽然您不能保证来自其他来源的输入是有效的，但是您可以知道您自己的代码的输入是有效的。

当编写一个方法时，我们应该努力知道是谁在调用这个方法，并让方法的调用者负责不要传入垃圾。

我知道这不是一个流行的观点，因为它似乎违背了“防御性编程”的思想，但是防御性编程的思想被误解了。

查克·诺里斯自己曾经说过:

> 他们说最好的防御就是不去冒犯。



![defense](img/967bcf3e6106d9d6aae022cfe58ada21.png "defense")



那句口号在这里很适用。您的策略应该是确保您总是将有效值传递给方法，而不是试图编写方法来防御错误的输入。

(大家不要不文明！)

让我给你举个例子:

那些代码看起来是不是很傻？

这与我的建议完全相反。

与其试图决定我们应该保留这些检查中的哪一个，并试图遵循一些复杂的规则来决定我们什么时候应该像这样验证输入，我只是建议我们**去掉所有的检查！**

在之前，我已经写了关于不检查空值的文章，但是我现在确信，检查来自你控制的代码的任何输入都是一种代码味道。

## 你能做什么？

往好里说抛出异常，往坏里说推断调用者的意思，破坏数据。

在那里抛出异常有什么用？如果你尝试去引用一个空对象，你会得到一个异常。

如果你抛出一个异常，你会捕捉到它吗？

如果是这样，这是否意味着您在 try / catch 块中包装了您进行的每个方法调用？

试图验证由您控制的代码传递给您的输入的最大问题是，您实际上不能做任何有用的事情。你只是弄乱了你的代码。

另一个问题，如果你仍然热衷于验证所有方法调用的输入，你会这么做吗？

你是真的检查每一个参数，还是只是在你记得的时候。因为，如果你不统一使用支票，你就不能指望他们。

## 语境

我提倡验证传递到方法中的内容而不是传递到方法中的内容的一个主要原因是上下文。

如果你在一个方法中，有人传递给你一个空值，你就没有上下文。

是什么导致这个参数为空？我不知道——我不可能知道！

但是——另一方面，如果我要调用一个方法，并且我要给这个方法传递一个空值，我知道为什么。我知道我得到的列表是空的，我可以检查一下，然后把一个空列表传递给我要调用的方法。

更好的是，我可以更进一步，永远不从最初返回列表的方法返回 null。

关键是在调用方法之前，你有更多的上下文，而不是在方法中。如果您要验证输入，请在上下文允许您做一些有意义的事情的地方进行验证，而不是仅仅抛出一个随机异常。

## 更好的代码

这样思考会迫使你写出更好的代码。我坚信。

我们大多数人并不真正考虑我们传递给方法的是什么，或者我们是否从方法中返回空值，相反，我们倾向于考虑我们传递的是什么。

通过改变事物，它引导我们进入更好的不容易出错的编码实践。

我们不得不考虑标准化和[限制参数值](http://elegantcode.com/2010/05/08/the-power-of-enum/)的范围。

我们被迫开始考虑使我们的对象不可变，这样，如果我们正确地初始化它们，它们就不能包含空值。

最重要的是，我们的代码变得更干净，因为它没有错误检查。我们不是到处检查错误，而是以一种防止错误发生的方式编码。

所以下一次当你想通过另一个你能控制的方法来验证传入你的方法的参数时，不要这样做！

如果你不能相信你自己，你能相信谁？(也许是查克·诺里斯？)**