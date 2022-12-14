# 起床编码 43:饮食计划基础

> 原文：<https://simpleprogrammer.com/get-code-43-diet-plan-basics/>

这是我的第一集《起床编码》。最后一集是 Iris 的最后一集。录制一集完整的个人专辑比我想象的要难，但是我做到了，这就是我想要的。

在这一集里，我将谈论如何计算出你一天燃烧了多少卡路里，以及如何在此基础上制定饮食计划。

下面来看看吧。

[http://media.signalleaf.com/player/Get-Up-And-CODE/5310b18fb6971e0200000006/](http://media.signalleaf.com/player/Get-Up-And-CODE/5310b18fb6971e0200000006/)

[http://media.signalleaf.com/player/Get-Up-And-CODE/5310b18fb6971e0200000006/](http://media.signalleaf.com/player/Get-Up-And-CODE/5310b18fb6971e0200000006/)

下面是完整的文字记录

[显示](javascript:void(0))

约翰:大家好！欢迎回到起床和编码播客。我是约翰·桑梅兹，今天我独自一人在这里。这是有点悲伤的一天。我第一天独自录音。我想我们要看看这里会怎么样。你可能已经听说了 Iris 已经离开了这个节目，不是因为我们大吵了一架之类的原因。她只是很忙，她觉得是时候离开了。你可以听最后一集，我相信是第 42 集，如果你想从她身上找到她离开这部剧的确切原因。当然很难过。我当然很喜欢让她上节目，但是，嘿，节目必须继续，所以我要试着继续下去。

独角戏有点难，所以我们要看看它会如何发展。我打算今天谈谈我为我们这个展览准备了什么，我想在未来做些什么。然后，我还将谈论一个我认为非常重要的话题，那就是如何基本上建立一个饮食计划，或者如何达到你的目标，比如减掉脂肪或增加肌肉，如何基本上建立你的饮食计划。我认为这是一件非常重要的事情，许多人都在为此奋斗，这真的没有那么难。

在我们进入任何一个话题之前，让我花一点时间感谢我们的赞助商提供的这个节目。如果你去 signalleaf.com，你可以找到关于创建你自己的播客的信息。真的很好做。这至少很容易开始，SignalLeaf 让这变得非常容易，因为他们提供了播客托管服务，您可以使用它来托管您的播客。SignalLeaf 在 Get Up and Code 上托管我们的播客，他们也可以托管你的播客，所以如果你有兴趣创建自己的播客，别忘了去 signalleaf.com[看看。](http://www.signalleaf.com/)

好了，现在我们来谈谈这部剧会发生什么。坐在这里自言自语确实有点奇怪。我已经录制了许多 [Pluralsight 视频](https://simpleprogrammer.com/pluralsight)，我也录制了 YouTube 视频，但出于某种原因，在 solo 模式下播放播客似乎真的很难。我看着时间流逝，我想，“哇，我才讲了两分钟。”我们大部分的剧集都是 20 到 30 分钟。我怎么能说那么久呢？我想我们会看到这里会发生什么。会很有趣的。我肯定会有一些面试。

这个节目的很多形式可能会包括从现在开始的采访，至少直到我找到另一个合作主持人。我不是 100%确定我会选择哪条路。我在考虑找另一个主持人，但我必须找到合适的主持人，我认为这对这类节目非常重要。如果你有一些建议或想法，或者如果你认为你会成为一个很好的共同主持人，我绝对愿意倾听。你可以给我发一封电子邮件，地址是[show@getupandcode.com](mailto:show@getupandcode.com)或[john@simpleprogrammer.com](mailto:john@simpleprogrammer.com)，然后我们来谈谈我对起床和编码的看法。

嗯，就像我说的，我不想停止这个节目，因为我觉得它让很多人受益匪浅。我收到了很多你听这个节目的电子邮件和回复，说它对你有多大的帮助，无论是关于健身和饮食的激励，还是实现你想要实现的一些结果。我绝对觉得这个节目应该以某种形式继续下去。就像我说的，我认为我们需要进行更多的采访，因为我很难只谈论一个话题而不来回谈论 20 分钟，不管这个节目有多长。

如果你对这个节目的主题有什么想法，请告诉我。从现在开始，我真的想让这个节目的人尽可能地帮助你实现你的目标。至少当我们有一集不一定是采访，我只是在谈论一个话题，即使我有一个嘉宾，我们可以一起谈论一个话题，我想知道你的目标是什么。你在减肥吗？你想增肌吗？你想为某种运动进行训练吗？你心中有其他类型的目标吗？在 show@getupandcode.com 给我发一封电子邮件。让我知道你的目标是什么，你想听什么样的话题。

同样的，如果你有你认为适合这个节目采访的人，请告诉我，给我发电子邮件，告诉我一些关于他们的情况和他们的名字，并做介绍，我会尽力在这里实现。

说了这么多，让我们谈一点我今天想谈的话题，基本上是你如何建立饮食和一些基本的饮食指南，以了解如何减肥或增肌。当我试图以某种方式改变我的身体时，我会制定一个饮食计划。这是我在建立某种健身计划之前做的第一件事，因为饮食非常重要。弄清楚如何做到这一点可能会令人困惑。我已经通过反复试验弄明白了这一点。我这里有很多不同的文章和技巧可以帮助我做到这一点。

我尝试了很多不同的东西。我不会说我只有一个有效的成功公式。但是在我们真正开始创造饮食之前，我们需要知道一些基础知识。有几个基本的东西，我们需要基本计算或弄清楚。我们在节目中已经谈了一点，但我想更深入一点，谈谈我们如何把这些数字放在一起算出事情的答案。

首先，你需要知道你一天基本上燃烧了多少卡路里。这是一个关键的数字，知道你是否要制定任何一种饮食计划，因为你基本上会有两种饮食，实际上有三种。你的饮食中热量过剩，所以你的体重会增加。你的饮食热量不足，所以你要减肥。然后是维持型饮食，你要尽可能保持同样的体重。

计算你当前卡路里需求的方法是你必须查找你的基础代谢率。如果你只是搜索基础代谢率，我就在这里做。你应该找到很多计算器来做这件事。有一个基础代谢率计算器。你可以填上你的身高。例如，我要输入我的身高。我身高 6 英尺 3 英寸。我现在的体重大约是 230 磅，年龄 33 岁，男性。我要计算我的基础代谢率，然后它会告诉我，我的基础代谢率是 2227 卡路里。这是我的身体在不做任何其他事情的情况下燃烧所需的基本卡路里量。

我们仍然需要用哈里斯-本尼迪克特方程来计算活动水平。有些计算器已经可以帮你做这个了，但是你可以看看你是否搜索了哈里斯-本尼迪克特公式，如果你的计算器还没有搜索的话，有一些不同的层次。久坐很少或没有运动，这将是一个基础代谢率 x 1.2。即使你基本上不做任何运动，它也将是你基础代谢率的 1.2 倍或 120%。

如果你轻度活动，轻度锻炼，每周运动 1 到 3 天，那么需要 BMR x 1.375。适度运动，适度锻炼，每周运动 3 到 5 天，这可能是我想说的，可能比这高一天，这将是你的基础代谢率 x 1.55，所以超过你基础代谢率的 150%。如果你非常活跃，那就是每周 6 到 7 天的艰苦锻炼/运动，没有太多人属于这一类。我想我可能属于那一类，因为我每周举重 3 次，跑步 3 次，还做一些其他的事情。在保守的一边，看我总是站在保守的一边。我要说的是，我在中度活跃而非非常活跃之前。

如果你非常活跃，那么它是 1.725 倍基础代谢率。然后是额外的活动，非常艰苦的锻炼，运动和体力工作或 2 次训练，所以这就像你在为奥运会类型的交易训练。没有多少人会在这里。是 BMR x 1.9。

我建议你选择你认为自己保守的一面，这样你就可以准确地计算出来。就我而言，我的保守观点是 1.55。这就是适度活跃。

所以我要取那个 2227 x 1.55。这将告诉我，我每天应该燃烧的基本卡路里大约是 3451 卡路里。我把它四舍五入，再次，我尽可能保守地说，“好吧，我一天大概燃烧 3400 卡路里。”这是一个重要的数字，因为如果我想保持我现在的体重，我需要摄入 3400 卡路里。如果我想增加体重，显然我需要吃更多的东西。如果我想减肥，我需要少吃那么多卡路里。

我还可以增加活动来增加这一点。如果我每天走一个小时或者额外跑一圈，我就可以计算出做这些活动我会额外燃烧多少卡路里。

所以这真的很重要。知道你的基本利率是多少。我会说，这不会是 100%准确的，因为这里的事情是，记住这些数字是…我们有一个因子，从 1.2 一直到 1.9 倍的基础计算。这取决于你有多活跃。不会 100%准确。这就是为什么我说，如果你正在努力减肥，特别是因为你想低估你燃烧的卡路里，所以你不会因为试图建立一个不会让你成功的饮食而感到沮丧。

一旦我们有了这些，接下来我们需要做的就是弄清楚我们的目标是什么。我们在努力增加体重吗？我们是在减肥吗？还是努力保持原样？现在大多数人，我要大胆猜测，在这里都在努力减肥。我之所以会这样猜测，是因为健身行业销售的 90%的产品都是关于减肥的。90%的电视节目都是关于健身或减肥的。

如果你想减肥，你需要做的是计算出每天需要摄入多少卡路里来减肥。这就是你如何想出你的饮食计划。如果你雇佣私人教练或营养学家来为你制定饮食，他们基本上会和我在这里做的步骤一样。我没有得到任何许可来做这件事，但这是常识。健美运动员也做同样的事情。

在我们开始具体研究之前，让我们先来讨论一下一磅脂肪中大约有多少卡路里。如果你想减掉一磅脂肪，顺便说一句，你不仅要减掉一磅脂肪，还要减掉一些肌肉。只是减脂是不可能的。一磅脂肪的基本热量是 3500 卡路里。同样，这是一个估计。这并不完美。它不是绝对准确的。这大约是一磅脂肪所含的热量。

如果你想减肥，比方说你想每周减掉一磅，你需要每周摄入大约 3500 卡路里的热量。我们基本上可以说，3500 除以那周的 7 天，你一天的热量不足 500 卡路里。

让我们想象一下，我想一周瘦一磅。我知道我每天的烧损在 3400 左右。我知道我的赤字需要 500 英镑。我需要的是摄入不超过 2900 卡路里的热量。事实上，我想每天摄入接近 2900 卡路里的热量。现在，再一次，因为事情不是精确的，因为我们在这里使用一些平均值，一些估计值。如果我计算得出 29，我可能会把它降低，然后一直降到 2800 或 2700。

现在，很明显，如果你的体型小，卡路里少，你不会减少 200 卡路里，也许会更少，一个更小的百分比，但我想确保我没有搞砸。更有可能的是，你会摄入更多的卡路里，燃烧更少的热量。如果你在浪费时间，你会感到沮丧的。我可能估计我一天需要吃 2800 卡路里。

现在下一步，我知道我每天需要摄入多少卡路里。假设我想每周减掉 2 磅，那么我的赤字需要是 1000 磅，所以我每天需要吃大约 1800 卡路里。事实上，现在，这正是我正在做的。我刚刚结束了增肌阶段。我吃的热量过剩，举得很重，并试图获得一些肌肉。我的体重接近 240 磅，现在是 230 磅。我想减到 220。我正试图一周减掉 2 磅。

你可以看到我每天需要摄入 1000 卡路里的热量。如果你试图走得更远，你的赤字将会非常非常高。例如，我是一个相当大的家伙，230 磅，6 英尺 3 英寸。我打算一天只吃 1800 卡路里。相信我，卡路里并不多。那一点也不多。想象一下，如果我想每周减掉 3 磅，现在我要减掉 500 磅，所以我每天要吃 1300 卡路里，或者如果我想每周减掉 4 磅，现在我要减掉 500 磅，我每天要吃 800 卡路里？不会吧。这是不可能的。太疯狂了。

请记住，我比你大。我燃烧更多的卡路里，我很活跃，所以我有更多的卡路里来减肥。如果你的身材只有我的一半，那你的活动范围就更小了。像我这样体重约 230-240 磅的人，一周内不可能减掉超过 2-3 磅的体重。一周 3 磅是推动它。如果你认为你一周能减掉 5 磅，那你绝对是疯了。除非你非常非常超重，否则你不会那样做，这是非常非常不可能发生的。你需要有一个超过 4000 或者更多的维护等级才能有机会做到这一点。

现实地想一想，对于大多数人来说，这可能是因为他们没有我逐渐形成的纪律，特别是如果你有失败的记录，设定一周 1 磅的目标是完全可以接受的。你甚至可以在开始的时候把它设置得更小。我肯定会尽量把它做得足够大，因为有足够多的忽悠因素。请记住，我们在这里使用的估计是，如果你搞砸了一点点，它不会完全摆脱你，让你零损失。对我来说，每周 1 到 2 磅，像我说的，每周 2 磅，会让我摄入 1800 卡路里的热量，这不会让我快乐，但这是一个可行的饮食范围。

如果你想减肥，你应该已经计算过了，你应该知道你一天需要摄入多少卡路里。接下来要做的是把它分成我们称之为常量营养素的部分。我们的蛋白质、碳水化合物和脂肪的百分比是多少？我不打算就此进行大辩论和讨论，但我发现一些水平对我来说最有效，至少对保持肌肉和减少脂肪来说。除非你摄入足够的蛋白质和脂肪，否则你减掉脂肪的速度越快，你减掉肌肉的可能性就越大。

我倾向于发现，你可能需要对此进行一点点实验，但是大量的数据表明，对许多其他人来说这是正确的，即拥有一个良好的高脂肪、高蛋白、低碳水化合物的饮食将是最好的，特别是如果你试图一周减掉 2 磅以保持肌肉。除此之外，你还需要举重，这样你就能给你的身体一个保持肌肉的理由。

我通常用百分比来表示。我不想引用确切的百分比，因为我不想让你偏离我的百分比，但我通常会有大约 50%的蛋白质，也许 30%的脂肪和 20%的碳水化合物的饮食。我可能会稍微改变一下，把蛋白质含量降低一点，比如 40%蛋白质，40%脂肪和 20%碳水化合物。我努力保持高脂肪和高蛋白质，我会告诉你为什么我要这么做。

这里有两个基本原因。首先让我们看看，我们没有多少卡路里可以消耗。我一天 1800 卡路里。为了获得保持肌肉所需的一切，我必须非常保守地消费卡路里。我想在蛋白质上花费大量的卡路里，因为我知道我的身体需要蛋白质来维持我的肌肉，特别是我有相当高的肌肉，我的体脂百分比很低，所以我的身体需要大量的氨基酸和蛋白质来重建我正在分解的肌肉并保持它。

第二部分是脂肪部分。脂肪其实对你没那么坏。卡路里更高，所以你可能会吃得更少。你会吃更多的高密度食物，但是吃脂肪，尤其是对男性来说，会增加睾丸激素的产生。相反，如果你没有摄入足够的脂肪，你的睾丸激素就会降低。我们想要高睾丸激素，因为这将帮助你燃烧脂肪。这会帮助你变得更瘦。睾丸激素对男性和女性都有好处。我们要确保我们的脂肪含量相当高。当你举重物时，这对你的关节也很有帮助。你热量不足，你不想受伤，所以保持高脂肪水平肯定是好的。

这就是我的想法。碳水化合物对我们并没有太大帮助，但我确实会保留一些。如果你试图降低碳水化合物的摄入量，你会变得非常暴躁。你会变得非常情绪化。坚持节食将会非常困难。我发现通过保持这个比例，只要我摄入足够多的脂肪，我总体感觉会更好。我不只是饿了。这似乎是关键的事情，所以我可以保持那些碳水化合物低一点。

接下来你需要计算的是你的百分比是多少。有一些饮食，你可以做相同的部分，如 33%的蛋白质，33%的脂肪，33%的碳水化合物。那可能没问题。我只是告诉你我做什么。你应该考虑一下这个问题，弄清楚你想要的比率是多少。

一旦你明白了这一点，你就需要弄清楚你要用什么食物来弥补这些。我尽量吃简单的食物。现在，我实际上仍然在做瘦收益，间歇性禁食的类型。我一天只吃两三顿饭。当我离开时，其中一餐是蛋白奶昔，但我基本上保持事情非常简单，所以对我来说创建一个饮食并不困难。

我以前节食过，我一天吃 6 到 7 顿饭，这很难，尤其是如果你想吃全天然的食物，因为你必须烹饪这些食物，你的整个生活就变成了节食。这不是什么真正实用的东西，除非你打算以此为职业。你要像我以前一样为比赛或拍照而训练。保持动力真的很难。

以下是我的推荐。这是我现在正在做的事情，这很简单，只吃简单的食物。因为鸡蛋富含蛋白质和脂肪。你可以吃瘦肉，比如鸡肉或鱼肉，然后吃菠菜或西兰花，它们会补充一点碳水化合物。它们会是你吃的很好的碳水化合物，因为它们也富含纤维。它们不会有很多卡路里，所以你可以吃这些东西来填饱肚子。这将会给你更多的空间来吃东西，这将会帮助你不感到饥饿。

我也尽量让事情尽可能快。我可以很容易地用微波炉煮鸡蛋。我可以在上面放一些切达奶酪，以增加我需要的适量脂肪，另外鸡蛋是很好的蛋白质来源。午餐时，我可以做一些事情，比如用一些清淡的罐头汤，放一些菠菜或其他蔬菜，让它更蓬松一些，或者放一些农家奶酪在里面。是的，我知道罐头食品对你来说不是最健康的，它们含有高钠，但是，嘿，这只是为了方便。

我也做冷冻鸡胸肉，像红烧鸡胸肉，我能从山姆会员店或 BJ 的一些不同的杂货店找到，在美国这里也有，还有火鸡肉丸，也是高蛋白和脂肪结合非常低碳水化合物。

我挑选那些主食，也许你有一些你喜欢的主食。我可能会选择 5 或 6 种主食，其中一些是蔬菜，一些是蛋白质来源，一些是脂肪或脂肪/蛋白质来源，然后尽可能将它们分成几份。许多食物可以让你很容易地将它们分成不同的部分，以调整你食物中的卡路里含量，不管是脂肪、碳水化合物还是蛋白质，都会非常有用。

找出一些你可以用来烹饪的基本食物和基本膳食，然后制定几份菜单，A 日和 B 日，或者可能是 A 日、B 日、c 日。我只有 A 日和 B 日。我可以不要这些品种。你投入的种类越多，难度就越大，但对你来说可能会更有趣一点。你必须平衡你喜欢多样化还是轻松。我倾向于选择轻松的一面，因为我不喜欢花很多时间做饭、准备食物和思考这些。这取决于你自己。

我说过的另一件事是，我在准备过程中使用了很多冷冻的东西。不是新鲜食材。有些人非常热衷于此。我没有发现冷冻和新鲜对我的体质有很大的影响，所以我倾向于冷冻。尤其是蔬菜，冷冻绝对没有错。事实上，在很多情况下，它们比新鲜的更好，因为它们实际上是在采摘时速冻的，所以它们实际上是在成熟时采摘的，而不是像你在许多杂货店里看到的那样提前运出。

所以我们在这里有基本的东西。这里要讲的内容太多了。在这里简单回顾一下，你要做的第一件事是弄清楚你的基础代谢率是多少。用计算器，然后用乘数算出它实际上是什么。一旦你有了基础代谢率，你就要弄清楚你的赤字或盈余是多少。我们一会儿会谈到过剩，但让我们假设你正在减肥或试图减肥。弄清楚你的赤字是什么。就像我说的，1，2 磅，如果你试图做太多，这对你来说真的很疯狂。如果你想帮忙的话，你可以增加一些有氧运动，但是，还是那句话，不要太疯狂。你会戒酒的。你要在一个晚上吃掉一整袋奥利奥和两盒冰淇淋，那就相当于 10，000 卡路里。在这里尽量讲道理。

然后你要弄清楚你的宏观比率是多少，然后你要像那样计划你的食物。就像我说的，吃饭的次数不再那么重要了，除非你真的把它调整到分钟的细节，如果你在健美比赛或什么的。如果你是那种你已经知道的普通人每天吃 2 到 3 顿饭来计算你的卡路里的人，试着确保你达到了卡路里和宏量营养素的目标。

我会给你一个小提示。例如，我去迈阿密参加代码营，我知道我不能坚持我原来的计划，我要出去吃饭或做些什么，所以我在那几天不吃早餐和午餐，把 1800 卡路里的热量留在晚餐。你的身体真的不知道有多大区别，所以这是其中之一——你不会一直这样做，但你可以在旅行的某一天这样做，或者你知道你不能基本上坚持你的计划。

那就是减脂。同样的事情也适用于增肌，除了你会处于卡路里过剩的状态。现在你想要一个干净的多余卡路里。你不想想吃多少卡路里就吃多少。你要确保这些卡路里是高质量的，是真正能帮助你锻炼肌肉的东西。

再说一次，增加肌肉很像减少脂肪。你不可能一周增加 5 磅肌肉。事实上，它会变得更小。一般来说，增肌比减脂更难，而且你会因此增加脂肪。假设你想增加大约一磅的体重。请记住，可能是 70%的肌肉和 30%的脂肪或其他什么。假设你需要 3500 的热量盈余。同样，我们知道这意味着我们每天需要摄入 500 卡路里的多余热量。你可以在这里算一下，也许对我来说，如果我的基数是 3400 卡路里，那么我需要达到 3800 卡路里。我在这里估计的有点高，我想说，好吧，让我们确保我摄入了 4000 卡路里，以确保我达到了摄入足够卡路里的目标，如果我想增重的话。

现在，请注意，我并没有把卡路里增加到 5 或 6000 卡路里。如果我这样做，我会增加肌肉，是的，但我会增加大量的脂肪。我们想慢慢增加质量。我们要小心，特别是如果你已经失去了一些重量，现在你正试图增加一些肌肉。你要慢慢拨号。看看有多少卡路里，最少的卡路里是多少，你能增加多慢，这样你增加的大部分是肌肉而不是脂肪。很容易让事情顺其自然，让它们溜走，然后吃一堆卡路里，然后突然你就变胖了。

这是基本相同的策略，除了相反的一面，如果你想增肌的话。显然，你会在健身房里举重，因为你需要它来增加肌肉。当你计划你的膳食时，除了你只是增加了份量之外，这是完全一样的。这是你应该记住的一件事。你的增肌食谱应该和减脂食谱一样，只不过分量要大一些。你应该吃同样的食物，同样的健康食物。你不应该吃一堆蛋糕、披萨和所有这些垃圾食品，因为你会摄入多余的卡路里，相反，你应该吃和节食时一样的干净食物。

就是这样。这是最基本的。希望你觉得这很有用。如果你有任何问题，不要害怕问。请发电子邮件到 show@getupandcode.com 给我，或者在推特、博客或脸书上发送。让我知道你对这个格式的想法。就像我说的，我需要更多的想法来让这集继续下去，并为客人和类似的事情。

祝你在这里的目标好运。我只想说这是一个很多人放弃的点。我们在二月底来到这里，许多人开始了他们的新年，“是的，我要去举重。我要减肥了。”熬过了 1 月和 2 月，大多数健身房会员或健身房指望人们在这一点上逐渐消失。没关系。这是会发生的，但事情是这样的，这是你成功的方法，你要重新回到马背上。你会继续前进，不会让一个小小的挫折阻止你。如果你搞砸了，如果你已经放弃了，现在是时候重新启动，重新设置。使用我在这一集给你的这类信息来弄清楚——一旦你明白了它是如何工作的，减肥和增重是如何工作的，那么你就会更有动力，因为你知道你会看到结果。

如果你使用这些数字，我在这里说的这些数字，你正在遵循饮食，并据此建立饮食，你会看到它的结果。我刚开始减肥。很明显，你必须调整你的数据，因为这会改变你的燃烧量。如果你长胖了也是一样。如果你这样做，科学、数学、物理学会告诉你，如果你有盈余或赤字，你会减肥或增重。你也要给它足够的时间。你要给它至少几个星期，因为如果你踩在秤上，不同的日子会有微小的波动。

希望这对你有用，下周我会再和你谈谈。保重。