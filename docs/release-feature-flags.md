# 充分利用发布特性标志的 3 种方法

> 原文：<https://simpleprogrammer.com/release-feature-flags/>

![release feature flags](img/5333dd775de670b67c2606ecded9395a.png)

Feature flags are being called one of the next big things in development, and for good reason. Not only are they a key to a true continuous delivery cycle, they can remove the anxiety from a high-stakes release, enable developers to ship new features with confidence and allow for the incremental release of features to test their impact. It’s no wonder, then, that a [Forrester survey](https://www.forrester.com/blogs/feature-management-is-hot-feature-experimentation-is-just-warming-up/) found 31% of teams said feature management is critical to their software development initiatives. What’s more, the [latest report](https://cloud.google.com/blog/products/devops-sre/announcing-dora-2021-accelerate-state-of-devops-report?blaid=2273156) from Google’s DORA team shows elite performers–those using [trunk-based development](https://simpleprogrammer.com/release-trunk-based-development/), including feature flags–deploy 973 times more frequently.

在特性管理领域，发布特性标志——也称为特性切换——是使用最广泛的标志之一。发布特性标志将新特性发布与部署分开，并确保代码的[连续交付](https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912/ref=sr_1_1?crid=2SNNMF6U1OV9Z&keywords=continuous+delivery&qid=1638825729&s=books&sprefix=continuous+%2Cstripbooks%2C809&sr=1-1)。它们可以用于交付不完整的代码，控制发布的展开，将不完整的代码合并到您的主分支中，而不会干扰您的测试或发布过程，并且在您准备好的时候发布。

下面是如何在三种不同的场景中应用发布特性标志:

1.  **将不完整的代码交付生产**

发布特性标志允许您将不完整的、未测试的或者未准备好的代码发布到产品中，而不需要打开它们。因此，特性标志是减少将新代码部署到产品中的次数的有效方法。

当您希望进行持续更新时，您需要一个植根于[持续集成](https://www.amazon.com/Continuous-Delivery-Docker-Jenkins-applications/dp/1838552189/ref=sr_1_1_sspa?crid=2BI11AY6FNXKV&keywords=continuous+integration+and+delivery&qid=1638825788&s=books&sprefix=continuous+integ%2Cstripbooks%2C255&sr=1-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEzRTNXVzhGR1RaMllKJmVuY3J5cHRlZElkPUEwMjQwOTkwMVIzMUhIV0c3S1U4UyZlbmNyeXB0ZWRBZElkPUEwNTY4ODczMlcwWVhSTjFWNVBFJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ==)和部署(CI/CD)的战略。功能标志可用于持续验证用户子集的更改。这个用例允许您更快更自信地发布特性，同时最小化风险。

您可以获得更快的发布、更高质量的特性，并最大限度地降低出错的风险。使用功能标志，您可以通过 CI/CD 部署新版本。准备就绪后，您可以启用新功能，而无需将更新推送到生产环境中，这样您就可以更轻松地推出诸如错误修复或新功能之类的更改。

1.  **控制功能发布和推广**

特性标志为新特性的发布带来了极大的效率，使特性能够快速安全地发布。实现发布标志是一种最佳实践，它允许产品经理按照他们自己的时间表控制一个特性的发布和展示。它还允许软件开发团队或其他利益相关者，如产品和营销团队，提前制定发布计划。

一旦您的特性准备好了，您就可以直接在生产中测试它。您可以将您的功能定位为仅对内部用户、最常使用它的用户、QA 测试人员或 beta 客户可见。还可以通过位置或任何自定义属性将一个特性定位到内部团队。

一个重要的开发者习惯是在[向你的整个用户群发布一个新特性](https://simpleprogrammer.com/best-practices-deployment/)之前从你的客户那里得到反馈，以及控制一部分用户是否可以使用这个特性。然后，您可以基于所选择的 KPI 来评估性能，同时避免向所有用户显示有缺陷的特性所带来的任何损害风险。

有了百分比展示，你只向一部分用户发布一个新的特性，然后逐渐向更多的用户展示。然后，您可以决定您希望向整个客户群中的多大比例的人发布新功能。您还可以决定这些用户中有多大比例的人会首先收到它，然后随着时间的推移将它推广给其他人。

1.  **加速融入你的主要分支**

发布特性标志使得将不完整的代码合并到[主分支](https://simpleprogrammer.com/release-trunk-based-development/)中成为可能，而不会干扰测试或连续的发布过程。这种方法是基于主干的开发不可或缺的一部分，在这种开发风格中，几个开发人员独立地处理小批量的代码，然后将他们的工作合并到主干中，一天一次甚至几次。在基于主干的开发中，代码被直接推送到主干，这实现了更好的版本控制，并帮助团队避免在 Gitflow(又名特性分支开发)模型中更常见的“合并地狱”。

使用 Gitflow，有更多的分支和更大的提交。每个开发人员都有自己的分支，当他们完成时，他们会将分支合并到主干中。不仅将这些长期存在的分支合并在一起更加困难，而且不可避免地会有冲突，因为团队对其他人正在进行的并且可能影响他们的更改视而不见。

发布特性标志，特别是当与基于主干的开发一起使用时，极大地提高了开发和发布新特性的速度和安全性，并且有助于连续交付。因为特性标志可以随时打开和关闭，所以代码可以安全地投入生产，即使它还没有完成，这大大加快了周期时间。这些类型的特性标志还允许逐步发布，因此代码可以在对每个人执行之前，用部分用户组进行测试，以评估其影响。

由于发布特性标志能够帮助您发布更多内容，减少顾虑，它们正在成为每个开发人员工具箱中不可或缺的一部分，并且是安全和成功的持续交付周期的关键。预计在未来几年，发布特性标志将继续改变软件开发和交付的面貌。