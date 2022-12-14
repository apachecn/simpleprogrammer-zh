# 领域驱动设计的重要性

> 原文：<https://simpleprogrammer.com/importance-domain-driven-design/>

领域驱动设计(DDD)是一种软件开发方法，它通过将实现与不断发展的模型联系起来，简化了开发人员面临的复杂性。

如果我们把一个概念分成四种成分，然后把它们搅拌在一起，或者把同一个概念作为四种不同的东西放在一个盘子里，哪个更有效？让我们以食物为例，比如一碗辣椒。我们知道，辣椒是由不同的原料(如肉、酱和豆类)制成的，将它们放入锅中，煮 30 至 45 分钟。相比之下，我们的盘子里有牛排、土豆和蔬菜，随时可以上桌。

如果我们要添加/删除项目，哪一个更容易管理:从一碗辣椒中取出豆子和西红柿丁，还是从一个盘子中取出蔬菜并添加另一个食物项目？在这种情况下，chili 代表数据驱动的设计。一层又一层的配料(如豆类、肉类、番茄和调味汁)按顺序排列在一起，构成了完整的食谱。

让我们将这与领域驱动的设计进行比较，在领域驱动的设计中，您有领域(牛排)、有界限的上下文(蔬菜)和单一责任原则(土豆)，其中任何一个都可以被领域之外的不同东西所替代，这顿饭仍然会被认为是一道完整的菜。能够添加/删除有组织的软件是 DDD 的功能，这就是为什么它对软件开发人员和企业所有者的使用很重要。

DDD 的目的是:

*   提供解决难题的原则和模式
*   基于领域模型的复杂设计
*   在技术专家和领域专家之间发起创造性的协作，迭代地改进解决领域问题的概念模型

作为开发人员，我们很兴奋地投入到一个项目中，开始编码，并构建软件。然而，我们不能在没有首先理解客户需求的情况下构建软件。DDD 不仅非常重视理解客户的需求，也非常重视在项目中与他们合作。最终目标不仅仅是写代码，甚至不是构建软件，而是解决问题！

## 理解领域驱动的设计

![](img/bc978e29e66f34147e67cf8ced31e46f.png)

为了更好地理解 DDD，我们需要知道第一个“D”是什么意思——领域。领域是应用程序逻辑围绕的知识和活动领域。在软件工程的世界中，领域指的是应用程序打算应用的主题领域。

创建 DDD 是为了让这个领域成为设计的焦点。DDD 最初是由一位名叫 Eric Evans 的程序员在他 2004 年的书《领域驱动设计:在软件的核心解决复杂性》中介绍并流行起来的。 在 Eric 的书中，他进一步定义了一些在描述和讨论 DDD 实践时有用的常用术语:

*   **语境:**一个单词或语句出现的环境，决定了它的意思。关于模型的陈述只能在上下文中理解。
*   模型:一个抽象系统，它描述了一个领域的选定方面，可以用来解决与该领域相关的问题。
*   **无处不在的语言:**一种围绕领域模型构建的语言，由所有团队成员使用，将团队的所有活动与软件联系起来。
*   **有界环境:**对一个边界(通常是一个子系统或者一个特定团队的工作)的描述，在这个边界内模型被定义和应用。

DDD 的重点是理解如何创建问题领域的抽象模型，该模型可以用一组技术来实现。DDD 是一种方法论，它提供了模型开发和技术开发如何产生一个系统的指导方针，该系统既能满足用户的需求，又能在面对问题领域的变化时保持健壮。

## 如何使用领域驱动的设计

那么我们如何利用 DDD 呢？嗯，我们可以从描述 DDD 过程如何工作开始。

领域驱动设计的过程包括开发人员和非开发人员之间的合作。理想情况下，一个人将拥有一个共享的模型(它是一个可以在不同的有界上下文之间共享的模型)和共享的语言，这样当来自不同领域、具有不同观点的人讨论解决方案时，他们就拥有一个共享的知识库和共享的概念。你可以在这里找到一个概念列表[。](http://uniknow.github.io/AgileDev/site/0.1.8-SNAPSHOT/parent/ddd/core/building_blocks_ddd.html)

## 领域驱动设计的优点和缺点

![](img/76f944f4bfedd87bf3b62d7528ed185a.png)

DDD 是用于软件开发的一个很好的方法。但是，并不建议每个项目都这样做。DDD 有优点也有缺点，对于开发人员来说，在项目中使用 DDD 方法之前了解它们是什么是很重要的。

### DDD 的优势

*   领域驱动的设计给软件开发人员提供了解决软件中棘手问题的原则和模式，有时在商业中。
*   **业务逻辑:**领域驱动设计通过从领域的角度解释需求来创建业务逻辑。根据业务领域概念化系统软件，减少领域专家和开发团队之间误解的风险。
*   成功历史:领域驱动设计在复杂项目中有着成功的历史，与软件开发人员的经验和开发的软件应用程序相一致。

### DDD 的缺点

*   即时时间消耗:软件开发人员必须花费大量时间与领域专家一起彻底了解领域。决定子域和系统边界也可能需要很多时间。
*   **较高的学习曲线:**领域驱动设计的学习曲线较高。开发一种新的思维方式一开始可能会很痛苦。为了有助于高学习曲线，我推荐约翰·桑梅兹的[“快速学习任何东西的 10 个步骤”](https://simpleprogrammer.com/store/products/learn-anything-quickly/)。
*   **如果复杂性不是问题，则不理想:** DDD 旨在简化复杂性。很多时候，复杂性在软件开发中不是问题，比如 CRUD(创建、读取、更新和删除)或者开发数据驱动的应用程序。如果需要简化的话，DDD 是软件开发的一个很好的方法，但是如果不需要，它就不是必需的。

总的来说，DDD 是值得学习的，因为它简化了每个职业关系中都很复杂的一个因素:沟通。DDD 允许开发人员、领域专家、数据库管理员、企业所有者和(最重要的)客户为了解决问题而有效地相互交流。

## 与领域驱动的设计有效沟通

领域驱动设计是编写清晰、可测试代码的有效方法，并提供了解决困难问题的原则和模式。客户通常对代码如何工作或者软件如何构建不感兴趣，但是他们感兴趣的是能够工作的产品。与客户就他们的产品进行有效沟通，而不需要非常专业，这是 DDD 能够提供的最大好处之一。