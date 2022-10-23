# 克服…的局限性。网络核心

> 原文：<https://simpleprogrammer.com/net-core-development/>

![](img/68d4004c50dd6c80b900c48f73ddb7ee.png)

For over a decade .NET Framework was the main platform that [Microsoft](https://simpleprogrammer.com/history-internet-microsoft-corporation/) stack developers could use to write their code. And during all those years, the platform evolved into a feature-rich set of tools, suitable for building any type of application imaginable.

和...一样伟大。NET Framework 有一个主要的缺点—它是专门为 Windows 设计的。这一限制在很大程度上限制了它在构建纯商业和工业用途的应用程序中的使用，因为大多数大中型公司都使用基于 Windows 的工作站，并在 Windows Server 上托管他们的内部网应用程序。这是因为 Windows 是可靠且广泛使用的，有一系列良好的支持选项可用。

。NET Framework 不容易用于消费级跨平台应用程序，因为它不能在 Linux 或 Mac 上本地运行。同样，它也不是建立网站的最佳平台。尽管它提供了构建网站所需的所有工具，但在 Windows server 上托管网站的成本通常是令人望而却步的，尤其是因为大多数托管服务提供商提供的基于 Linux 的托管服务只占成本的一小部分。

微软通过发布新跨平台的同类产品克服了这些问题。公司称之为. NET 框架。网芯。

## 。NET 核心与. NET 框架

两者有很多相似之处。他们使用相同的编程语言。此外，中的许多方面都有所改进。NET Core 基于从其前身的长期渐进发展中吸取的经验教训。

不幸的是。NET Core 缺少许多在。NET 框架。这些例子包括不能。NET Core 播放音频和执行某些图形操作。这是因为这些特性在不同的操作系统上以完全不同的方式实现。

然而，即使这些特性在开箱即用的平台中并不存在，也不是不可能编写自己的实现。

在本文中，我将特别关注如何实现播放音频的能力和构建带有图形用户界面的本机桌面应用程序的能力。然而，这里描述的一些技术将同样适用于。网芯目前缺乏。

## 跨平台音频播放的困难

而。NET Framework 附带了各种可以在 Windows 计算机上本地播放音频的库。网芯自带无。

这是因为音频在不同的操作系统上的架构完全不同。虽然各种现代版本的 Windows 使用相同的标准化国际 API 集进行音频播放，但不同的 Linux 发行版可能会有一些显著的差异。

虽然 [ALSA](https://www.alsa-project.org/main/index.php/Main_Page) 是 Linux 上事实上的标准音频架构，但它并不保证会出现在任何给定的发行版中。即使它存在，也不能保证在所有 Linux 设备上以相同的方式配置。例如，可以通过一个设备上的模拟音频插孔可靠地播放音频文件内容的 Bash 命令，在最好的情况下，在另一个设备上什么也不做，或者在最坏的情况下，只是返回一个错误。

这可能是微软开发者决定不考虑这个特性的主要原因之一。网芯。

### 拯救行动的节点服务

实现音频回放功能的最简单方法是从另一种流行的编程技术中获得一些帮助。

。NET Core 并不是唯一一个独立于操作系统的编程平台。其中最受欢迎的是 [Node.js](https://simpleprogrammer.com/specializing-in-node-js/) 。

Node.js 有一个自己的[限制列表](https://mobiletechtracker.co.uk/geekhub/geekhub-article.php?pagename=popular-misconceptions-about-node.js)，这些限制在。网芯。就像。NET Core，基本安装只包含使平台可用的最基本的功能。任何其他功能都是通过[节点包管理器(NPM)](https://www.npmjs.com/) 由定制包添加的，与其他平台上存在的所有等效库相比，这是最受欢迎的软件组件库。

![](img/abf14b5209b9ad1add6d2d3443a96291.png)

Of course, .NET Core has an equivalent repository of third-party components known as [NuGet](https://www.nuget.org/). However, as the platform is relatively young, there aren’t that many packages on it.

另一方面，Node.js 要老得多。因此，它有许多可用的包，涵盖了几乎所有你能想到的功能。

微软开发者意识到了这一点。这就是为什么他们创建了节点服务库。NET 核心，允许编译后的代码与 Node.js 应用程序进行互操作。

在 NPM 上已经有几个与音频相关的包。而且，在 NodeServices 的帮助下，可以直接从您的。NET 核心代码。

深入研究 NodeServices 的工作原理超出了本文的范围，因为已经有很多关于这个主题的文章发表了。例如，[本页](https://mobiletechtracker.co.uk/geekhub/geekhub-article.php?pagename=how-to-play-sound-on-.net-core)提供了在这种情况下如何使用[播放声音](https://www.npmjs.com/package/play-sound) NPM 套件的说明。

使用节点服务的一个警告是，它不一定是最有效的解决方案。该库依赖于 ASP.NET 核心组件，通常只用于构建 web 托管的应用程序。如果您的应用程序只打算在一台特定的机器上运行，而不是托管在网络上，那么您的应用程序中就会有那些相当大的文件，原因不外乎是为了实现与 Node.js 的互操作性。

此外，您的代码只能在安装了 Node.js 的机器或容器中运行。这是更多的计算开销。因此，这种解决方案并不适用于所有情况。

### 编写自己的音频库

幸运的是，在没有任何第三方依赖的情况下，编写自己的代码并将其编译成音频库的过程并不复杂。

我写的一个这样的库，NetCoreAudio，已经可以在 nuget.org 上找到了。它相当基础，只包含最基本的音频播放器动作。但是，它是开源的；因此，它的代码可以作为编写更复杂库的示例。

它背后的原理很简单，任何熟悉 C#语言环境中面向对象编程的人都应该理解。如果没有，[微软官方参考文档](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/interface)解释了下面使用的“接口”和“实现”的概念。

有一个公开所有可用播放器动作的公共接口，包括播放、暂停、停止和恢复。作为。NET Core 可以在三种不同的操作系统上工作——Windows、Mac 和 Linux——每种操作系统都有自己的接口实现。根类，即由调用库的代码直接访问的库的入口点，确定应用程序运行在哪个 OS 上，并相应地选择接口实现。

在这个特定的库中，Windows 实现通过直接调用特定的程序集来使用[媒体控制接口(MCI)](https://docs.microsoft.com/en-us/windows/desktop/multimedia/mci) ，该程序集存在于任何标准版本的 Windows 操作系统中。

Linux 和 Mac 实现使用不同的方法。由于这两个操作系统都基于一个叫做 Unix 的旧操作系统，所以两个实现都使用[进程类](https://docs.microsoft.com/en-us/dotnet/api/system.diagnostics.process?view=netcore-2.1)。C#使用这个类在后台调用任何外部程序。在这种情况下，它通过 [Unix Bash](https://www.gnu.org/software/bash/manual/html_node/What-is-Bash_003f.html) 启动特定于操作系统的音频工具，这是任何基于 Unix 的操作系统上都有的标准命令行工具。暂停和恢复音频是通过使用相应的“-STOP”和“-CONT”标志的“kill”命令来暂停和恢复过程来完成的。这些标志的用法在[这篇文章](http://www.pervasivecode.com/blog/2010/04/03/unix-tip-kill-stop-and-kill-cont/comment-page-1/)中有更详细的描述。

简而言之，这就是图书馆的工作方式。还有一个教程可以更详细地解释这个库背后的原理。

## 在任何操作系统上启用 GUI

我们已经讨论了音频回放。但是，还有一个重要的特性是。NET 核心，用户和开发人员都希望在任何已安装的应用程序中使用——图形用户界面。

任何原生应用程序，无论是移动应用程序还是安装在桌面计算机上的应用程序，都有一个 GUI。当然，通过文本输入和输出与本地应用程序进行交互是可能的，许多开发人员就是这样做的。然而，这是现在绝大多数用户想要的。可悲的是，这就是。网芯缺乏。

![](img/e8911f7fc7ce5105e2db1bcf03c076fd.png)

.NET Framework has at least three different ways of creating native apps with a GUI on Windows: [Windows Forms](https://docs.microsoft.com/en-us/dotnet/framework/winforms/), [Windows Presentation Foundation](https://docs.microsoft.com/en-us/dotnet/framework/wpf/getting-started/introduction-to-wpf-in-vs), and [Universal Windows Platform](https://docs.microsoft.com/en-us/windows/uwp/design/basics/design-and-ui-intro). However, each of these contains a hint of why none of them can be used on .NET Core in an OS-independent manner: They are all made specifically for Windows.

正因为如此，这些技术不可能被移植到。网芯。此外，由于窗口 GUI 应用程序依赖于特定于操作系统的 API。NET Core 没有任何固有的能力来构建带有 GUI 的本地应用程序。

在其最基本的配置中，您只能构建控制台应用程序。当您添加 ASP.NET 库时，您可以构建网站或 web 应用程序，但这些应用程序的 GUI 只能通过浏览器访问。该平台上没有任何其他类型的应用程序模板。

但是，有一种方法可以将 GUI 添加到您的。NET Core app。解决方案同样来自 Node.js，尽管更加间接。

[Electron.js](https://electronjs.org/) 是一个基于 Node.js 的平台，就像 web 应用一样，它在 GUI 中使用 JavaScript、CSS 和 HTML。但是，它不是托管在任何地方，在其上编写的应用程序可以本机安装。

有一些流行的桌面应用程序就是使用这种技术构建的。使用非常广泛的群聊应用程序 [Slack](https://slack.com/) 的一个客户端就是最值得注意的例子之一。

但是，电子. js 无法通过访问。NET 核心代码，就像纯 Node.js 一样简单。因此，NodeServices 库在这里没有用。

幸运的是，已经创建了第三方库来解决这个问题。它被称为 Electron.NET，并作为一个 [NuGet 包](https://www.nuget.org/packages/ElectronNET.API/)提供。

该库依赖于 ASP.NET 核心组件。这是因为从技术上来说，Electron.js app 是一个 web 应用程序，而不是碰巧作为一个 web 应用程序托管的。它也在自己的窗口中运行，而不是在浏览器中。

因此，使用 Electron.NET，您将创建一个标准的模型视图控制器(MVC) web 应用程序，并在中间件管道中注册一些额外的组件。使用 ASP.NET 核心的任何人都会熟悉 MVC 应用程序模板。然而，你不需要任何服务器软件来托管它。一旦应用程序被编译，您将能够直接从编译代码的位置打开它。

该库的代码是开源的，其 [GitHub 库](https://github.com/ElectronNET/Electron.NET)上的文档包含使用说明，所有这些都使使用它变得非常简单。然而，应用程序代码并不简单。因此，除非您至少具备中级编程技能，并且对 Electron.js 相当熟悉，否则不应该试图修改它。

## 充分利用。网络核心

。NET Core 是一个很棒的平台，它的代码可以在任何 OS 上运行。它唯一的缺点是相对较新，因此，它没有更成熟的编程平台那么多的库。因此，它可能会缺少某些关键业务功能。

![](img/2a4db3aa6a8786c81122df2e801197a2.png)

However, this is something that the developers of .NET Core anticipated. They created NodeServices in order to leverage Node.js, a much more mature OS-independent platform.

我们已经看到了如何使用这个库通过 Node.js 代码在. NET 核心应用程序中播放音频。但这显然不是图书馆的极限。Node.js 中缺少但在 NPM 上可用的任何其他功能都可以被它利用。

虽然这是向中添加任何新功能的最简单的方法。网芯，并不是最高效的方式。C#本身就足以访问任何特定于操作系统的组件；因此，您可以编写自己的轻量级库，在应用程序中添加您想要的任何功能。我们已经看到了如何使用这种方法来编写自己的音频回放库。

识别中缺少的任何其他常见功能。NET Core，并编写一个库来支持它，这对您来说可能是一个很好的辅助项目，可以帮助您获得宝贵的经验并提高您的声誉。也许你写的一个库能让你或其他人构建出解决一个重要问题的伟大软件。