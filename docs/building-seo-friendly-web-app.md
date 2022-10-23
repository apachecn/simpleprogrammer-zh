# 开发人员构建 SEO 友好的 Web 应用程序指南

> 原文：<https://simpleprogrammer.com/building-seo-friendly-web-app/>

![building seo-friendly web app](img/7bd5a7b5602179a0c4252cc516ba48f0.png)

Search Engine Optimization (SEO) helps attract users who are truly interested in your service/content, which is a top reason why you need to apply SEO techniques when developing an app. However, when talking about [SEO for developers](https://neilpatel.com/blog/seo-developers/), the recommendation isn’t that developers should do SEO, but instead that a developer should make sure that a website is SEO-ready.

网站的生存能力、可见性和灵活性都落在开发者的肩上。一个 SEO 友好的 web 应用程序初看起来可能很容易，但是有一些特性应该被考虑到——例如，React 和 SEO 的问题，我们很快就会看到。

目前的指南将有助于阐明开发者应该做些什么来确保他们的网站与搜索引擎很好地合作，特别关注 SEO 和 React.js 的结合。

## 为什么需要 SEO？

web 开发没有 [SEO 走不远。换句话说，如果你正在为你的网站寻找有机的流量，没有什么比 SEO 更好的了。搜索引擎优化让那些正在搜索你提供的内容/服务类型的用户更有可能登陆你的网站。](https://moz.com/blog/javascript-seo-guide)

当你建立一个搜索引擎友好的网站时，你的主要目的是[进入前 5 名搜索结果](https://www.amazon.com/How-Get-Top-Google-2022/dp/B09QP86BLJ?ref_=Oct_d_onr_d_6133991011&pd_rd_w=dr5kv&pf_rd_p=9493a408-b460-43d0-bc2e-eb7b6f6520ed&pf_rd_r=0M7VNH1AA9DTXA6RBC3B&pd_rd_r=0f2d063c-4e74-407b-b84f-91c88123bf39&pd_rd_wg=7jair&pd_rd_i=B09QP86BLJ)。SEO 的主要目标是让搜索引擎算法相信你的网站符合用户的要求。

作为一名开发者，你需要做一些调整来确保网站在搜索引擎上有很高的可见性。让我们一个一个来看。

## 为搜索引擎优化组织内容

为了让搜索引擎发现你的内容，它必须以一种允许他们“看到”的方式来组织。要确保这一点，您需要做几件事情。

### HTML Meta Tags

为了在搜索时识别内容的类型，Googlebot 会寻找某些 [HTML 元标签](https://simpleprogrammer.com/html-meta-tags-guide-programmers/)，也称为标题和描述。meta 标签必须包括与你的网站相关的关键词——用户在浏览器搜索框中输入的单词和短语。最相关的关键字必须在 H1 标签和 H2 标签中使用，并且不应该超过 60 个字符。

描述标签并不重要，但是它给用户提供了关于页面内容的所有必要信息，并说服他们点击进入。它不应该超过 150 个字符，包括空格，并且应该包括关于文章内容和有用性的简要信息。

### 对找到的页面进行优先级排序

爬虫是由搜索引擎操作的互联网机器人，主要功能是网页索引。阻止他们访问某些页面——例如，对流量不重要的页面——将有助于避免应用服务器不堪重负。为此，您可以将 noindex robots meta 标记添加到页面的 HTML 代码中。

### 以正确的方式构建数据

Google 使用网页中的结构化数据以特殊格式(例如，带有链接和图像的特殊卡片)显示在搜索页面结果上。这就是所谓的“丰富的结果”你可以使用谷歌的丰富结果测试来检查你的页面是否支持丰富的结果。

## 用搜索引擎寻找站点可见性

确保谷歌看到你网站的所有重要页面是至关重要的。这些页面拥有最有价值的内容(尤其是登陆页面)。谷歌分三步对网页的优先级进行检查和排名。

### 爬行

正如我前面提到的，爬行是搜索引擎在互联网上查找更新内容的过程，例如新网站、页面、网站更改、媒体、文件和死链接。在这个过程中，谷歌使用了 Google bot——一种特殊的网络爬虫，它使用一种算法来确定要抓取哪些网站以及抓取的频率。

不管格式如何，内容都是通过链接发现的:Googlebot 首先加载一些网页，然后根据这些网页上的链接找到新的 URL。爬行器沿着链接的路径跳跃，找到相关的材料并将其添加到检测到的 URL 的库中。这就是 Googlebot 发现新内容的方式。

让谷歌理解你的网站是谷歌机器人能够在搜索中找到你的网站的必要条件。这可以通过以下建议来实现:

*   页面加载速度是便捷用户体验的一部分，对 SEO 来说极其重要，所以你必须**确保页面快速加载**。这是 Googlebot 在对页面进行排名时考虑的因素之一。页面加载时间不应超过三秒。这就是为什么你必须尽一切可能来提高页面的加载速度:优化图片的大小，减少重定向的数量，等等。

*   重要的是**确保你网站上的所有页面看起来都是正确的**,这样 Googlebot 就可以找到它们。这意味着 Googlebot 必须能够看到并理解页面的所有元素。

*   如果你经常添加新页面或更新内容，**使用 sitemap**——一个特殊的文件，提供关于页面内容及其元素的信息。这样，你将减轻搜索引擎的工作，使爬行更有效。

*   改进你的主页:访问者应该在进入网站后就能看到你的网站是关于什么的。方便的导航系统也是很重要的一点。

### 索引

![](img/31e14e5013882ffc5f102f62d4a55073.png)

Search engines process and store the information they find in a content database. Once the search engine processes each of the pages viewed, it compiles an index of the visible words and their location on each page. The information is organized and interpreted by a search engine algorithm to measure importance compared to similar pages.

对于一个在搜索引擎结果页面上排名靠前的站点，确保搜索引擎正确抓取和索引该站点是很重要的。否则，他们将无法在搜索结果中对网站内容进行排名。

这是您改进索引的方法:

*   创建简短且信息丰富的标题。长标题对读者来说没有吸引力。短标题能让用户在一秒钟内理解文章的内容。

*   确保标题反映了页面的内容。大多数读者倾向于阅读标题来熟悉文章的内容并找到他们要找的信息。

*   **给出文本格式。**谷歌比图像和视频更理解文本，所以以文本形式提供所有关于页面的重要信息，对视觉内容使用标题。

### 等级

页面排名是基于许多不同的方面。除了技术细节，谷歌还比较了各种因素:网站类型、背景、视觉布局等。所有这些因素都有助于搜索引擎从其索引库中找到最相关的答案，并根据用户的查询提供这些答案。

要提高排名:

*   提供有用的最新内容。确保不断为访问者提供新鲜的内容，让他们始终觉得你的网站有用。
*   **确保便捷的用户体验。**你网站的设计和导航系统应该简单直观。
*   当然，正如已经提到的，要确保你网站的所有页面都能快速加载。

## 设备和编程的注意事项

除了我上面给你展示的领域，还有一些更具体的事情你需要记住。正如我在导言中提到的，其中一些涉及某些技术特性。让我们来看看它们

### 针对所有设备进行优化

如果你的网站只针对网络浏览器进行优化，你会失去很多有价值的流量，所以所有的内容(文本、图像、视频)都应该在移动设备上可见。此外，移动友好也是谷歌排名算法的一部分。为了确保你的网站是手机友好的，你可以使用[手机友好测试](https://search.google.com/test/mobile-friendly)。

### 修复与搜索相关的 JavaScript 问题

Googlebot 可以运行 JavaScript，但是有一些限制和特性需要考虑。例如，如果您想使用 React JS 创建一个单页面应用程序(SPA)，您必须知道 SPA 是在客户端呈现的，这会对 SEO 产生负面影响，使初始加载时间更长。

这样，你需要使用一个 SEO 友好的 JavaScript 框架来启用服务器端渲染(例如， [Gatsby.js](https://www.gatsbyjs.com/) 或 [Next.js](https://nextjs.org/) )。这样的 JS 框架旨在使单页 React 应用程序 SEO 友好。这样做，就可以把 [React.js 和 SEO](https://clockwise.software/blog/seo-for-react-apps/) 结合起来。

### 关注网站的表现

你的网站的完美表现是你确保它有高排名的关键。要检查你网站的状态，运行[谷歌灯塔](https://developers.google.com/web/tools/lighthouse/)。这是检查网站的可访问性和性能以及提高网页质量的有效工具。

### 确保你的网站是灵活的

SEO 需要内容经理、分析师、设计师和其他贡献者不断的调整和改变。当你开发你的网站时，你需要确保它的灵活性:你应该在每个页面上有一个可编辑的标题标签，并使元标签和图像 ALT 属性在 CMS 中可编辑。

## 搜索引擎优化友好的网络应用是值得的

在这篇文章中，我为你提供了宝贵的建议，告诉你如何制定自己的搜索引擎优化策略并创建一个搜索引擎优化友好的网络应用。

当然，您可能认为担心 SEO 超出了开发人员的能力范围，但是像创建响应式界面和 React.js 以及 SEO 交互这样的事情，只有开发人员才能完成。而且，你可以使用很多技术性的 SEO 做法，让网站在搜索引擎上排名靠前。

最后，搜索引擎优化友好的网络应用程序值得你在这个过程中投入时间和精力。SEO 优化的应用带来更多的流量，这意味着更高的收入或结果。