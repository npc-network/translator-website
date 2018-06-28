---
title: Notes on Blockchain Governance
tags:
---

原文地址：https://vitalik.ca/general/2017/12/17/voting.html

_In which I argue that “tightly coupled” on-chain voting is overrated, the status quo of “informal governance” as practiced by Bitcoin, Bitcoin Cash, Ethereum, Zcash and similar systems is much less bad than commonly thought, that people who think that the purpose of blockchains is to completely expunge soft mushy human intuitions and feelings in favor of completely algorithmic governance (emphasis on “completely”) are absolutely crazy, and loosely coupled voting as done by Carbonvotes and similar systems is underrated, as well as describe what framework should be used when thinking about blockchain governance in the first place.  
  
在我认为“紧密耦合”的在线投票被高估的情况下，比特币，比特币现金，以太坊，Zcash和类似系统实行的“非正式治理”的现状没有通常认为的那么糟糕，那些认为区块链的目的是为了彻底清除模糊的人类直觉和感受以支持完全算法治理（强调“完全”）的人们是彻底疯狂的，Carbonvotes和类似系统所做的松散耦合投票被低估了，描述在考虑区块链治理时首先应该使用什么框架的重要性也被低估了。
  
See also: [https://medium.com/@Vlad_Zamfir/against-on-chain-governance-a4ceacd040ca](https://medium.com/@Vlad_Zamfir/against-on-chain-governance-a4ceacd040ca)_

One of the more interesting recent trends in blockchain governance is the resurgence of on-chain coin-holder voting as a multi-purpose decision mechanism. Votes by coin holders are sometimes used in order to decide who operates the super-nodes that run a network (eg. DPOS in EOS, NEO, Lisk and other systems), sometimes to vote on protocol paramters (eg. the Ethereum gas limit) and sometimes to vote on and directly implement protocol upgrades wholesale (eg. [Tezos](http://tezos.com/)). In all of these cases, the votes are automatic - the protocol itself contains all of the logic needed to change the validator set or to update its own rules, and does this automatically in response to the result of votes.

区块链治理最近的一个更有趣的趋势是作为多用途决策机制的在线硬币持有人投票机制的复苏。 硬币持有人的投票有时用于决定谁来运营超级节点从而运行整个网络（例如，EOS，NEO，Lisk和其他系统下的DPOS），有时对协议参数进行投票（例如以太坊gas限制） 有时可以对协议参数进行投票（例如以太坊gas限制），有时可以进行投票并直接实施协议升级(eg. [Tezos](http://tezos.com/))。在所有这些情况下，投票都是自动的——协议本身包含了更改验证器集或更新自己的规则所需的所有逻辑，并自动响应投票结果。

Explicit on-chain governance is typically touted as having several major advantages. First, unlike the highly conservative philosophy espoused by Bitcoin, it can evolve rapidly and accept needed technical improvements. Second, by creating an _explicit_ decentralized framework, it avoids the perceived pitfalls of _informal_ governance, which is viewed to either be too unstable and prone to chain splits, or prone to becoming too de-facto centralized - the latter being the same argument made in the famous 1972 essay “[Tyranny of Structurelessness](http://www.jofreeman.com/joreen/tyranny.htm)”.

明确的链上治理通常被吹捧为具有几个主要优势。 首先，与比特币所倡导的高度保守的哲学不同，它可以迅速发展并接受所需的技术改进。 其次，通过创建一个_explicit_分散的框架，它可以避免非正式治理的缺陷，这种缺陷被认为既不稳定又容易出现连锁分裂，或者容易变得过于事实上的中心化——后者与1972年著名论文“Tyranny of Structurelessness”中的论点相同。http://www.jofreeman.com/joreen/tyranny.htm

Quoting [Tezos documentation](https://www.tezos.com/governance):

> While all blockchains offer financial incentives for maintaining consensus on their ledgers, no blockchain has a robust on-chain mechanism that seamlessly amends the rules governing its protocol and rewards protocol development. As a result, first-generation blockchains empower de facto, centralized core development teams or miners to formulate design choices.

> 尽管所有区块链都提供财务激励来维护对其分布式账本的一致性，但没有哪个区块链具备这么好鲁棒性的链上机制，能够实现无缝修改协议的管理规则和奖励协议开发规则。因此，第一代区块链完成的是从事实上的中心化的核心开发团队或矿工，到定制设计的选择多样化转变。

[And](https://twitter.com/tez0s/status/884528964194238464):

> Yes, but why would you want to make \[a minority chain split\] easier? Splits destroy network effects.

> 是的，但为什么人们想让[少数链的拆分]变得更容易？ 拆分会摧毁网络效应。

On-chain governance used to select validators also has the benefit that it allows for networks that impose high computational performance requirements on validators without introducing economic centralization risks and other traps of the kind that appear in public blockchains (eg. [the validator’s dilemma](https://eprint.iacr.org/2015/702.pdf)).

用于选择验证器的链上管理还具有这样的好处，即它允许网络对验证器施加高计算性能要求，而不会引入经济中心化风险和公链中出现的其他类型陷阱（例如[验证器的难题]（https://eprint.iacr.org/2015/702.pdf)）

So far, all in all, on-chain governance seems like a very good bargain…. so what’s wrong with it?

到目前为止，总体而言，链上治理似乎是一个非常好的途径......所以它有什么问题呢？

### What is Blockchain Governance?

### 什么是区块链治理

To start off, we need to describe more clearly what the process of “blockchain governance” _is_. Generally speaking, there are two informal models of governance, that I will call the “decision function” view of governance and the “coordination” view of governance. The decision function view treats governance as a function `f(x1, x2 ... xn) -> y`, where the inputs are the wishes of various legitimate stakeholders (senators, the president, property owners, shareholders, voters, etc) and the output is the decision.

首先，我们需要更清楚地描述“区块链治理”的过程。 一般来说，有两种非正式的治理模式，我将称之为治理的“决策职能”治理观点和“协调”治理观点。 决策智能观点将治理视为一个函数‘f（x1，x2 ... xn） - > y’，其中输入是各种合法利益相关者（参议员，总统，财产所有者，股东，选民等）的意愿， 而输出的是决定。

![](http://vitalik.ca/files/decisionfunction.png)

  

The decision function view is often useful as an approximation, but it clearly frays very easily around the edges: people often can and do break the law and get away with it, sometimes rules are ambiguous, and sometimes revolutions happen - and all three of these possibilities are, at least sometimes, _a good thing_. And often even behavior inside the system is shaped by incentives created by _the possibility_ of acting outside the system, and this once again is at least sometimes a good thing.

决策函数视图通常可以用作近似值，但它很容易出现在灰色地带：人们经常能够并且确实违反法律并逃避法律，有时候规则是模棱两可的，有时会发生革命 - 所有这三个 可能性，至少有时是一件好事。 而且，系统内部的行为往往受到所在系统外进行行动的可能性所激发的激励机制的影响，而这至少有时是一件好事。

The coordination model of governance, in contrast, sees governance as something that exists in layers. The bottom layer is, in the real world, the laws of physics themselves (as a geopolitical realist would say, guns and bombs), and in the blockchain space we can abstract a bit further and say that it is each individual’s ability to run whatever software they want in their capacity as a user, miner, stakeholder, validator or whatever other kind of agent a blockchain protocol allows them to be. The bottom layer is always the ultimate deciding layer; if, for example, all Bitcoin users wake up one day and decides to edit their clients’ source code and replace the entire code with an Ethereum client that listens to balances of a particular ERC20 token contract, then that means that that ERC20 token _is_ bitcoin. The bottom layer’s ultimate governing power cannot be stopped, but the actions that people take on this layer can be _influenced_ by the layers above it.

而协调治理模型，相比之下，将治理视作存在于多层面的东西。最底层是，在现实世界中，自然界的法则（一个地缘政治现实主义者会说：枪炮和炸弹）。在区块链的空间中我们可以抽象一点地讲：对每个独立个体来说，在他们的能力范围之内，作为用户，矿工，权益拥有者，验证者等等，按自由意志运行什么样的软件是他们的能力。而最底层总是最终的决策层；比如，如果所有的比特币用户在某天醒来并决定将他们的源代码改为符合ERC20 token交易的以太坊客户端，那么这就意味着那个ERC20 token就是比特币。最底层的最终决策力量是不可阻挡的，但是人们在这一层面上的行为可以被更上层所影响。

The second (and crucially important) layer is coordination institutions. The purpose of a coordination institution is to create focal points around how and when individuals should act in order to better coordinate behavior. There are many situations, both in blockchain governance and in real life, where if you act in a certain way alone, you are likely to get nowhere (or worse), but if everyone acts together a desired result can be achieved.

次底层（至关重要）是负责协调的机构。协调机构的目的是围绕个体怎样行动才能创造一个更好的协调行为创造一个范本。在区块链治理和现实世界中都有许多这样的情况：如果只是一个人以一种特定的行为行事什么都不会发生（或者变得更糟），但是如果每个人都一起行动，就能取得理想的结果。

![](http://vitalik.ca/files/coordinationgame.png)  
An abstract coordination game. You benefit heavily from making the same move as everyone else.

一个抽象的协调游戏，你能够通过像其他人一样行动而受益

In these cases, it’s in your interest to go if everyone else is going, and stop if everyone else is stopping. You can think of coordination institutions as putting up green or red flags in the air saying “go” or “stop”, _with an established culture_ that everyone watches these flags and (usually) does what they say. Why do people have the incentive to follow these flags? Because _everyone else_ is already following these flags, and you have the incentive to do the same thing as what everyone else is doing.

在这些案例中，和大家的行动一致是你的利益驱使。你可以想象，协调机构举起绿色或者红色的旗帜代表“走”或“停”，根据已有的规则大家看到这些旗帜通常会做出机构所期望的行为。为什么人们有动机去跟随着这些旗帜的引导呢？因为其他人都这么做了，而你有动机像大家一样行动。

![](http://vitalik.ca/files/byzantinegeneral.jpg)  
A Byzantine general rallying his troops forward. The purpose of this isn't just to make the soldiers feel brave and excited, but also to reassure them that _everyone else_ feels brave and excited and will charge forward as well, so an individual soldier is not just committing suicide by charging forward alone.

一个拜占庭将军集结他的部队前进。这一行为的目的不仅仅是让士兵受到鼓舞并变得勇敢，同样是向他们显示每个人都是一样的勇敢和振奋，并且会向前冲锋，所以不是士兵单个个体向前冲锋而导致自杀行为。

> **Strong claim**: this concept of coordination flags encompasses _all_ that we mean by "governance"; in scenarios where coordination games (or more generally, multi-equilibrium games) do not exist, the concept of governance is meaningless.

强有力的宣言：这个协调指令的概念囊括了“治理”的所有内容，在一个协调博弈（或者更广义的来说，多平衡博弈）不存在的场景下，治理的概念是毫无意义的。

In the real world, military orders from a general function as a flag, and in the blockchain world, the simplest example of such a flag is the mechanism that tells people whether or not a hard fork “is happening”. Coordination institutions can be very formal, or they can be informal, and often give suggestions that are ambiguous. Flags would ideally always be either red or green, but sometimes a flag might be yellow, or even holographic, appearing green to some participants and yellow or red to others. Sometimes that are also multiple flags that conflict with each other.

在现实世界中，来自一个将军的军事命令是一面旗帜，在区块链世界中，这类指令最简单的例子是告诉人们是否进行硬分叉的机制。协调机构可以非常正式，也可以非正式，他们经常给出模糊的建议。而理想的指令，最好要么是红的要么是绿的，但有时候是也有黄的，甚至全息的，这意味着对有些人来说它是绿的，对有些人却是黄的或者红的。有时还有多条指令相互矛盾。

The key questions of governance thus become:

治理的核心问题因此变成：

*   What should layer 1 be? That is, what features should be set up in the initial protocol itself, and how does this influence the ability to make formulaic (ie. decision-function-like) protocol changes, as well as the level of power of different kinds of agents to act in different ways?
*   What should layer 2 be? That is, what coordination institutions should people be encouraged to care about?

*   最底层应该是怎样的？意思是说，我们应该为最底层设计怎样的特点，以及这样的特点应该怎样去影响我们公式化地改变协议的能力，以及不同种类不同级别的代理如何以不同的方式行动？

*   第二层又该是怎样的？这是说，应该鼓励人们关心什么样的协调机构？

### The Role of Coin Voting

### 持币投票扮演的角色

Ethereum also has a history with coin voting, including:

以太坊同样有一个代币投票的历史，包括：

*   **DAO proposal votes**: [https://daostats.github.io/proposals.html](https://daostats.github.io/proposals.html)
*   **DAO 提案投票 ：https://daostats.github.io/proposals.html
*   **The DAO Carbonvote**: [http://v1.carbonvote.com/](http://v1.carbonvote.com/)
*   **DAO Carbonvote：http://v1.carbonvote.com/
*   **The EIP 186/649/669 Carbonvote**: [http://carbonvote.com/](http://carbonvote.com/)
*   **EIP 186/649/669 Carbonvote：http://carbonvote.com/

![](http://vitalik.ca/files/vote2.png) ![](http://vitalik.ca/files/vote3.png)  
  
![](http://vitalik.ca/files/vote1.png)

  

These three are all examples of _loosely coupled_ coin voting, or coin voting as a layer 2 coordination institution. Ethereum does not have any examples of _tightly coupled_ coin voting (or, coin voting as a layer 1 in-protocol feature), though it _does_ have an example of tightly coupled _miner_ voting: miners’ right to vote on the gas limit. Clearly, tightly coupled voting and loosely coupled voting are competitors in the governance mechanism space, so it’s worth dissecting: what are the advantages and disadvantages of each one?

这三个例子都是松耦合代币投票，或者代币投票作为第二层的协调机构。以太坊没有任何紧密耦合代币投票的例子（或者代币投票作为第一层协议内功能），虽然它确实有密耦合矿工投票的例子：矿工对gas上限投票的权力。显然，密耦合投票和松耦合投票在治理机制领域是竞争对手的关系。所以，他们的优缺点也值得剖析。

Assuming zero transaction costs, and if used as a sole governance mechanism, the two are clearly equivalent. If a loosely coupled vote says that change X should be implemented, then that will serve as a “green flag” encouraging everyone to download the update; if a minority wants to rebel, they will simply not download the update. If a tightly coupled vote implements change X, then the change happens automatically, and if a minority wants to rebel they can install a hard fork update that cancels the change. However, there clearly are nonzero transaction costs associated with making a hard fork, and this leads to some very important differences.

假设零交易费，如果被用作唯一的治理机制，两者是对等的。如果一个松耦合投票说改变X的方案应该被执行，就会释放一个“绿色旗帜（命令）”来鼓励所有人去下载那个更新。如果一个密耦合投票决定改变X的方案应该被执行，那么改变就会自动发生，并且如果少数人想要反抗，他们只能启动一个硬分叉更新来取消这次改变。然而，硬分叉意味着存在实际不为零的交易费，这就产生了一些与松耦合投票非常重要的不同点。

One very simple, and important, difference is that tightly coupled voting creates a default in favor of the blockchain adopting what the majority wants, requiring minorities to exert great effort to coordinate a hard fork to preserve a blockchain’s existing properties, whereas loosely coupled voting is only a coordination tool, and still requires users to actually download and run the software that implements any given fork. But there are also many other differences. Now, let us go through some arguments _against_ voting, and dissect how each argument applies to voting as layer 1 and voting as layer 2.

一个非常简单且重要的不同点是，密耦合投票在区块链中创造了一个偏爱多数人认可的决策默认机制，并要求少数人花大力气去进行一次硬分叉来保存区块链之前的特性。而松耦合投票只是一个协调工具，它仍然要求用户们自行实际下载并运行这些含有更新的软件。当然还有很多不同点，现在让我们解析每一个论点是如何应用于投票作为最底层和次底层的。

### Low Voter Participation

### 低投票参与率

One of the main criticisms of coin voting mechanisms so far is that, no matter where they are tried, they tend to have very low voter participation. The DAO Carbonvote only had a voter participation rate of 4.5%:

代币投票一个被批驳的主要地方在于，不论这种机制在哪里被尝试，投票参与率总是很低。DAO Carbonvote只有4.5%的参与率。

![](http://upyun-assets.ethfans.org/uploads/photo/image/97e569c5676248db835c1a01eaf0e790.png)

  

Additionally, wealth distribution is very unequal, and the results of these two factors together are best described by this image created by a critic of the DAO fork:

此外，财富分布也非常的不均衡，而这两个因素共同导致的结果可以被下面这幅图完美的展现，作为对DAO分叉（fork）的批判：

![](https://i0.wp.com/elaineou.com/wp-content/uploads/2016/07/Screen-Shot-2016-07-18-at-1.28.08-PM.png)

  

The EIP 186 Carbonvote had ~2.7 million ETH voting. The DAO proposal votes [did not fare better](http://themerkle.com/the-dao-undergoes-low-voting-turnout/), with participation never reaching 10%. And outside of Ethereum things are not sunny either; even in Bitshares, a system where the core social contract is designed around voting, the top delegate in an approval vote only got [17% of the vote](https://bitcointalk.org/index.php?topic=916696.330;imode), and in Lisk it got [up to 30%](https://explorer.lisk.io/delegateMonitor), though as we will discuss later these systems have other problems of their own.

EIP 186 Carbonvote有大约270万的ETH投票。DAO提案投票也好不到哪里去，而投票率却从未超过10%。以太坊以外的投票也没好多少；即使在Bitshares，一个围绕投票设计出来的专属核心社会契约的系统中，得票率最高的代表也只有17%的选票，虽然在Lisk中有30%，我们之后会讨论这个系统，它也有问题。

Low voter participation means two things. First, the vote has a harder time achieving a perception of legitimacy, because it only reflects the views of a small percentage of people. Second, an attacker with only a small percentage of all coins can sway the vote. These problems exist regardless of whether the vote is tightly coupled or loosely coupled.

低投票参与率意味着两件事。第一，这个投票很难达到一个合理的百分比，也无法展示出合法性，因为它仅仅反映了小部分人的观点。第二，一个攻击者只需要持有小部分的代币就能够左右整个投票。这些问题在无论是松耦合还是密耦合的投票中都一样存在。

### Game-Theoretic Attacks

### 博弈论论攻击

Aside from “the big hack” that received the bulk of the media attention, the DAO also had a number of much smaller game-theoretic vulnerabilities; [this article from HackingDistributed](http://hackingdistributed.com/2016/05/27/dao-call-for-moratorium/) does a good job of summarizing them. But this is only the tip of the iceberg. Even if all of the finer details of a voting mechanism are implemented correctly, voting mechanisms in general have a large flaw: in any vote, the probability that any given voter will have an impact on the result is tiny, and so the personal incentive that each voter has to vote correctly is almost insignificant. And if each person’s size of the stake is small, their incentive to vote correctly is insignificant _squared_. Hence, a relatively small bribe spread out across the participants may suffice to sway their decision, possibly in a way that they collectively might quite disapprove of.

除了受到大部分媒体关注的“大黑客”之外，DAO还有一些小得多的博弈论漏洞; [来自HackingDistributed的这篇文章]（http://hackingdistributed.com/2016/05/27/dao-call-for-moratorium/）在总结它们方面做得很好。 但这只是冰山一角。 即使投票机制的所有细节都得到了正确实施，投票机制通常也存在很大缺陷：在任何投票中，任何特定投票人对结果产生影响的可能性都很小，因此， 每个选民必须正确投票几乎是微不足道的。 如果每个人的股份规模都很小，他们正确投票的动机是微不足道的。 因此，在参与者身上散布的相对较小的贿赂可能足以影响他们的决定，可能以他们可能完全不同意的方式行事。

Now you might say, people are not evil selfish profit-maximizers that will accept a $0.5 bribe to vote to give twenty million dollars to Josh arza just because the above calculation says their individual chance of affecting anything is tiny; rather, they would altruistically refuse to do something that evil. There are two responses to this criticism.

First, there are ways to make a “bribe” that are quite plausible; for example, an exchange can offer interest rates for deposits (or, even more ambiguously, use the exchange’s own money to build a great interface and features), with the exchange operator using the large quantity of deposits to vote as they wish. Exchanges profit from chaos, so their incentives are clearly quite misaligned with users _and_ coin holders.

Second, and more damningly, in practice it seems like people, at least in their capacity as crypto token holders, _are_ profit maximizers, and seem to see nothing evil or selfish about taking a bribe or two. As “Exhibit A”, we can look at the situation with Lisk, where the delegate pool seems to have been successfully captured by two major “political parties” that explicitly bribe coin holders to vote for them, and also require each member in the pool to vote for all the others.

Here’s LiskElite, with 55 members (out of a total 101):

![](http://vitalik.ca/files/liskpool1.png)

  

Here’s LiskGDT, with 33 members:

![](http://vitalik.ca/files/liskpool2.png)

  

And as “Exhibit B” some voter bribes being paid out [in Ark](https://bitcointalk.org/index.php?topic=1835497.new):

![](https://i.imgur.com/evqfsMj.png)

  

Here, note that there is a key difference between tightly coupled and loosely coupled votes. In a loosely coupled vote, direct or indirect vote bribing is also possible, but if the community agrees that some given proposal or set of votes constitutes a game-theoretic attack, they can simply socially agree to ignore it. And in fact this has kind of already happened - the Carbonvote contains a blacklist of addresses corresponding to known exchange addresses, and votes from these addresses are not counted. In a tightly coupled vote, there is no way to create such a blacklist at protocol level, because agreeing who is part of the blacklist is _itself_ a blockchain governance decision. But since the blacklist is part of a community-created voting tool that only indirectly influences protocol changes, voting tools that contain bad blacklists can simply be rejected by the community.

It’s worth noting that this section **is not** a prediction that all tightly coupled voting systems will quickly succumb to bribe attacks. It’s entirely possible that many will survive for one simple reason: all of these projects have founders or foundations with large premines, and these act as large centralized actors that are interested in their platforms’ success that are not vulnerable to bribes, and hold enough coins to outweigh most bribe attacks. However, this kind of centralized trust model, while arguably useful in some contexts in a project’s early stages, is clearly one that is not sustainable in the long term.

### Non-Representativeness

Another important objection to voting is that coin holders are only one class of user, and may have interests that collide with those of other users. In the case of pure cryptocurrencies like Bitcoin, store-of-value use (“[hodling](https://bitcointalk.org/index.php?topic=375643.0)”) and medium-of-exchange use (“buying coffees”) are naturally in conflict, as the store-of-value prizes security much more than the medium-of-exchange use case, which more strongly values usability. With Ethereum, the conflict is worse, as there are many people who use Ethereum for reasons that have nothing to do with ether (see: cryptokitties), or even value-bearing digital assets in general (see: ENS).

Additionally, even if coin holders _are_ the only relevant class of user (one might imagine this to be the case in a cryptocurrency where there is an established social contract that its purpose is to be the next digital gold, and nothing else), there is still the challenge that a coin holder vote gives a much greater voice to wealthy coin holders than to everyone else, opening the door for centralization of holdings to lead to unencumbered centralization of decision making. Or, in other words...

![](https://i0.wp.com/elaineou.com/wp-content/uploads/2016/07/Screen-Shot-2016-07-18-at-1.28.08-PM.png)

  

And if you want to see a review of a project that seems to combine all of these disadvantages at the same time, see this: [https://btcgeek.com/bitshares-trying-memorycoin-year-ago-disastrous-ends/](https://btcgeek.com/bitshares-trying-memorycoin-year-ago-disastrous-ends/).

This criticism applies to both tightly coupled and loosely coupled voting equally; however, loosely coupled voting is more amenable to compromises that mitigate its unrepresentativeness, and we will discuss this more later.

### Centralization

Let’s look at the existing live experiment that we have in tightly coupled voting on Ethereum, the gas limit. Here’s the gas limit evolution over the past two years:

![](http://vitalik.ca/files/governance3.png)

  

You might notice that the general feel of the curve is a bit like another chart that may be quite familiar to you:

![](https://philoofalexandria.files.wordpress.com/2011/10/top_marginal_income_tax_rate_1913-2003.jpg)

  

Basically, they both look like magic numbers that are created and repeatedly renegotiated by a fairly centralized group of guys sitting together in a room. What’s happening in the first case? Miners are generally following the direction favored by the community, which is itself gauged via social consensus aids similar to those that drive hard forks (core developer support, Reddit upvotes, etc; in Ethereum, the gas limit has never gotten controversial enough to require anything as serious as a coin vote).

Hence, it is not at all clear that voting will be able to deliver _results_ that are actually decentralized, if voters are not technically knowledgeable and simply defer to a single dominant tribe of experts. This criticism once again applies to tightly coupled and loosely coupled voting equally.

_Update: since writing this, it seems like Ethereum miners managed to up the gas limit from 6.7 million to 8 million all without even discussing it with the core developers or the Ethereum Foundation. So there is hope; but it takes a lot of hard community building and other grueling non-technical work to get to that point._

### Digital Constitutions

One approach that has been suggested to mitigate the risk of runaway bad governance algorithms is “digital constitutions” that mathematically specify desired properties that the protocol should have, and require any new code changes to come with a computer-verifiable proof that they satisfy these properties. This seems like a good idea at first, but this too should, in my opinion, be viewed skeptically.

In general, the idea of having norms about protocol properties, and having these norms serve the function of one of the coordination flags, is a very good one. This allows us to enshrine core properties of a protocol that we consider to be very important and valuable, and make them more difficult to change. However, this is exactly the sort of thing that should be enforced in loosely coupled (ie. layer two), rather than tightly coupled (layer one) form.

Basically any meaningful norm is actually quite hard to express in its entirety; this is part of the [complexity of value](https://wiki.lesswrong.com/wiki/Complexity_of_value) problem. This is true even for something as seemingly unambiguous as the 21 million coin limit. Sure, one can add a line of code saying `assert total_supply <= 21000000`, and put a comment around it saying “do not remove at all costs”, but there are plenty of roundabout ways of doing the same thing. For example, one could imagine a soft fork that adds a mandatory transaction fee this is proportional to coin value * time since the coins were last sent, and this is equivalent to demurrage, which is equivalent to deflation. One could also implement another currency, called Bjtcoin, with 21 million _new_ units, and add a feature where if a bitcoin transaction is sent the miner can intercept it and claim the bitcoin, instead giving the recipient bjtcoin; this would rapidly force bitcoins and bjtcoins to be fungible with each other, increasing the “total supply” to 42 million without ever tripping up that line of code. “Softer” norms like not interfering with application state are even harder to enforce.

We _want_ to be able to say that a protocol change that violates any of these guarantees should be viewed as illegitimate - there should be a coordination institution that waves a red flag - even if they get approved by a vote. We also want to be able to say that a protocol change that follows the letter of a norm, but blatantly violates its spirit, the protocol change should _still_ be viewed as illegitimate. And having norms exist on layer 2 - in the minds of humans in the community, rather than in the code of the protocol - best achieves that goal.

### Toward A Balance

However, I am also not willing to go the other way and say that coin voting, or other explicit on-chain voting-like schemes, have no place in governance whatsoever. The leading alternative seems to be core developer consensus, however the failure mode of a system being controlled by “ivory tower intellectuals” who care more about abstract philosophies and solutions that sound technically impressive over and above real day-to-day concerns like user experience and transaction fees is, in my view, also a real threat to be taken seriously.

So how do we solve this conundrum? Well, first, we can heed [the words of slatestarcodex](http://slatestarcodex.com/2017/11/21/contra-robinson-on-public-food/) in the context of traditional politics:

> The rookie mistake is: you see that some system is partly Moloch \[ie. captured by misaligned special interests\], so you say “Okay, we’ll fix that by putting it under the control of this other system. And we’ll control this other system by writing ‘DO NOT BECOME MOLOCH’ on it in bright red marker.”  
> (“I see capitalism sometimes gets misaligned. Let’s fix it by putting it under control of the government. We’ll control the government by having only virtuous people in high offices.”)  
> I’m not going to claim there’s a great alternative, but the occasionally-adequate alternative is the neoliberal one – find a couple of elegant systems that all optimize along different criteria approximately aligned with human happiness, pit them off against each other in a structure of checks and balances, hope they screw up in different places like in that swiss cheese model, keep enough individual free choice around that people can exit any system that gets too terrible, and let cultural evolution do the rest.

In blockchain governance, it seems like this is the only way forward as well. The approach for blockchain governance that I advocate is “multifactorial consensus”, where different coordination flags and different mechanisms and groups are polled, and the ultimate decision depends on the collective result of all of these mechanisms together. These coordination flags may include:

*   The roadmap (ie. the set of ideas broadcasted earlier on in the project’s history about the direction the project would be going)
*   Consensus among the dominant core development teams
*   Coin holder votes
*   User votes, through some kind of sybil-resistant polling system
*   Established norms (eg. non-interference with applications, the 21 million coin limit)

I would argue that it is very useful for coin voting to be one of several coordination institutions deciding whether or not a given change gets implemented. It is an imperfect and unrepresentative signal, but it is a _Sybil-resistant_ one - if you see 10 million ETH voting for a given proposal, you _cannot_ dismiss that by simply saying “oh, that’s just hired Russian trolls with fake social media accounts”. It is also a signal that is sufficiently disjoint from the core development team that if needed it can serve as a check on it. However, as described above, there are very good reasons why it should not be the _only_ coordination institution.

And underpinnning it all is the key difference from traditional systems that makes blockchains interesting: the “layer 1” that underpins the whole system is the requirement for individual users to assent to any protocol changes, and their freedom, and credible threat, to “fork off” if someone attempts to force changes on them that they consider hostile (see also: [http://vitalik.ca/general/2017/05/08/coordination_problems.html](http://vitalik.ca/general/2017/05/08/coordination_problems.html)).

Tightly coupled voting is also okay to have in some limited contexts - for example, despite its flaws, miners’ ability to vote on the gas limit is a feature that has proven very beneficial on multiple occasions. The risk that miners will try to abuse their power may well be lower than the risk that any specific gas limit or block size limit hard-coded by the protocol on day 1 will end up leading to serious problems, and in that case letting miners vote on the gas limit is a good thing. However, “allowing miners or validators to vote on a few specific parameters that need to be rapidly changed from time to time” is a very far cry from giving them arbitrary control over protocol rules, or letting voting control validation, and these more expansive visions of on-chain governance have a much murkier potential, both in theory and in practice.
