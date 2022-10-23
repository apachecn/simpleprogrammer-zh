# 如何让搜索引擎爱上你的 AngularJS 应用

> 原文：<https://simpleprogrammer.com/angularjs-app-seo/>

![angularJS SEO](img/14443eddbf3ccb49dcee8a05c11c7111.png)

The market is full of different unique software,  like [emerging front-end development frameworks](https://simpleprogrammer.com/top-10-emerging-front-end-frameworks/) and AngularJS.

作为一名开发人员，您可能在创建网站和应用程序时观察到了一些技术及其优势和挑战。

它是一个用于动态 web 应用程序的 JavaScript 开源框架。AngularJS 是一个开发人员友好的框架，有许多强大的工具和实用程序，如 Angular CMS 工具、后端框架等。

带有 Angular 的 JavaScript 框架在不断发展和增强其能力，以满足搜索引擎的需求。有了每一个内容管理系统，你就能遵循最佳的搜索引擎优化实践，让你的网页在搜索引擎上获得出色的表现；使用 AngularJS 效果会更好。

新的 Angular 版本有编辑和执行元数据的库和许多其他功能，使应用程序 SEO 友好。AngularJS 构建的应用程序被称为单页应用程序(SPA)。这些页面一旦被加载，就会动态地呈现其他页面，而无需再次重新加载整个网页。

Angular JavaScript 通过运行 JavaScript 代码或仅加载所需内容来修改页面。它提高了页面性能，并提供了惊人的用户体验。

然而，AngularJS 网站尽管有许多令人印象深刻的品质，却面临着 SEO 的不利影响。你需要处理元数据代码，并为你的 Angular 站点提供特殊的 SEO 处理，使其在搜索引擎上有更好的表现。

## 搜索引擎上的 AngularJS 问题

对于有棱角的 JavaScript 站点来说，最大的困难是在网络爬虫中的可索引性差。因为浏览器和网络爬虫总是先访问元数据，再通过渲染 JavaScript 访问页面上的文本和链接。

这限制了单页应用程序的搜索引擎潜力，并导致潜在的问题。

尽管 Google 已经提高了索引和抓取 JavaScript 页面的能力，但它仍然不完全可靠。其他搜索引擎在抓取 JavaScript 页面时也面临问题。

## 用 AngularJS 克服搜索引擎问题

为了克服 AngularJS 的搜索引擎问题，你必须知道网络爬虫检查源代码中页面的内容和组件，以确保内容被正确索引。SEO 问题仅仅从这第一点开始。

消除搜索引擎问题的一个解决方案是考虑利用一个预渲染平台，如 Prerender.io。预渲染是一个中间件，它可以抓取您的站点页面，执行所有 JavaScript 文件，并托管您的 Angular 页面的存储(或缓存)版本。

每当请求来自网络爬虫机器人时，它显示缓存版本，而非机器人访问者可以看到实际的角页面，而不是缓存版本。所以，这看起来像是隐形。然而，谷歌已经确认它不是。

谷歌也表达了同样的观点，只要你的期望是进一步开发用户体验，并且访问者可以访问的内容等同于引入到谷歌机器人的内容，这就是合法的。

### 单页应用的搜索引擎优化

正如我们上面讨论的，AngularJS 在搜索引擎上有问题，因此带有 Angular 的 JavaScript 页面显示出 SEO 问题。然而，随着时间的推移，AngularJS 已经发展并找到了解决这一问题的方案。

您可以用有角度的页面创建静态页面；静态页面通常包含正确的元数据和预先呈现的内容，这有助于解决 SEO 问题。

### 为 Angular SEO 设置元数据

元数据是 AngularJS 的一项服务，它为 AngularJS 网页添加 HTML meta 标签，使页面搜索引擎更加友好。这些 HTML 标签是小段代码，它们描述了网页上的内容，如描述、作者、关键字等。

要添加元数据和修改页面，您需要用下面提到的代码更新 home.component.ts 文件的代码。

使用 ng-bind——这有助于将网页的<title>与 AngularJS 中的任何动态变量绑定。</title>

示例:

手动修改 DOM(文档对象模型)——DOM 管理你的网站的 HTML，这是决定你在 SERPs 中的索引的一个因素。

DOM 操纵只不过是与 DOM APIs 进行交互，以修改应该在浏览器上呈现的 HTML 文档。您可以根据需要通过删除、添加或移动元素来修改 HTML 文档。

使用一些指令，使用给定的函数，可以手动编辑 DOM:

### 搜索引擎友好的 HTML 标签

![angularJS SEO](img/08fa944ec098bef35113d9102328015e.png)

The HTML tags help browsers to understand the content, title, and other description well. By adding the tags, you make your pages SEO-friendly and improve their performance on web crawlers.

规范的 URL 标签:规范的 URL 标签就像一个 301 重定向，它有助于通知搜索引擎必须将多个页面视为一个页面，而不会将访问者重定向到新的 URL。搜索引擎支持“规范的 URL 标签”来帮助网站所有者在索引中消除自己创建的重复内容，这有助于您的[网站变得对 SEO 友好](https://simpleprogrammer.com/building-seo-friendly-web-app/)。

这个标签并不新，但是和 nofollow 一样，它只是使用了一个新的 rel 参数。例如:

`<link rel="canonical" href="https://example.com/blog" />`

这将有助于搜索引擎理解页面及其内容。

备选 URL 标签:为了向 Google 发送关于 AngularJS 网站的语言和目标受众的信号，并帮助爬虫理解用户的正确语言或 URL，可以使用 rel="alternate" hreflang="x "注释。

`<link rel="alternate" href="http://www.example.com/" hreflang="en-in">`

请注意，Bing 目前不支持 hreflang 标签。其他方法，如内容语言、标签内容和语言标签，有助于 Bing 理解语言和 AngularJS 网站的目标受众。

### 搜索引擎友好的无哈希 URL

为了在一个页面上处理和维护所有的路线，您在 AngularJS 网站中有一个#。

你可以很容易地把这个#从你的 URL 中删除。

但是一定要从服务器端和客户端删除它，否则你会因为 URL 中的# mode 而继续遇到搜索引擎问题。此外，在请求到达服务器之前，#后面的任何内容都会失去它的能力。

您应该尝试下面提到的步骤来删除#

客户端–将 HTML5 模式设置为 True

服务器端——重写 index.html 的所有内容

你必须启用 URL 重写，并将所有请求转发给 index.html。因为如果你直接通过一个链接打开一个无哈希的 URL，服务器会把它当作一个请求，并试图在服务器上定位文件/应用程序/常见问题，这将给出一个 404 错误，因为任何这样的文件都不存在。

如果您使用的是 Nginx Web 服务器，请在 Nginx 配置文件中添加一个位置块，用于 URL 重写，如下所示:

如果您的 AngularJS 网站使用 Apache Web 服务器，那么编辑您的。htaccess as:

### 角通用也是一个帮助

[Angular Universal](https://github.com/angular/universal) 是 Angular 的预渲染解决方案，可以在构建应用程序的一开始就使用，也可以整合到现有的应用程序中。同样，您可以使用 Universal Bundle 同时进行客户端渲染。

当一个请求到达你的服务器时，Angular 抓取服务器端页面用于底层程序结果。强大的客户端内容被处理并取代了静态代码。在客户会议期间，应用程序继续以客户端模式运行。这使得客户端可以快速准确地连接内容，而不会出现加载或重新加载缓慢的情况。

使用角度通用很容易。即使是新手或者编码知识很少的人，也可以自行部署这个服务器端的 app。这不仅会消除关键的 AngularJS 页面加载速度问题，改善其搜索引擎索引，而且还会消除雇用专业人员处理搜索引擎问题的机会。

## 搜索引擎喜欢你的 Angular.js 应用了吗？

AngularJS 为用户创建了动态网页(即所谓的 SPAs ),以便与他们实时互动。正如我们在上面读到的，如果你遵循[最佳 SEO 实践](https://www.skynettechnologies.com/blog/ecommerce-website-seo)，SPAs 是有效的、以性能为导向的页面，可以降低跳出率，提高 UX。

虽然谷歌和其他搜索引擎正在发展和调整 AngularJS 索引问题，你不应该依赖搜索引擎的能力。

而是尽最大努力在搜索引擎上获得正确的索引，让你的 AngularJS 网站表现良好。因此，如果你的网站是基于任何其他技术，你可以做一些改变，使其搜索引擎优化友好。

上面提到的解决方案(添加元数据、从 URL 中移除#、使用预渲染方法、角度通用技术等。)将帮助您解决 AngularJS 搜索引擎的问题，并提高您网站的质量，因为我们知道，随着我们在搜索引擎方面的改进，网站的整体性能也会提高。