# 测试的正确测试用例设计——第 2 部分——边界值分析

> 原文：<https://simpleprogrammer.com/proper-test-case-design-for-testing-part-2/>

本系列的第二篇文章关注于使用黑盒测试的高效测试用例设计。这些帖子的目标是让你更好地设计测试用例，这样你就可以开发更高质量的系统。深入的解释和实践练习是这些教程的核心。

在本教程的第一部分，我们讨论了:

*   一个设计良好的测试用例是什么
*   不同类型的软件测试
*   黑箱测试
*   等价划分

## 边界值测试

今天，我们将继续学习黑盒测试技术。具体来说，我们将学习***【BVT】***。BVT 进一步扩展了你在等价划分教程中掌握的概念。您将利用等价划分技术来帮助您进行边界值测试。

在上一篇文章中，我从一个非常简单的测试用例开始。我将在这里进一步阐述它。

*测试场景*

考虑以下情况，其中文本框允许输入以下整数:

1–5 次成功

5–9 只猴子

9-11 根香蕉

使用你新发现的技能来创建等价类。(*见下面完整的例子。*)你可能会注意到你在所有的 ***边界*** ，或者 ***边缘情况*** 都遇到了问题。例如，如果输入 5，返回的是“成功”还是“猴子”？9 号也是一样。那会返回“猴子”还是“香蕉”？

软件测试中测试边缘条件被称为 ***边界值测试*** 。这个名字很有意义，是不是很棒？

## 边界值测试

### 

![Silhouette man walking musing looking up](img/b2c4fc65cf425c6be59d79cf05d8f10c.png)

什么是软件测试中的边界值测试？

BVT 用于测试等价划分之间的边界。BVT 最适用于输入值是连续范围的情况，原因很简单，因为这里存在很多缺陷。让我们考虑一下前面的例子。

*测试场景*

考虑以下情况，其中文本框允许输入以下整数:

1–5 次成功

5–9 只猴子

9-11 根香蕉

具有任何技能的开发人员都会编写类似这样的代码:

显然，你会遇到前面提到的重叠条件的问题。然而，涉及边界的最大问题是开发人员错误地编写了不正确的等式运算符。而不是“< =”，他们可能编码“

这种错误很常见。这就是 BVT 如此有效的原因。我在凌晨 2 点编码时犯过这样的小错误，我也见过真正聪明的开发人员犯同样的错误。我们都是人。

### 设计边界值测试用例的步骤是什么？

1.  确定等价类
2.  确定每个类别的界限
3.  为每个边界创建测试用例

*   a)边界下的一个点
*   b)边界上的一个点
*   c)边界上方的一点

### 练习设计一个测试用例

*简单场景*

让我们假设有一个文本框，它接受从 1 到 5 的整数范围。

1.  *识别等价类*

2.  *确定每类的边界*

边界是可能出错的边缘，比如输入不正确的相等运算符。

3.  *围绕每个边界创建测试用例*

因为我们的度量单位是一个整数，所以我们的测试单位也是一个整数。因此，每个边界的正负 1。如果我们的单位是一个有两个小数点的百分比，你的测试用例将会是每边界正负 0.01。在这个场景中，有两个边界，有六个边界测试用例。

### 边界值测试的优点是什么？

BVT 是一个很好的方法来发现你的应用程序中的错误。这项技术非常容易应用，但非常有效。当你的测试时间很短时，这种技术可以为你的努力带来最好的投资回报。

### 边界值测试的缺点是什么？

与所有黑盒测试技术一样，BVT 不保证测试应用程序(AUT)的完全测试覆盖。它有可能使应用程序的许多部分未经测试。理想情况下，BVT 应该与[其他测试设计技术](https://simpleprogrammer.com/2015/08/05/specification-based-test-design-techniques-enhancing-unit-tests-part-1/?preview_id=14034&preview_nonce=c00d9f4915&post_format=standard&preview=true)一起使用，以最大化测试覆盖率。

### 边界值测试练习

*更复杂的场景*

让我们假设有一个接受从. 50 到. 60 范围内的数字的文本框。测试该系统所需的所有边界值条件是什么？

想想这个。界限是什么，界限周围的数字是什么？

*解决方案*

等价类的界限是 0.50 和 0.60。因此，您需要一个测试用例，一个在边界下，一个在边界上，一个在边界上。

您将到达六个测试用例:. 49，. 50，. 51，. 59，. 60，. 61

*测试场景 2*

让我们假设有一个接受从. 50 到. 52 范围内的数字的文本框。使用 BVT，测试该系统需要哪些测试用例？你自己想想这个，把答案写下来。提高保留率！

*解决方案*

所有需要的测试用例都是:. 49，. 50，. 51，. 52，. 53。没错，你只需要五个测试用例，而不是六个。当某个边界值属于不同边界的等价类(. 51)时，您不需要重复那个测试用例。只需使用它并测试两个相关的分区。

*测试场景 3*

一家名为软件测试抵押贷款(STM)的抵押贷款公司将根据此人的收入水平发放抵押贷款。只有当这个人的月收入在 1000 美元到 5000 美元之间时，他们才会发放抵押贷款。此外，STM 只会给每个人发放 1-2 笔抵押贷款。

使用 BVT，创建测试该场景所需的所有测试用例。像往常一样，使用尽可能少的测试用例。

*解决方案*

不要不知所措，只要一次一步地遵循所有的步骤。这个场景的不同之处在于，有三个变量影响我们的测试用例，而不仅仅是一个。因此，我们需要在 x-y 坐标图上绘制我们的数据，而不仅仅是单维数字线。

凭借我出色的图形[设计](https://simpleprogrammer.com/2015/06/08/design-patterns-simplified-the-bridge-pattern/)技能，我创作了下面这个给大家举例。

注意 x 轴代表每月收入，y 轴代表房子数量。红点代表无效分区，绿点代表有效分区。在交叉点处，颜色并不代表正确的分区，因为该点可能对一个分区有效，而对另一个分区无效。

一切完成后，这几乎看起来像一个笛卡尔坐标平面。要创建测试用例，只需选择一个起点和起始轴。我从 999 开始，这是 x 轴上的无效收入。之后，只需遍历所有其他分区的 y 轴。

这个过程将为 y 轴上的每个边界值(房屋数量)乘以 x 轴上的每个边界测试用例(每月收入)产生四个测试用例，总共产生 24 个边界测试用例。

| 收入 | 房屋数量 | 预期的 |
| Nine hundred and ninety-nine | Zero | 病人 |
| Nine hundred and ninety-nine | one | 病人 |
| Nine hundred and ninety-nine | Two | 病人 |
| Nine hundred and ninety-nine | three | 病人 |
| One thousand | Zero | 病人 |
| One thousand | one | 有效的 |
| One thousand | Two | 有效的 |
| One thousand | three | 病人 |
| One thousand and one | Zero | 病人 |
| One thousand and one | one | 有效的 |
| One thousand and one | Two | 有效的 |
| One thousand and one | three | 病人 |
| Four thousand nine hundred and ninety-nine | Zero | 病人 |
| Four thousand nine hundred and ninety-nine | one | 有效的 |
| Four thousand nine hundred and ninety-nine | Two | 有效的 |
| Four thousand nine hundred and ninety-nine | three | 病人 |
| Five thousand | Zero | 病人 |
| Five thousand | one | 有效的 |
| Five thousand | Two | 有效的 |
| Five thousand | three | 病人 |
| Five thousand and one | Zero | 病人 |
| Five thousand and one | one | 病人 |
| Five thousand and one | Two | 病人 |
| Five thousand and one | three | 病人 |

## 结论

![Depositphotos_73405325_m-2015](img/e926b645e6720d73afe25892c09ac113.png)

Be sure to actually put all this knowledge into practice so that your retention rate is better. You will be able to see that this technique is actually really useful in helping you to come up with possible test cases.

在下一篇教程中，您将学习用于测试用例设计的*决策表*技术。到时候再聊。这里随时欢迎评论。

**引文**

*   李·科普兰。软件测试设计从业者指南

**巨大的资源**

*   [教授一系列 ISTQB 技术的网站](http://istqbexamcertification.com/what-is-a-static-test-technique/)
*   [测试概述和黑盒测试技术](http://agile.csc.ncsu.edu/SEMaterials/BlackBox.pdf)
*   [软件测试](http://users.ece.cmu.edu/~koopman/des_s99/sw_testing/)