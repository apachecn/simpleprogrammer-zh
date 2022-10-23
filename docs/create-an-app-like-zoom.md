# 如何建立一个像 Zoom 这样的应用程序

> 原文：<https://simpleprogrammer.com/create-an-app-like-zoom/>

![create app like zoom](img/1b7cd7779c856ebed55f4a239c4c0c6c.png)

During the COVID-19 pandemic, there were multiple businesses that fell flat on their faces, while others rode the tide and came out on top. Uber should definitely be considered one of the disasters, suffering heavy losses and announcing to about [3,500 employees](https://www.firstpost.com/business/uber-lays-off-3500-employees-in-a-three-minute-long-zoom-call-says-today-will-be-your-last-working-day-8369211.html) they were fired in a three-minute-long Zoom call.

你看到我做了什么吗？如果你是一个有洞察力的读者，你一定已经发现我不仅举了一个苦苦挣扎的公司的例子，也举了一个做得很好的公司的例子。

Zoom 是极少数不被看好的公司之一，在这次疫情中，它不仅兴旺发达，而且广受欢迎。Zoom 是一款视频会议应用，已经成为从休闲视频通话到企业商务电子会议的必备工具。

像 Zoom 这样的应用是雄心勃勃的项目。了解它们的实现将有助于您提出更全面的策略。在这篇文章中，我们将快速浏览一下使 Zoom 成功的基本元素，并且我将分享一些关于如何创建类似东西的技巧。

## 你的 App 需要具备哪些功能？

我们都听说过 Skype，它是早在 2003 年就出现的视频会议应用程序之一，而 Zoom 直到 2011 年 4 月 21 日才推出。

但我们都知道，当疫情开始时，Skype 上的形势是如何逆转的。这么说吧，没人再谈论 Skype 了。虽然 Zoom 的营销团队功不可没，这使它在目标受众中脱颖而出，与其他应用程序不同，但大部分成功是 Zoom 基本功能的结果。

### 虚拟背景

视频会议的互动性更强了，因为你可以改变会议的背景。没错，如果你有一个绿色屏幕，你可以用任何图像替换背景，这有助于确定会议的基调。

微软团队也推出了同样的功能，以便跟上。有预设的主题供您选择，但如果您愿意，也可以上传自己的主题。公司在他们的虚拟活动中使用这个来闪现标志。

### 记录

使用缩放功能，您可以录制视频会议。考虑到你可以通过 Skype 甚至谷歌视频聊天工具做同样的事情，这并不特别，但考虑到它允许 500 人参加会议，企业更喜欢举办大型活动而不是应用程序，这使得记录功能变得更加不可或缺。

### 图库视图

Zoom 的最大特点之一是它能够同时允许 500 人参加视频会议。现在，如果你有这么多人，必须有一个界面在屏幕上显示所有加入的人。Zoom 的图库视图允许您对会议有更广阔的视野。您可以在一个图库视图中打开多达 49 个窗口。

### 屏幕共享

如果您可以访问一些重要信息，并希望通过电话与其他成员分享，只需分享您的屏幕即可。在工具栏上，有一个“[分享屏幕](https://support.zoom.us/hc/en-us/sections/201740106-Screen-Sharing)”图标，你可以点击它分享你屏幕上发生的任何事情。你可以选择是共享整个桌面还是只共享一个窗口。

### 美颜模式

直到现在，我们只在智能手机上听说过图片中的美颜模式。但是如果你想做一个重要的演讲，为什么不在演讲的时候看起来漂亮一点呢？嗯，Zoom 支持美颜模式，是极少数支持这种模式的会议应用之一。在那里，你可以在应用程序的视频设置下找到“修饰我的外观”按钮。

### 基本隐私

![create app like zoom](img/8eb02b32f9144097183daf7ae462fe06.png)

If you don't want others to see you or hear you, you can easily turn off the camera and mic on Zoom. You can already mute before going on the call by simply opening the in-app settings, selecting “audio,” and then tapping on the mute microphone icon before joining a meeting. On the desktop, you can mute and unmute the audio by clicking on the space bar.

### 端到端加密

端到端加密确保所有对话都是保密的，该组之外的任何人都无法访问。像 AES-256 和 HMAC-SHA256 这样的协议保证了对话的安全。

然后，这些协议将数据分成 256 位的长块，然后加密，传输到目的地，最后在接收方解密。

### 噪声消除

背景噪音破坏了谈话。也许正在施工，或者背景中有小孩在玩耍，这需要尽可能地减少。得益于深度学习算法，它可以轻松地将用户的声音从背景中分离出来，并用白噪声抑制同样的声音。

### 虚拟举手

当会议中有太多的参与者时，主持人需要知道在那个时刻谁想发言。这是通过使用一个设计成举起手的虚拟表情符号来完成的。在你的应用程序中集成这一功能非常重要，因为它可以防止多个用户同时发言，从而帮助你保持会议的礼仪。

## 像 Zoom 这样的应用的技术要求

下一步是了解开发像 Zoom 这样的应用需要哪些技术。在这里，我们看一下您需要的一些方面，以及这些方面将采用的技术:

### 网络服务器

无论何时你访问互联网，你都在访问存储在某个地方的文件，而这个地方就在“网络服务器”中。当浏览器通过 HTTP 请求文件时，web 服务器存储可以被访问的数据。

Zoom 使用[亚马逊网络服务](https://aws.amazon.com/)作为其服务器，因为需要一个可靠的服务器来无延迟地处理大量的呼叫(数千个)。Microsoft Azure、Apache 和 Serverspace 是您可以选择的一些流行的服务器示例。

### 后端开发

如果你想创建一个视频会议应用程序，你首先需要考虑的是服务器端或后端。通过后端开发，你可以确保没有任何影响用户使用应用程序体验的错误或故障。

虽然一些应用程序可以使用现成的 BaaS(后端即服务)解决方案，但像 Zoom 这样的应用程序需要更复杂的技术，最好从头创建一个服务器。Zoom 使用 React JS、Angular JS 和 Vue 作为后端。

### 前端开发

处理完后端之后，您必须考虑拥有一个有吸引力的用户界面和用户体验。一个直觉的 UX 是你应该努力争取的。就拿 Zoom 本身来说，看看它有多人性化，多轻便。

你可以阅读更多关于[设计心理学](https://growth.design/psychology/)的内容，以了解你如何拥有一个让你的[完美观众](https://shanebarker.com/blog/perfect-audience-review/)兴奋的最佳设计。Zoom 在其前端使用 HTML、CSS 和 JavaScript。

前端开发的 app 包括 ewebrtc API(media stream、RTC DataChannel、RTCPeerConnection，以及 Pubnub、CometChat、OpenVidu 等实时聊天和通信 API。)

## 像 Zoom 这样的应用程序的移动应用程序技术要求

### iOS 应用程序

要创建一个基于 iOS 的视频会议应用，你可以使用 Swift。它被设计成与苹果的 Cocoa 和 Objective-C 代码一起工作。此外，Swift 是由苹果开发的，用于构建原生 iOS 应用程序。在使用第三方服务构建会议应用程序时，使用 Swift 更容易、更快捷。

总结一下，这就是你所需要的一切:

*   编程语言:Swift
*   工具包:苹果代码
*   视频聊天:WebRTC
*   SDK: iOS SDK

### 安卓应用

Java 和 Kotlin 用于开发原生 Android 应用。这两种编程语言在业界都以[构建功能强大的应用](https://www.amazon.com/dp/B01N4WQRQA/makithecompsi-20)而闻名，但更重要的是，这两种编程语言都有出色的应用性能、第三方集成和 UI/UX 可能性。

总而言之，这就是你所需要的一切:

*   编程语言:Kotlin、Java
*   工具包:Android Studio
*   视频聊天:WebRTC
*   SDK: Android SDK

### 第三方 API

API(应用程序编程接口)是一组能够在一个软件产品和另一个软件产品之间进行数据传输的代码。API 还包含数据交换的条款。它使用[函数调用](https://www.computerhope.com/jargon/f/funccall.htm)来触发软件执行特定的动作和服务。

以下是您通常在 Zoom 等移动应用程序中使用的一些第三方[API](https://simpleprogrammer.com/apis-help-developers-build-apps/):

*   Vonage 视频 API(前身为 TokBox OpenTok)
*   Wowza GoCoder SDK
*   PubNub
*   Twilio
*   CometChat
*   Quickblox

## 像 Zoom 这样的应用程序真的很有吸引力

![](img/8532b8726ebe938a5bc961b08159d5e7.png)

An MVP (Model-View-Presenter) of the Zoom video call app consists of a user profile, user registration, search and add friends, text calls, voice calls, group chat videos, video calls, settings, and user list modules.

根据应用程序开发团队的功能、设计和小时费率，在美国或加拿大等第一世界国家，定制视频会议应用程序开发的平均成本为 70，000 美元到 100，000 美元。

如果你从印度或印度尼西亚这样的国家雇佣一家离岸开发公司，那么开发成本可能会降到 45，000 到 70，000 美元。

然后你还要在雇佣跨平台开发者和原生应用开发者之间做出选择。例如， [React 原生开发者](https://www.resourcifi.com/hire-react-native-developer/)可以帮助你开发一个跨平台的移动应用，这意味着一个适用于两个平台的应用。

然后，你甚至可以选择雇佣一名 iOS 或 Android 开发人员，即一次为一个平台开发一个应用程序的人。如果你想让你的应用在两个平台上运行，你需要两个开发者。

总而言之，像 Zoom 这样的应用程序在许多情况下都是非常有吸引力的解决方案——无论是电子学习应用程序还是在线活动应用程序——可能性是无穷的。像 Zoom 这样的应用程序不断提供新的创新功能，这使得该平台有利于学习和远程工作。所以为什么不创造你自己的呢！