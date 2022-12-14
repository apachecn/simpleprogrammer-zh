# 简化测试

> 原文：<https://simpleprogrammer.com/simplified-testing/>

我一直在努力应对瀑布式测试方法和敏捷测试方法之间的冲突。对于敏捷中的“端到端”和“系统测试”是什么样子，确实没有一个很好的可靠的说法。是时候简化测试了。

为了保持简单，让我们从最终目标开始分解:在迭代结束时产生可发布的代码。

这来自于敏捷原则:

*频繁交付工作软件，从 a*

**几个星期到几个月，用**

对较短时间尺度的偏好。

为了交付可工作的软件，该软件在那时必须是可用的或完整的。几乎每一个敏捷过程都包括在进入下一个之前完成一个用户故事(至少是一个迭代中的所有用户故事)。)

可发货的软件是已经过完全测试的软件。如果你坚持“系统测试”的谬论，那么在一次迭代中达到这一点是不可能的“系统”或“端到端测试”到底是什么？我从未见过一个真正的系统级缺陷不存在于功能级。当你只改变了一小部分功能时，测试整个系统有什么价值？当您在这种高水平的测试中发现缺陷时，您最终不得不将它们归类到根本原因。

如果我们把它切掉呢？如果我们说系统中所有期望的功能都由与代码一起产生的自动化测试来表示呢？

如果我们做两件非常简单的事情会怎么样:

1.  对于每个用户故事，我们编写自动化测试，定义我们对系统的期望；当这些都过去了，故事就结束了。看看 Kent Beck 的书[测试驱动开发](http://www.amazon.com/gp/product/0321146530/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=0321146530&linkCode=as2&tag=makithecompsi-20)。
2.  每次我们完成一个故事，我们运行所有以前的自动化测试，以确保没有任何东西被破坏。一本关于测试的好的通用书籍是[测试计算机软件](http://www.amazon.com/gp/product/B000S1LVEU/ref=as_li_ss_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B000S1LVEU&linkCode=as2&tag=makithecompsi-20)。

如果我们做了这两件事，并且我们确定系统的用户(或者代表用户的人)已经同意自动化测试充分地覆盖了他们想要故事完成的内容，还有必要做其他的事情吗？或者这种非常复杂的测试方法真的就那么简单？