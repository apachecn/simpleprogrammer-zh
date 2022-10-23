# android 演示者使用 juice 进行活动

> 原文:[https://simple programmer . com/Android-presenter-to-activity-using-guice/](https://simpleprogrammer.com/android-presenter-to-activity-using-guice/)

在之前的一篇文章中，我谈到了如何对 android 应用程序进行单元测试。我提到了将一个活动与一个演示者联系起来，但是我并没有真正展示我是如何做的。

有人要求我展示一些示例代码，所以我想我应该解释一下我在这里做什么，看看是否有人有更好的建议。

## 机器人

为了使单元测试更容易，并尽可能地解耦我的系统，我使用了一个叫做 [Roboguice](http://code.google.com/p/roboguice/) 的依赖注入框架。它基本上是移植到 Android 的 Google Guice 框架，并添加了一些 Android 特定的功能。

在使用 Roboguice 时，您最有可能首先遇到的一个挑战是，演示者需要一个对表示其视图的 Activity 类的引用。由于 Activity 类必须创建 presenter，这就带来了依赖注入的挑战。

我们不能只是从我们的容器中请求一个 presenter，然后让它自动解析对活动的依赖。(也就是说，在这种情况下，我们不能依赖构造函数注入。)

## 二传手注射拯救

我们可以做的一件事是，使用 setter 注入而不是 constructor 注入来注入我们的演示者需要的其他引用。

Guice 为我们提供了一种在创建对象后执行 setter 注入的简单方法。我使用这种技术来确保我可以将我的活动传递给 presenter，并且仍然可以将其他依赖项注入到 presenter 中。

下面的代码展示了我的活动中的 OnCreate 方法。

这段代码创建了我的 presenter 的一个实例，它保存了对它所操作的活动或视图的引用。然后，Guice 使用我创建的模块将依赖项注入到任何用@Inject 注释的属性中。

下面是一些演示者设置方法的样子:

您可以看到它们在模块中是这样声明的:

这并不十分漂亮，但 Android 应用程序实际上是一组松散耦合的活动，是代码的入口点。这使得创建我们可能习惯的 MVP 类型的框架变得非常困难。

如果你知道比我正在做的更好的方法，请让我知道，如果你有任何问题或建议，我总是很高兴听到他们或帮助我。