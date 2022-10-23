# 让开关重构更好——默认字典

> 原文:[https://simple programmer . com/making-switch-refactorings-better-defaultable-dictionary/](https://simpleprogrammer.com/making-switch-refactorings-better-defaultable-dictionary/)

我以前写过关于将开关重构为地图或字典的想法。

![](img/b1c34ebe60b700e0c6e13434db391f16.png)

不过，我遇到了一个大问题。由于一个主要原因，Switch 语句和字典在功能上是不等价的…

## 开关允许默认

当我要实现一个字典来代替一个开关时，我一直在为此而奋斗。我该如何处理默认情况？

当然，有许多方法可以处理字典或映射中的默认情况，但是我并不喜欢任何一种解决方案，因为它们要么要求我在查找之前记得检查我的条目是否在字典中，要么依赖于捕获异常。

让我给你举个例子:

将它转换成字典，我们会得到这样的结果:

如此笨拙，只是为了处理默认情况。

做这样的事情会好得多:

现在你可以了！

输入 [DefaultableDictionary](https://github.com/jsonmez/Defaultable-Dictionary) ！

也是我放在 GitHub 上的第一件东西！

这个想法非常简单，我只是为 IDictionary 创建一个装饰器。

DefaultableDictionary 有一个采用 IDictionary 和默认值的构造函数。

然后，它将所有方法委托给传入的 IDictionary 引用。对于查找值的方法，如果字典中不存在该键，它将返回默认值。

我创建了一个扩展方法，让您只需将. WithDefaultValue()放在字典声明的末尾，就可以自动为您提供一个带有默认值的 DefaultableDictionary。

## 睡个好觉，我的朋友

知道您不能创建具有默认值的字典，如果没有找到传入的键，将返回默认值而不是抛出异常。

我毫不怀疑，在第三世界国家，孩子们仍在挨饿，但在第一世界国家，用 VS Express 使用 MonoTouch 破解 iPhone 应用程序的孩子们将不必从不知道如何返回默认值的字典中捕捉异常。

![](img/e35875c410bca97a5d97f9ee8389a582.png)

所以现在没有借口了！重构这些开关！