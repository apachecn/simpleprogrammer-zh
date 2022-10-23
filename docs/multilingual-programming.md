# tlhIngan pejatlh(我会说克林贡语)-用多种语言编程

> 原文：<https://simpleprogrammer.com/multilingual-programming/>

诚然，我实际上是用这个来翻译这个标题的拉丁字母。我得到这个标题的想法是因为[怪异艾尔的白色&书呆子](https://www.youtube.com/watch?v=N9qYF9DZPdw)。虽然我至少会说一些 JavaScript，但我对克林贡语的精通绝对是不光彩的事。

也许像你们中的许多人一样，在我的职业生涯中，我一直对自己改变技术堆栈的能力感到惊讶，同时仍然符合我的同行群体的技术能力标准。

以下是我迄今为止工作过的技术集合(不包括我的实习):

| **第一份工作** | **第二份工作** | **第三份工作** | **当前工作** |
| ASP。网 | ASP.Net | Java / Spring / Hibernate / Groovy | PHP / Symfony /教义/作曲 |
| 微软 | 微软 | PostgreSQL 和 DB2/400 SQL | MySQL / InnoDB |
| 没有 JS 框架或用法 | VB6，WinForms，WPF | vanilla JS/angular JS/jQuery/Dojo | 安古斯 |
| 没有构建系统 | TFS 建筑代理 | 詹金斯 | 竹子 |
| 文件系统…不是真正的版本控制 | 源安全和 TFS | 饭桶 | 饭桶 |
| 无配置管理 | 虚拟机 | 木偶 | 厨师 |

希望这不会让你觉得我在跟你分享是在吹牛(或者是势不可挡或者是可笑的)。我主要是用这个来帮助我重申约翰最近特别明确的一点，他在给时事通讯订户的电子邮件中推销他的学习课程([如果你还没有注册，你也可以注册！](https://simpleprogrammer.com/about-simple-programmer/))。

作为程序员/工程师，我们最大的财富是我们快速学习的能力。这也是我们许多人日复一日苦苦挣扎的事情。约翰让我们注意到了这一点，并分享了一些关于如何成为更好的学习者的材料。谢天谢地，有了这样的教导，尽管每次换工作时我都要经历一个急剧的学习过程，但我从未觉得这妨碍了我迅速成为团队的积极贡献者。

# 学习一门外语

![Depositphotos_21160265_m-2015](img/496bbfb0eb1bc71ba0aaf3dc71bffa8d.png)

I’ve only got a barely rudimentary knowledge of the Spanish language – but it’s enough of an understanding that I could say the wrong thing and end up with a live chicken instead of some McNuggets. (Chicken the animal and chicken the food have different words in Spanish, you know, like Cow vs. Beef. Chicken in a farm = *la gallina*. Chicken on the table = *el pollo*). One of the things that always helps me when I brush up on my Spanish is finding ways to compare its words and phrases to ones I know in English. A couple of trivial examples, then I’ll explain how my autodidactic learning applies to programming languages, too:

*   卡路里=热
    *   卡路里->将 1 克水的温度升高 1℃所需的能量
*   amor =爱
    *   多情的->表现出、感觉到或与性欲有关的。(这个有点牵强，因为爱≠欲望，但它足够接近，所以行得通。)

学习像西班牙语这样的语言需要理解的主要事情是，它有拉丁语的词根，也就是说，它是一种浪漫的语言。很多英语也有拉丁语词根，所以对我来说，学习西班牙语最简单的方法就是将它与那些看起来有相同(或非常相似)意义的英语单词联系起来。

# 编写一门外国计算机语言

所以，假设你已经花了 3-5 年的时间适应 Java 生态系统。具体来说，您已经开始使用 Spring 框架以及它所暗示的一切。

您在 Spring 中使用的大多数模式(以及其他相关的依赖项)可以很容易地转换成 Symfony(我现在用于 PHP 编程的 Spring 版本)中应用的模式。AngularJS 提供了类似的依赖注入(至少在 1.x 中)。

当你试图将你当前的知识转化到一个新的环境中时，最重要的事情是寻找一些模式，你可以用这些模式作为隐喻来帮助你理解新语言做另一种语言也做的事情的方式。

虽然每种面向对象类型的语言实现这些共享模式的方式都有所不同，但你可以指望它们都存在，并在改变时使用它们的隐喻速记。以下是我所依赖的一些有用的模式，尽管我确信其他模式也存在。

# Getters 和 Setters

虽然这似乎是一个非常明显的声明，但是在编程语言中首先要寻找的是域类管理其属性的方式。通过查看给定语言的 getters 和 setters，您至少可以获得它们如何工作的基本起点结构。

通过查看 getters 和 setters 中的简单构造，您会注意到 PHP 使用$作为变量名，使用->作为设置值，Java 使用“.”，还有。Net 倾向于支持 PascalCase 而不是 camelCase。这里有一个人为的非常琐碎的例子来说明我的意思:

### C#

### 爪哇

### 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

通过这个，你可以看到静态类型语言和动态类型语言之间的区别。Java 和 C#都明确定义 boolean 是存储作为克林贡语使用者的星际舰队学员状态的属性。PHP 没有这样的要求或假设，事实上，您甚至可以指出这些函数需要一个布尔值的唯一方法是使用良好的文档。这种联想的方法不会帮助你学习更复杂的语言结构，但至少它会帮助你看到你目前的语言技能如何从句法上翻译成对你来说是新的。一旦你做到了这一点，你就可以开始寻找其他的东西。以下是一些建议。

# 数据库访问

程序员与数据库打交道。不管我们是否喜欢它，避免它真的不是一个选项。无论如何，我们必须说服其他人的机器将应用程序置于给定的状态，最普遍的方法是将对象数据存储在数据库中。如今，大多数主流公司都会使用某种 ORM(对象关系管理器)。我的一个朋友称之为“对象关系破坏器”虽然我不倾向于反对他，但是你会经常发现你的代码库也使用了 ORM 技术。这也将为您在新的代码库中工作提供一个很好的比较起点。不要误解我的意思——我并不热衷于去适应 ORM 模式。但是，当它们已经存在时，它们是寻找相似之处的好工具。我最熟悉的所有语言都提供了对数据库结构的更直接的访问。PHP 有 [PDO](http://php.net/manual/en/pdo.query.php) ，Java 有 [JDBC](https://docs.oracle.com/javase/tutorial/jdbc/basics/processingsqlstatements.html) ，C#有[ADO.Net](https://msdn.microsoft.com/en-us/library/dw70f090(v=vs.110).aspx#_SqlClient)。所有这三种方法或多或少都将数据库数据分解为数组/映射/集合的概念，其中每一行都由集合中的一个索引条目表示，每一列都由一个名称类似地引用。如果您找到了普通的 SQL，希望它可以作为学习如何将数据对象传输回您的应用程序的基础。

# 文件

很多人认为代码应该是自文档化的，包括我自己。然而，在一个执行严格的模块化和变量命名规则、允许自文档化代码工作的地方工作，并不总是我们可以依赖的现实。如果你不在一个有自文档化代码的地方工作，希望你已经得到了下一个最好的东西，所有的 PHPDoc/JavaDoc/etc。格式良好、整洁且准确。并且，希望您的内联文档也讲述了一个关于代码的好故事。相信你的代码遵守良好的自我记录标准有点不确定。有时文档实际上对理解一门不熟悉的语言很有帮助。有时候你会得到这个:

老实说，对于文档如何在代码库中工作，我有一种复杂的感觉。关于这个主题的更多阅读(以及许多其他关于正确编码方式的令人惊奇的话题)，请查阅这本书: *[干净的代码:敏捷软件工艺手册](http://www.amazon.com/exec/obidos/ASIN/0132350882/makithecompsi-20)* 。说真的。这是大多数开发人员应该至少阅读一次并经常参考的书籍之一。

# 单元/自动化测试

![test-button](img/7aab18cf8b50ad105e87940158991b1f.png)

Hopefully you’re working inside of a codebase where you can run unit tests to get an idea of coverage and functional acceptance. I think that regression protection through an appropriate automated test pyramid is one of the foundational building blocks of being on a good project/product/team.

我大力提倡测试自动化的最大原因之一是，它还教会了一个人如何在他们面前使用代码。希望这些测试写得很好，可以作为代码的指南，让您在理解每个测试证明了什么的同时，学习一些功能。

如果你真的想一头扎进代码库，从测试套件开始。我向你保证没有测试套件完成过。您总是可以找到一些地方来添加另一个测试，这有助于使您的代码更具抗回归性。此外，这是一个非常低的进入门槛——如果你通过编写自动化测试开始学习代码，你不会破坏任何东西。

只要确保你没有签入一个编译失败(或者变红)的测试，除非你想让一个高级团队成员把你[发送到这里](http://www.youbrokethebuild.com/)。

# API 路由

我生活在与 JSON 通信的 Web APIs 的世界里。如果有一件事可以让你确定跨平台的相似性，那就是 HTTP 请求和响应模式都遵循一个严格的契约，不管使用的后端服务器基础设施是什么。

如果您能弄清楚您的应用程序服务器如何将/api/v1/starfleetCadets/转换为流向您的服务层的流量，而不管您正在学习哪种语言，您将会看到类似的模式出现。只要您有一个良好的代码基础，web API 控制器应该做的唯一事情就是将流量从 HTTP 请求导向应用程序逻辑。

当我试图学习一门新的语言时，这是我开始寻找的第一个地方。JSON 在 web API 世界中相当普遍，无处不在，因此它也是在一个新的地方寻找舒适领域的一个很好的跳板。

# 那么，我最喜欢哪种语言呢？

简而言之，全部。编程语言就像杂工腰带上的工具。你不会用螺丝刀在干墙上打洞，也不会用锯子拧螺丝。同样的概念也适用于[编程语言](http://www.amazon.com/exec/obidos/ASIN/0124104096/makithecompsi-20)。有些更适合大型数据集和统计分析(比如 Scala 或 R)，有些更适合让程序员拔毛骂浏览器(比如 JavaScript)。

![Man in ballet tutu isolated on white](img/d31c2f76ecaafad472388de1392db4bb.png)

As I’ve heard before, though, there are two kinds of programming languages. Those that everyone hates, and those that nobody uses. [And then there are those that just make you want to quit programming and go join the ballet](http://www.topdesignmag.com/top-13-most-absurd-programming-languages/).

我用过的所有语言都是我的最爱，原因各不相同。当然，它们都有缺点。但它们都有我觉得有吸引力的优点，并且在有意义的时候喜欢应用到正确的解决方案中。

我们大多数人都没有在一个可以选择哪种语言适合手头特定任务的地方工作。通常，我们正在为技术栈的一部分编码，并且不得不在我们工作的空间里凑合。然而，这不应该限制我们对其他选择的理解。编程既是一门科学，也是一门艺术。没有一种语言能完美地解决特定领域的所有问题。通过努力在混乱中创造一致性，你最终会掌握比你想象中更多的语言。