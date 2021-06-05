# 为什么我讨厌大多数的WoW私人服务器

*Written by Francesco Borzi' aka Shin*

为什么WoW的私人服务器已经存在了这么多年，但仍然有这么多的bug？

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

别担心，这不是一般的关于暴雪的版权讲座。
我只是想解释一下为什么我讨厌大多数的[魔兽世界](https://en.wikipedia.org/wiki/World_of_Warcraft)私人服务器。

## 简介

我从14岁起就对WoW的模拟游戏着迷了。我记得我第一次加入这些 "特殊领域 "的时候，有很多bug，但你至少可以免费玩。你知道，当时我没有一分钱，所以我没有其他选择。

15岁时，我开始想知道私人服务器究竟是如何工作和存在的，特别是从技术角度来看。也许有人从[暴雪](https://en.wikipedia.org/wiki/Blizzard_Entertainment)偷了代码？我不知道--当时我是如此的年轻和缺乏经验 尽管如此，我还是开始瞎折腾，在我的一个老朋友（Fabio）的帮助下，我终于成功地在自己的电脑上安装了一个WoW服务器。

那时我甚至无法想象我将会得到多少满足感，以及我将会在这个神奇的世界里学到多少东西。

这听起来很奇怪，但是这个世界现在仍然让我着迷，作为一个成年人，我把整个[计算机科学的硕士学位论文](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation)都献给了这个主题。

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

但是仍然如此。**我讨厌大多数的私人服务器，我真的想解释一下原因**。

## 少一些技术术语

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

为了让你理解我的观点，我需要在关于WoW工作过程的一个小的技术性括号上多说几句，我将尝试用简单的话来说明。

### 原始魔兽世界是如何工作的

在软件层面上，有两个程序可以被认为是这个游戏的主要演员。

- **客户应用程序** - 这是实际的 "魔兽世界 "程序，由每个玩家安装在他们的计算机上，以便进入游戏。

- **服务器程序**：这是运行在服务器机器上的程序。

这个过程非常简单：所有的客户端（玩家）都连接到一个服务器，以便相互之间的互动。客户端知道服务器的地址，因为它存储在著名的 "**realmlist.wtf**"文件中（这就是为什么你必须修改这个文件，以便切换到另一个服务器）。

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### WoW私人服务器如何工作

在私人服务器上游戏时，原理是完全相同的。区别在于你使用的软件。

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENT**。每个人都可以使用原始的《魔兽世界》客户端。你可以通过购买或在线下载轻松获得它。这个程序正是你在官方服务器上玩的那个程序。显然，不同的私人服务器有不同的客户端版本，但它们总是参考原始客户端。你只需要对 "realmlist.wtf "文件做一个小改动，将零售服务器的地址替换成私人服务器的地址。这就是了。

**SERVER**。这是完全不同的。暴雪公司以外的人都无法接触到运行《魔兽世界》官方服务器的原始软件。所以这些应用程序与原来的完全不同。

### 逆向工程

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

每一个运行私人服务器的软件都是通过 "逆向工程 "技术创建的，简单地说，这意味着 "我试图写一个程序来模仿另一个程序的行为，而不看原始代码"。

现在的问题是：谁实现了这个软件，何时发生的？


#### 关于版权的题外话

谁创造了运行WoW私人服务器的软件应用程序（通常称为 "模拟器"）？他们又是如何做到的？

## 非官方的WoW服务器应用程序

谁创造了运行WoW私人服务器的软件应用程序（通常称为 "模拟器"）？他们又是如何做到的？



### 复杂性

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

你不需要成为专家就能明白，为《魔兽世界》这样大范围的MMORPG编写一个服务器应用程序肯定不是儿戏。

暴雪是一个拥有成千上万员工的大公司。编写一个 "模仿 "他们的服务器应用程序的程序对于一个人（或一小群程序员）来说肯定不是小事或可行的。

而且这不仅仅是一个复杂的问题。让我们想想非常琐碎但重复的任务，比如把每一个NPC加入到世界中，包括他们的每一个战利品都有自己的几率，等等。基本上是一个非常了不起的工作。更不用说所有非常复杂的任务，需要数小时的研究和测试，如法术机制，老板机制等。

你不需要成为专家就能明白，为《魔兽世界》这样大范围的MMORPG编写一个服务器应用程序肯定不是儿戏。

暴雪是一个拥有成千上万员工的大公司。编写一个 "模仿 "他们的服务器应用程序的程序对于一个人（或一小群程序员）来说肯定不是小事或可行的。

而且这不仅仅是一个复杂的问题。让我们想想非常琐碎但重复的任务，比如把每一个NPC加入到世界中，包括他们的每一个战利品都有自己的几率，等等。基本上是一个非常了不起的工作。更不用说所有非常复杂的任务，需要数小时的研究和测试，如法术机制，老板机制等。

简而言之，....，即使是世界上最好的程序员也不可能独自完成所有这些工作。

然而，有一些私人服务器，以及使其运行的软件。而一些私人服务器现在能够提供与原版相差无几的游戏质量（这里我主要指的是旧版的扩展）。

这怎么可能呢？

### MaNGOS和开放源码的发展模式

> 如果你有一个苹果，我有一个苹果，我们交换这些苹果，那么你和我仍将各拥有一个苹果。但如果你有一个想法，我有一个想法，我们交换这些想法，那么我们每个人都会有两个想法。(George Bernard Shaw)

简单点说：开源程序是一个代码公开的程序。

在私人服务器的背景下，开放源码起着基本的作用。

一些老玩家可能记得，曾经私人服务器上的游戏质量真的很差。几乎没有任何东西可以工作。
例如，如果你是一个隐身的流氓，你可以被任何写着`/target Yourname`的人盯上。猜猜我为我的第一个角色选择了哪个等级......

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

到目前为止，绝大多数的私人服务器都运行在基于MaNGOS/TrinityCore的应用程序上。

多年来，[不同的项目](http://mangosrumors.org/best-wow-emulator-2020/)诞生了，它们都是基于MaNGOS/TrinityCore的代码，主要根据支持的WoW版本而不同。
例如用于3.3.5的[AzerothCore](https://www.azerothcore.org/)，用于2.4.3的[OregonCore](https://github.com/OregonCore)，用于5.4.8的[SkyFire](https://www.projectskyfire.org/)，用于经典/TBC/WOTLK的[CMaNGOS](https://cmangos.net/)，以及许多其他项目... 所有这些都是基于MaNGOS和/或TrinityCore。

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### 回顾

因此，私人服务器能够达到这样的质量，完全是由于许多贡献者在过去几年（从2005年到今天）实现了越来越多的游戏功能。

今天，任何有经验的PC用户都可以轻松地安装一个WoW服务器，甚至不需要是一个程序员。

## 开源与私人服务器

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### 假设的情况

- 假设Alice和Bob各拥有一个私人服务器，我们假设他们使用的是同一版本的游戏。
  Alice和Bob都想向他们的玩家发布一个新的内容，由于Boss `A`,`B`,`C`和`D`有相当多的bug，所以到目前为止已经关闭。
  - Alice是一个非常好的开发者，她可以修复A和B两个Boss。
  - 鲍勃仍然是个初学者，只能修复Boss C`。

### 在一个理想的世界里

Alice和Bob一起工作，交换他们的修复方法。结果，他们两个人的服务器都有完美修复的Boss`A`，`B`和`C`。
此外，Alice和Bob将联合起来，以便在`D`上也进行工作。

结果，两个服务器上的玩家都非常高兴，因为他们玩的是完全修复的内容。

### 在现实世界中

Alice和Bob是竞争对手，所以他们互相开战。在Alice的服务器中，只有Boss`A`和`B`工作。而在Bob的服务器中，只有`C`可以工作。
一些玩家从Bob的服务器转移到Alice的服务器。鲍勃的服务器在一段时间后关闭了。一些Alice服务器的玩家停止了游戏，因为他们厌倦了总是只做`A`和`B`，因为`C`和`D`不起作用。

结果，两个服务器上的玩家都没有之前的情况下那么开心。爱丽丝通过玩家的捐赠比鲍勃赚了更多的钱。

### WoW模拟器开源许可

实际上，MaNGOS/TrinityCore代码（以及它们的衍生项目）是根据[GNU GPL许可证]（https://en.wikipedia.org/wiki/GNU_General_Public_License）发布的。

简单地说，这个许可证说的是：使用这些代码做任何你想做的事情，不需要支付任何费用，只要对原始代码的任何修改也是在同一个许可证下发布的。
基本上，这些项目的许可证要求使用它们的人向公众公布任何修改。

当然，大多数私人服务器把这个许可证当作**的厕纸。否则，不应该有私人服务器比其他服务器 "修得更好"。

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## 关于私人服务器的谎言

这里列出了许多WoW私人服务器的管理员不断对他们的玩家说的谎言。


###  "我们写了这个核心"

虚假的新闻。不管 "你 "做了多少改动，这都不重要。然而，你是从一个基于MaNGOS的项目开始的。

也许你做了一些改进，但大部分的代码仍然是MaNGOS/TrinityCore的。

也许你真的很厉害，多年来你已经重写了大部分的代码。但是，你还是从MaNGOS开始。如果没有它，在第一天，你甚至不会让登录功能工作。

###  "我们已经修复了X"

在绝大多数情况下，他们都没有真正修复什么。
他们只是下载了来自开源社区的修正，并将其应用于他们的核心。
但他们还是把所有的功劳都归于自己。

### "我们（真的）修复了X"

一些私人服务器真的自己修复了东西。他们通常有专门的开发团队，用玩家捐款的钱来支付。

他们中的大多数并不与开发社区分享这些修复。

好吧，社区（免费）给了你用来运行你的服务器的软件，要求你分享它们，但你仍然保持它的隐私。所以我还是恨你。

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## 私人服务器的 "理由"


###  "我保持隐私是为了使我的服务器成为一个特别的地方，比其他的更好"

好吧，冠军。试着想一想：如果所有的开发者都像你一样，你和你的私人服务器都不会存在。

为什么？因为MaNGOS（或TrinityCore、AzerothCore等......）都不会存在。
这些项目的存在要感谢那些与你不同的开发者，他们分享了他们的代码。

如果所有的开发者都保留他们的代码，我们就不会有像样的WoW模拟器，你就不能打开你的私人服务器，因为不会有任何软件可用。


### "如果我分享我的修正，竞争对手就会偷走它们"

没有什么可以 "偷 "的。他们不能 "偷 "那个代码，因为它不 "属于 "你。不，即使你真的写了它也不行。

开源理念很明确：你可以免费使用那段代码，只要对它的任何修改都必须公开。

哦，你不同意吗？好吧。那就不要使用任何开源代码，从头开始写你自己的WoW模拟器。

## 这对玩家有什么影响

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

我完全理解，这整个关于道德和许可证的故事对于普通的魔兽世界玩家来说是非常重要的。
玩家只想在一个稳定的、固定的服务器上游戏，他们并不太关心这个服务器是否与开源合作。

但是......请试着从另一个角度看一下。

开源项目（MaNGOS、TrinityCore、AzerothCore等......）的开发者基本上不怎么关心私人服务器做什么。
当然，作为一个开发者，看到一些随机的服务器管理员拿着你的工作的功劳，这让你很生气，但最终它并没有改变你的生活。
许多开放源码的开发者只是为了好玩和教育目的。

事实上，如果所有的私人服务器都与开源合作，玩家的生活就会完全改变！你知道吗？
你知道，在这种情况下，每个服务器都会为任何扩展提供更好的游戏体验。之前提到的Alice和Bob的例子也可以适用于这种情况。

然而，现实就是这样：世界上有许多私人服务器，他们每个人总是在做同样的事情，竞相做得更快更好。
如果他们相互合作，他们将避免做不必要的工作，并将有更多的时间和劳动力。因此，他们肯定能够取得更大的成就。

*注：私人服务器的质量（和竞争）不应该（只）是关于修复的，还应该是关于其他因素，如管理员的管理技能。社区的质量也起着根本性的作用，就像在暴雪服务器中发生的那样（从技术角度看，所有的服务器都是平等的）*。

如果一个私人服务器关闭了，而它的开发者没有分享他们的工作，这些工作将永远失去。

## 揭露谎言

### 官方作者名单

最有趣的是，所有基于MaNGOS的项目都是完全公开的，所以有可能准确地核实谁对它们做出了贡献。

因此，这些项目的所有贡献者名单都是绝对公开的，任何人都可以验证谁真正修复了什么。

比如说:

- MaNGOS贡献者的官方名单： https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- TrinityCore贡献者的官方名单： https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- 艾泽拉斯核心的官方贡献者名单： https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: 你可以在所有这些列表中找到本文的作者

### 官方提交列表

任何开源项目（一般托管在GitHub上）都有不同开发者实现的提交列表。对于每个提交，作者和日期都在那里。

要验证这些信息非常容易，只需打开任何模拟器的官方仓库。例如，在谷歌上搜索 "TrinityCore github "或 "AzerothCore github"，然后看一看。

你会看到谁做了真正的事情。你会看到所有的代码行，它们的作者，其他开发者的评论，等等。你会看到一切。不再有谎言!


## 作为一个玩家，我可以做什么？

我的建议是你玩/支持与开源合作的私人服务器，尽管他们使用的扩展和模拟器的类型。

或者，至少要避免那些以自己的名义兜售别人的作品，把原作者的功劳去掉的服务器。

**新的：**在2021年，新的项目[ChromieCraft](https://www.chromiecraft.com/about)已经启动，其特点是一个完全开源的服务器，具有渐进式眨眼的味道。

![ChromieCraft logo](https://avatars1.githubusercontent.com/u/68329413?s=400&u=084b35243e0aed1becd6a67fa88717eb8c1674d8&v=4)

### 了解更多关于自由软件的信息

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## 谢谢

Special thanks to *Laura Bartiromo*
