# 关于代码签名的所有内容:它是什么，它是如何工作的，以及为什么应该这样做

> 原文：<https://simpleprogrammer.com/code-signing-primer/>

![code signing](img/f743f3fc0a786c141a7c40930bc3c41d.png)

In the summer of 2021, Microsoft [issued a security advisory](https://www.gosecure.net/blog/2021/08/13/the-neverending-story-the-printnightmare-debacle/) letting users know of a critical vulnerability in the Windows Print Spooler service. The flaw made it possible for attackers to run arbitrary code on just about any affected Windows machine if they could trick a user into installing a compromised printer driver. From there, they could gain near-total control of the machine and access to anything connected to it.

但是如果你阅读了公告的细节，你会注意到一条重要的信息:该漏洞围绕着用户安装未签名打印机驱动程序的能力。签名驱动程序不是问题——因为攻击者几乎不可能修改它们来包含他们发动攻击所需的恶意位。

在这种区别中，有一个给全世界软件开发人员的教训:代码签名是重要的，是我们在发布面向公众的软件时都需要做的事情。也就是说，似乎有很多开发人员不关心代码签名或者不理解它的重要性。

但是，不要搞错:代码签名对于保护您的客户和保护您自己作为软件开发人员一样重要。例如，想象一下，一个黑客或其他不良分子决定将恶意代码注入到您的一个软件中。当代码造成了它设计的破坏时，你认为你的客户会责怪谁呢？

如果你猜对了是你，得两分。

代码签名并不那么难做。为了帮助您理解它是如何工作的，这里有一个完整的代码签名指南。我们将介绍它是什么，它是如何工作的，以及为什么您应该这样做。我们开始吧，好吗？

## 什么是代码签名？

首先，让我们看看什么是代码签名——它非常简单，真的。代码签名是颁发可信数字证书的过程，该证书证明您是谁，并保证一个软件只包含您编写的并且您可以担保的代码。

换句话说，这有点像你买了一部有签名的电影纪念品后得到的真品证书。除了在代码签名的情况下，你不只是保证真实性，你保证普罗维登斯和安全。

它基于网络浏览器用来打开到远程服务器的 SSL 加密连接的同一种逻辑。使用可信的认证机构使得不了解您个人的计算机和用户有可能合理地确定他们将要执行的软件没有被以任何方式篡改。

如果在过去的二十年里，您曾经从互联网上下载过一个程序，并试图随时运行它，那么您可能已经看到了代码签名的实际应用。现代操作系统会检查下载软件的有效签名，并使用该信息提醒您谁在请求更改您的计算机。

未签名的软件将生成一个彩色的可怕的警告，让你知道一个未知的实体希望对你的电脑进行更改。但是签名的软件会导致一个看起来良性的警告，列出软件开发者的名字并请求允许继续。

在《网络安全、隐私和商业 一书中，有一个精彩的章节讨论了代码签名——以及许多其他开发者应该知道的网络安全话题。这也是一本很棒的手册，我相信每个开发人员都应该把它放在书架上，作为无数在线安全主题的参考。

## 代码签名是如何工作的？

对代码进行签名的过程与您为网站获取 SSL 证书的方式并没有什么不同。它涉及到使用一个公共和私有加密密钥对，让一个[可信认证机构](https://www.sslshopper.com/cheap-code-signing-certificates.html)向您颁发一个有效的代码签名证书，以便在您发布软件时使用。

要获得代码签名证书，您必须向证书颁发机构证明您的身份，以便他们知道您就是您所说的那个人。但是如何做到这一点取决于你想获得的证书的种类。有两种主要类型:

*   **组织验证代码签名证书—**通常称为标准代码签名证书，是两种证书中较容易获得的一种。要获得证书，您必须向证书颁发机构表明您的身份，并通过简单的验证过程。获得一个证书并不比获得一个标准的 SSL 证书困难多少。
*   **扩展验证代码签名证书—**扩展验证(EV)代码签名证书更难获得。要获得一个，你必须通过一个认证机构漫长的审查过程。有什么问题吗？EV 证书只颁发给组织，不颁发给个人。它们是为高容量软件发行商设计的，带有存储在物理硬件密钥上的私有加密密钥，以防止误用。

标准和 EV 代码签名证书之间的主要区别是它们允许您的软件做什么。标准证书使得操作系统可以将软件签名时的散列值与运行时的散列值进行比较。它也把你，开发者，作为一个特定软件的幕后人。

另一方面，电动汽车证书带来了一些额外的好处。首先，您可以使用 EV 证书来签署 Microsoft Windows 驱动程序，而不能使用标准证书来签署。还记得介绍中提到的安全建议吗？正是 EV 证书签名的驱动程序免受该漏洞的影响。

EV 证书的另一个主要附加好处与 [SmartScreen](https://support.microsoft.com/en-us/microsoft-edge/what-is-smartscreen-and-how-can-it-help-protect-me-1c9a874a-6826-be5e-45b1-67fa445a74c8) 有关，这是微软的内置网站和下载检查系统。当您使用 EV 证书签署您的软件时，SmartScreen 将立即信任您的软件。这大大提高了 Windows 用户下载你的软件而不会在屏幕上弹出任何可怕的安全警告的几率。

## 为什么您应该签署您的代码

![](img/8eca5813569dad2a60fd043587f840db.png)

There are a variety of reasons that you should be signing your code. Some of them are very obvious. Others are less so. Let’s begin with the most obvious reason of all: You want people to run your software, and if your software isn’t signed, there’s a very good chance that users will struggle to run it.

就微软而言，它对于阻止用户下载和运行未签名的代码是非常认真的。他们的操作系统保护系统会向用户呈现一系列[路障和警告](https://www.theregister.com/2020/06/05/windows_10_microsoft_defender_smartscreen/)来阻止他们这么做。他们没有明确说明如何绕过它们。

另一个主要的消费者操作系统 MacOS 也做着几乎完全相同的事情。包含本地处理器[的新款苹果电脑根本不会运行为其编译的未签名软件](https://mjtsai.com/blog/2020/08/19/apple-silicon-macs-to-require-signed-code/)。所以如果你想让人们能够使用你的软件，你需要养成签名的习惯。

签署你的软件的另一个原因是，它将提高企业的采用率。今天的[网络安全专家](https://studyonline.unsw.edu.au/blog/career-in-cyber-security-australia)既没有时间也没有兴趣审查未签名的软件，除非这是唯一的选择。大多数主要的公司网络限制下载或安装未签名的软件——理由很充分。当一段被修改的代码就可能导致数百万美元的数据泄露时，就没有出错的余地了。

最后但同样重要的是，你应该签署你的代码，以保护你的声誉。如果你是一个独立的开发者，以你开发的软件为生，你不能让别人把它作为恶意软件攻击的途径。如果发生这种情况，受影响的用户将不会区分你和对攻击负责的人。你遭受的名誉损害可能是不可挽回的。

## 对于开发人员来说，代码签名是值得的

这里的底线是开发者——包括你——应该创建一个过程来签署他们发布的所有代码。这样做将有助于提高你的声誉，并增加最终用户能够运行你的作品的几率。最终，这就是开发人员所要做的，不是吗？

但是请注意，签署你的代码意味着你在你的作品上盖了你个人的印章。因此，你也应该尽力编写从一开始就是安全的代码。毕竟，如果您给攻击者留下了使用您已经编写的代码的机会，他们就不需要修改您的代码。

如果你是软件开发的新手——即使你经历过几次——我建议你读一下 [*软件安全评估的艺术:识别和预防软件漏洞*](https://www.amazon.com/dp/0321444426/wwwerobillarc-20) 如果你能找到一个价格合理的副本。它会教你所有你需要知道的关于安全编码的知识，所以你可以完全放心地签署你的软件，它不会回来困扰你。

这就是全部了。希望您已经了解了为什么代码签名如此重要，以及为什么您应该这样做。现在去做吧！