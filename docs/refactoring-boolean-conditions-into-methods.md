# 将布尔条件重构为方法

> 原文:[https://simple programmer . com/refactoring-boolean-conditions-into-methods/](https://simpleprogrammer.com/refactoring-boolean-conditions-into-methods/)

有些人真的真的不喜欢把布尔条件重构成私有方法。有一次，有人告诉我，如果他们看到这样的代码:

他们会找到我并杀了我。我想知道[鲍伯·马丁](http://www.amazon.com/Robert-C.-Martin/e/B000APG87E/?_encoding=UTF8&camp=1789&creative=390957&linkCode=ur2&tag=makithecompsi-20)是否收到了很多死亡威胁，因为他在他的书“[干净代码:敏捷软件技术手册](http://www.amazon.com/gp/product/B001GSTOAM/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B001GSTOAM&linkCode=as2&tag=makithecompsi-20)

![](img/ea3d5605bb0a5c48c61846f3a9222927.png)

[](http://www.amazon.com/gp/product/B001GSTOAM/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B001GSTOAM&linkCode=as2&tag=makithecompsi-20)”中提倡这种做法，我目前正在阅读这本书。

自从我读了“[代码完成:软件构造实用手册](http://www.amazon.com/gp/product/B004OR1XGK/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B004OR1XGK&linkCode=as2&tag=makithecompsi-20)之后，我就一直在做这种重构

![](img/5e7203a5157afe1e21d6c617a58bcb15.png)

“.  (By the way every time I mention this book, I feel obligated to tell you that if you have not read this book, go read it now.  Seriously.  Buy this book and read it.)

现在，我上面展示的例子有点“简单”，但它仍然比将 *ProgramCode ==“特殊代码”*留在 main 方法中更容易阅读。(暂时忘记“特殊代码”应该是一个常量。)

让我们看一个不那么琐碎的例子:

在这个例子中，更不清楚逻辑试图做什么。当你阅读这段代码的时候，你必须在心里弄清楚所有这些布尔语句实际上在测试什么。

告诉我…这样更好理解吗？

如果你觉得第一个例子更容易理解，那你就比我聪明多了，因为我就是不能把第一组布尔条件绕在头上，(而且是我写的)。写一行小方法似乎很傻，但是价值是抽象的。这些单行方法使理解代码做什么变得容易得多，并允许您选择“放大”逻辑的级别。

*   你可以选择不关心猫如何决定吃东西，而只是从*的层面来看，如果猫决定吃东西，那他就吃。*
*   或者你可以从*这只猫如何决定进食的层面来看。*
*   或者你可以再缩小一个，看看*那只猫喜欢什么样的食物*级。

编写好的代码是为了让代码易于阅读和理解，而不是让代码紧凑。

你怎么想呢?你同意重构布尔条件吗？