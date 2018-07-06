---
title: governance-part-2-plutocracy-is-still-bad
治理，第2部分：财阀统治仍然是糟糕的
tags:
---

Coin holder voting, both for governance of technical features, and for more extensive use cases like deciding who runs validator nodes and who receives money from development bounty funds, is unfortunately continuing to be popular, and so it seems worthwhile for me to write another post explaining why I (and [Vlad Zamfir](https://medium.com/@Vlad_Zamfir/against-on-chain-governance-a4ceacd040ca) and others) do not consider it wise for Ethereum (or really, any base-layer blockchain) to start adopting these kinds of mechanisms in a tightly coupled form in any significant way.

持币投票除了用于技术的治理之外，更广泛的应用是，例如决定谁运行验证节点以及谁从开发奖金基金中获得奖金。不幸的是，这些持币投票仍然很受欢迎，所以值得写一篇文章来解释为什么我（和Vlad Zamfir及其他人）不认为以太坊（或者真的，任何基础层区块链）采用密耦合（tightly coupled）机制是明智的。

I wrote about the issues with tightly coupled voting [in a blog post](https://vitalik.ca/general/2017/12/17/voting.html) last year, that focused on theoretical issues as well as focusing on some practical issues experienced by voting systems over the previous two years. Now, the latest scandal in DPOS land seems to be substantially worse. Because the delegate rewards in EOS are now so high (5% annual inflation, about $400m per year), the competition on who gets to run nodes has essentially become yet another frontier of US-China geopolitical economic warfare.

我在去年的一篇博文中撰写了关于密耦合的理论，并关注了持币投票机制在过去两年中遇到的一些实际情况。现在，从DPOS上的最新丑闻来看似乎问题严重。由于EOS的代表奖励现在如此之高（年通胀率为5％，每年约为4亿美元），因此谁来运营节点的竞争基本上已成为美中地缘政治经济战争的另一个前沿领域。

![](https://pic4.zhimg.com/v2-a4b7403626be584f21d47837190e99e0_1200x500.jpg)

And that’s not my own interpretation; I quote from [this article (original in Chinese)](https://zhuanlan.zhihu.com/p/34902188):

这不是我说的; 我引用这篇文章（原文为中文）：

> **EOS supernode voting: multibillion-dollar profits leading to crypto community inter-country warfare**

EOS超级投票：数十亿美元的利润导致国家间加密社区战争

> Looking at community recognition, Chinese nodes feel much less represented in the community than US and Korea. Since the EOS.IO official Twitter account was founded, there has never been any interaction with the mainland Chinese EOS community. For a listing of the EOS officially promoted events and interactions with communities see the picture below.

从社区认可的角度来看，中国节点在社区中的活跃度比美国和韩国要小得多。 自EOS.IO官方Twitter账号成立以来，与中国大陆EOS社区从未有过任何互动。 有关EOS正式推出的活动和社区互动的列表，请参阅下面的图片。

![](http://vitalik.ca/files/plutocracy_image1.png)

> With no support from the developer community, facing competition from Korea, the Chinese EOS supernodes have invented a new strategy: buying votes.

由于没有开发者社区的支持，面对来自韩国的竞争，中国EOS超级节点想出了一种新策略：买选票。

The article then continues to describe further strategies, like forming “alliances” that all vote (or buy votes) for each other.

然后原文进一步的描述其策略，比如建立为对方投票（或买票）的“联盟”。

Of course, it does not matter at all who the specific actors are that are buying votes or forming cartels; this time it’s some Chinese pools, [last time](https://liskgdt.net/) it was “members located in the USA, Russia, India, Germany, Canada, Italy, Portugal and many other countries from around the globe”, next time it could be totally anonymous, or run out of a smartphone snuck into Trendon Shavers’s prison cell. What matters is that blockchains and cryptocurrency, originally founded in a vision of using technology to escape from the failures of human politics, have essentially all but replicated it. Crypto is a reflection of the world at large.

当然，具体的参与者是谁并不重要;因为这次可能是一些中国社区选民，上次也许是“位于美国，俄罗斯，印度，德国，加拿大，意大利，葡萄牙和来自世界各地的许多其他国家的会员”，下次可能是完全匿名或用智能手机悄悄进行贿赂买票。然而，最初建立在利用技术摆脱人类政治失败的愿景中的区块链和加密货币，基本上在这样的机制中重复现实的政治失败。

The EOS New York community’s response seems to be that they have issued a strongly worded letter to the world stating that [buying votes will be against the constitution](https://steemit.com/eos/@eosnewyork/block-one-confirms-vote-buying-will-be-against-eos-io-proposed-constitution). Hmm, what other major political entity has [made accepting bribes a violation of the constitution](https://en.wikipedia.org/wiki/Emoluments_Clause)? And how has that been going for them lately?

EOS纽约社区向全世界发出了措辞强硬的声明，声称买选票将违反EOS宪法。嗯，难道还有哪个主要政治主体能接受贿赂选举？  

* * *

  

The second part of this article will involve me, an armchair economist, hopefully convincing you, the reader, that yes, bribery is, in fact, bad. There are actually people who dispute this claim; the usual argument has something to do with market efficiency, as in “isn’t this good, because it means that the nodes that win will be the nodes that can be the cheapest, taking the least money for themselves and their expenses and giving the rest back to the community?” The answer is, kinda yes, but in a way that’s centralizing and vulnerable to rent-seeking cartels and explicitly contradicts many of the explicit promises made by most DPOS proponents along the way.

本文的第二部分将涉及到我这位经济学家希望让读者相信是的，贿赂事实上是很恶劣的事情。有人会质疑这种说法。通常质疑的理由是跟市场效率有关，”这不是很好，因为这意味着最便宜的节点将胜出，自己拿最少花费也最少，并将其余的回馈给社区？”“答案是肯定不是，这种方式容易受到寻租卡特尔的影响，并明显违背了大多数DPOS支持者在此过程中得到的承诺。

Let us create a toy economic model as follows. There are a number of people all of which are running to be delegates. The delegate slot gives a reward of $100 per period, and candidates promise to share some portion of that as a bribe, equally split among all of their voters. The actual N delegates (eg. N = 35) in any period are the N delegates that received the most votes; that is, during every period a threshold of votes emerges where if you get more votes than that threshold you are a delegate, if you get less you are not, and the threshold is set so that N delegates are above the threshold.

让我们创建一个微型经济模型来解释为什么：有很多人参加代表竞选，胜出代表能获得100美元的奖励，候选人承诺将其中的一部分奖金作为贿赂分享给所有投票给他的选民。任何时期，N个代表（例如N = 35）都能只能获得最多N个代表的选票;也就是说，在每个阶段都会出现一个投票的门槛，如果您获得的投票数超过该门槛，您就成为代表，如果您没有达到门槛票数，你就不是代表 。

We expect that voters vote for the candidate that gives them the highest expected bribe. Suppose that all candidates start off by sharing 1%; that is, equally splitting $1 among all of their voters. Then, if some candidate becomes a delegate with K voters, each voter gets a payment of 1/K. The candidate that it’s most profitable to vote for is a candidate that’s expected to be in the top N, but is expected to earn the fewest votes within that set. Thus, we expect votes to be fairly evenly split among 35 delegates.

我们预计选民将投票给那些给予他们贿赂金额最高的候选人。假设所有候选人开始以1％分享;即在所有选民中平均分配1美元。如果某个候选人成为K选民的代表，每个选民都会得到1 / K的支付。投票最有利的候选人应该是预计排名前N的候选人，但预计在该组合中获得最少的选票。因此，我们预计投票将在35名代表中平均分配。

Now, some candidates will want to secure their position by sharing more; by sharing 2%, you are likely to get twice as many votes as those that share 1%, as that’s the equilibrium point where voting for you has the same payout as voting for anyone else. The extra guarantee of being elected that this gives is definitely worth losing an additional 1% of your revenue when you do get elected. We can expect delegates to bid up their bribes and eventually share something close to 100% of their revenue. So the outcome seems to be that the delegate payouts are largely simply returned to voters, making the delegate payout mechanism close to meaningless.

现在，一些候选人希望通过提高贿赂金额来保证自己的胜出;通过分享2％，您可能会获得两倍于贿赂1％的投票。当您当选时，获得这一选举额外损失1％的收入。我们可以期待在这场竞选中，代表最终分享他们收入的100％。因此，结果似乎是变得毫无意义。

But it gets worse. At this point, there’s an incentive for delegates to form alliances (aka political parties, aka cartels) to coordinate their share percentages; this reduces losses to the cartel from chaotic competition that accidentally leads to some delegates not getting enough votes. Once a cartel is in place, it can start bringing its share percentages down, as dislodging it is a hard coordination problem: if a cartel offers 80%, then a new entrant offers 90%, then to a voter, seeking a share of that extra 10% is not worth the risk of either (i) voting for someone who gets insufficient votes and does not pay rewards, or (ii) voting for someone who gets too many votes and so pays out a reward that’s excessively diluted.

但更糟的是，贿赂将促使代表组成联盟（aka政党，又名卡特尔）来协调其份额百分比;减少了混乱竞争造成的损失，而这种竞争无意中导致一些代表得不到足够的选票。一旦卡特尔联盟成立，它可以开始减少其份额，因为它是一个很难协调的问题：如果一个卡特尔提供80％，那么一个新进入者提供90％，然后向一个选民寻求分享额外的10％不值得冒（i）投票得不到选票并且不支付奖励的人，或者（ii）为投票太多的人进行投票，并因此付出过度稀释的奖励。

![](http://vitalik.ca/files/plutocracy_image2.png)

_Sidenote: [Bitshares DPOS](https://bitshares.org/technology/delegated-proof-of-stake-consensus/) used approval voting, where you can vote for as many candidates as you want; it should be pretty obvious that with even slight bribery, the equilibrium there is that everyone just votes for everyone._

旁注：Bitshares DPOS使用核准投票，您可以根据需要为尽可能多的候选人投票; 即每个人都可以为每个后选人投票，这样即使有轻微的贿赂也能获得均衡，这是非常明显的 。

Furthermore, even if cartel mechanics _don’t_ come into play, there is a further issue. This equilibrium of coin holders voting for whoever gives them the most bribes, or a cartel that has become an entrenched rent seeker, contradicts explicit promises made by DPOS proponents.

此外，即使卡特尔机制不起作用，还有一个问题。持币者投票给行贿最高的后选人，或者是一个根深蒂固的寻租者卡特尔都与DPOS支持者的明确承诺相抵触。

Quoting “[Explain Delegated Proof of Stake Like I’m 5](https://hackernoon.com/explain-delegated-proof-of-stake-like-im-5-888b2a74897d)”:

引用“DPOS解释5”：

> If a Witness starts acting like an asshole, or stops doing a quality job securing the network, people in the community can remove their votes, essentially firing the bad actor. Voting is always ongoing.

如果一个证人开始作恶，或者停止/不能提供合格的工作确保网络安全，社区的人们可以删除他们的选票，投票继续进行。

From “[EOS: An Introduction](https://eos.io/documents/EOS_An_Introduction.pdf)”:

从“EOS：简介”：

> By custom, we suggest that the bulk of the value be returned to the community for the common good - software improvements, dispute resolution, and the like can be entertained. In the spirit of “eating our own dogfood,” the design envisages that the community votes on a set of open entry contracts that act like “foundations” for the benefit of the community. Known as Community Benefit Contracts, the mechanism highlights the importance of DPOS as enabling direct on-chain governance by the community (below).

按照惯例，我们建议将大部分价值返还给社区以实现共同利益 - 软件改进，解决纠纷等。本着“吃我们自己的狗粮”的精神，对有利于社区的一系列基础合约进行投票 。该机制被称为“社区效益合约”，强调了DPOS直接对社区链上治理的重要性（下文）。

The flaw in all of this, of course, is that the average voter has only a very small chance of impacting which delegates get selected, and so they only have a very small incentive to vote based on any of these high-minded and lofty goals; rather, their incentive is to vote for whoever offers the highest and most reliable bribe. Attacking is easy. If a cartel equilibrium does not form, then an attacker can simply offer a share percentage slightly higher than 100% (perhaps using fee sharing or some kind of “starter promotion” as justification), capture the majority of delegate positions, and then start an attack. If they get removed from the delegate position via a hard fork, they can simply restart the attack again with a different identity.

当然，这一切的缺陷在于，普通选民对选择哪个代表的影响很小，所以他们很难去就那些高瞻远瞩的目标进行投票;相反，他们投票给那些提供最高贿赂的参选代表。贿赂攻击很容易。如果卡特尔均衡没有形成，那么攻击者可以简单地提供略高于100％的份额百分比（可能使用费用分享或某种“促销”作为理由），捕获大部分选票，然后启动一个攻击。如果他们通过硬分叉代表位置被移除，他们可以简单地以不同的身份再次重新启动攻击。  

* * *

  

The above is not intended purely as a criticism of DPOS consensus or its use in any specific blockchain. Rather, the critique reaches much further. There has been a large number of projects recently that extol the virtues of extensive on-chain governance, where on-chain coin holder voting can be used not just to vote on protocol features, but also to control a bounty fund. Quoting a [blog post from last year](https://medium.com/@FEhrsam/blockchain-governance-programming-our-future-c3bfe30f2d74):

以上内容并非纯粹是针对DPOS共识或使用该共识的特定区块链项目的批评。然而，更加需要批评的是，最近有大量的项目广泛赞颂了上链式治理的优点，在这种上链式持币投票中，不仅可以用来对协议特征进行投票，还可以用来控制赏金发放。引用去年的博文：

> Anyone can submit a change to the governance structure in the form of a code update. An on-chain vote occurs, and if passed, the update makes its way on to a test network. After a period of time on the test network, a confirmation vote occurs, at which point the change goes live on the main network. They call this concept a “self-amending ledger”.  
> Such a system is interesting because it shifts power towards users and away from the more centralized group of developers and miners. On the developer side, anyone can submit a change, and most importantly, everyone has an economic incentive to do it. Contributions are rewarded by the community with newly minted tokens through inflation funding. This shifts from the current Bitcoin and Ethereum dynamics where a new developer has little incentive to evolve the protocol, thus power tends to concentrate amongst the existing developers, to one where everyone has equal earning power.

任何人都可以以代码更新的形式向社区提交治理结构更改的请求。进行链上投票，如果通过，更新将进入测试网络。在测试网络上经过一段时间之后，会发生确认投票，此时该更改将在主网络上进行。他们称这个概念为“自我修正分类账”。
这样的系统很有趣，因为它将权力转移给用户，而不是集中在开发人员和矿主身上。任何人都可以提交更改请求，更重要的是，每个人都有经济动机去这样做。社区通过新挖代币通胀来奖励有利于社区的贡献。这从目前的比特币和以太坊动态转向来看，新的开发者没有什么动力去发展协议，因为权力过度集中在现有的开发者之中，集中在相同的赚钱能力的人群中。

In practice, of course, what this can easily lead to is funds that offer kickbacks to users who vote for them, leading to the exact scenario that we saw above with DPOS delegates. In the best case, the funds will simply be returned to voters, giving coin holders an interest rate that cancels out the inflation, and in the worst case, some portion of the inflation will get captured as economic rent by a cartel.

当然，实际上，这很容易导致资金向为其投票的用户提供回扣，导致像上面的DPOS场景一样。在最好的情况下，资金将被简单地归还给选民，给代币持有人一个抵消通货膨胀的利率，在最坏的是，通货膨胀的一部分将被卡特尔当作寻租租金。

Note also that the above is not a criticism of _all_ on-chain voting; it does not rule out systems like futarchy. However, futarchy is untested, but coin voting _is_ tested, and so far it seems to lead to a high risk of economic or political failure of some kind - far too high a risk for a platform that seeks to be an economic base layer for development of decentralized applications and institutions.

还要注意的是，以上并不是对所有链上投票的批评;不排除有像futarchy这样的系统。虽然，futarchy没有经过测试，但代币投票被测试，到目前为止，它似乎导致某种经济或政治失败的风险很高 - 对一个试图发展成为经济基础层的平台分散的应用程序和机构的风险实在太高。
  

* * *

  

So what’s the alternative? The answer is what we’ve been saying all along: _cryptoeconomics_. [Cryptoeconomics](https://www.coindesk.com/making-sense-cryptoeconomics/) is fundamentally about the use of economic incentives together with cryptography to design and secure different kinds of systems and applications, including consensus protocols. The goal is simple: to be able to measure the security of a system (that is, the cost of breaking the system or causing it to violate certain guarantees) in dollars. Traditionally, the security of systems often depends on _social_ trust assumptions: the system works if 2 of 3 of Alice, Bob and Charlie are honest, and we trust Alice, Bob and Charlie to be honest because I know Alice and she’s a nice girl, Bob registered with FINCEN and has a money transmitter license, and Charlie has run a successful business for three years and wears a suit.

那么还有什么其他选择吗？答案就是我们一直在说的：加密经济学。密码经济学从根本上讲是利用经济激励和密码学来设计和保护不同类型的系统和应用，包括共识协议。目标很简单：能够以美元来衡量安全性的系统（即打破系统或违反某些保证的成本）。传统上，系统的安全性通常取决于社会信任的假设：如果系统中Alice，Bob和Charlie中的2/3是诚实的，系统将工作。我们相信Alice，Bob和Charlie是诚实的，因为我知道Alice和她是一个好女孩， Bob在FINCEN注册并拥有发卡机构许可证，Charlie已经成功运营了三年，并穿着西装。

Social trust assumptions can work well in many contexts, but they are difficult to universalize; what is trusted in one country or one company or one political tribe may not be trusted in others. They are also difficult to quantify; how much money does it take to manipulate social media to favor some particular delegate in a vote? Social trust assumptions seem secure and controllable, in the sense that “people” are in charge, but in reality they can be manipulated by economic incentives in all sorts of ways.

社会信任假设在许多情况下都能很好地发挥作用，但难以普及;在一个国家或一个公司或一个政治部落中信任的东西可能不会被其他人信任。量化也很难;在投票操纵社交媒体以支持某个特定代表需要多少钱？社会信任假设似乎是安全和可控的，因为“人”负责，但实际上他们可以通过各种方式受到经济刺激的操纵。

Cryptoeconomics is about trying to reduce social trust assumptions by creating systems where we introduce explicit economic incentives for good behavior and economic penalties for ban behavior, and making mathematical proofs of the form “in order for guarantee X to be violated, at least these people need to misbehave in this way, which means the minimum amount of penalties or foregone revenue that the participants suffer is Y”. [Casper](http://arxiv.org/abs/1710.09437) [is](https://github.com/ethereum/cbc-casper/wiki) [designed](https://medium.com/@jonchoi/ethereum-casper-101-7a851a4f1eb0) to accomplish precisely this objective in the context of proof of stake consensus. Yes, this does mean that you can’t create a “blockchain” by concentrating the consensus validation into 20 uber-powerful “supernodes” and you have to [actually think](https://medium.com/@icebearhww/ethereum-sharding-workshop-in-taipei-a44c0db8b8d9) to make a design that intelligently breaks through and navigates existing tradeoffs and achieves massive scalability in a still-decentralized network. But the reward is that you don’t get a network that’s constantly liable to breaking in half or becoming economically captured by unpredictable political forces.

密码经济学是通过创建系统来减少社会信任假设，我们引入明确的经济激励措施来奖励良好的行为和惩罚禁止行为，并对形式进行数学证明“为了保证X被违反，至少这些人需要以这种方式行为不端，这意味着参与者遭受的最低处罚或收益是Y“。Casper的目的是在证明利益共识的背景下完成这个目标。这意味着您无法通过将共识验证集中到20个超级强大的“超级节点”中来创建“区块链”，而且您必须真正考虑制定智能突破并使用现有折衷方案并实现大规模可扩展性的设计在一个仍然分散的网络中。但是，奖励是，你没有建立一个网络，这个网络一直不容易突破一半，或者变得经济上被不可预知的政治力量俘虏。
  

* * *

  

1.  _It has been brought to my attention that EOS may be reducing its delegate rewards from 5% per year to 1% per year. Needless to say, this doesn't really change the fundamental validity of any of the arguments; the only result of this would be 5x less rent extraction potential at the cost of a 5x reduction to the cost of attacking the system._

我注意到EOS可能将其代表奖励从每年5％降至每年1％。然尔，这并不会真正改变任何论点的有效性;这样做的唯一结果将是寻租开采可能性减少5倍，而将攻击系统的成本降低5倍。

2.  _Some have asked: but how can it be wrong for DPOS delegates to bribe voters, when it is perfectly legitimate for mining and stake pools to give 99% of their revenues back to their participants? The answer should be clear: in PoW and PoS, it's the protocol's role to determine the rewards that miners and validators get, based on the miners and validators' observed performance, and the fact that miners and validators that are pools pass along the rewards (and penalties!) to their participants gives the participants an incentive to participate in good pools. In DPOS, the reward is constant, and it's the voters' role to vote for pools that have good performance, but with the key flaw that there is no mechanism to actually encourage voters to vote in that way instead of just voting for whoever gives them the most money without taking performance into account. Penalties in DPOS do not exist, and are certainly not passed on to voters, so voters have no "skin in the game" (penalties in Casper pools, on the other hand, **do** get passed on to participants)._

有人问道：但DPOS代表贿赂选民的情况怎么会是错误的呢？对于矿工和股权投资者来说，99％的收入都用于再投资参与完全是合法的。答案应该很清楚：在PoW和PoS中，协议的角色是根据矿工和验证人的表现，确定矿工和验证人得到的回报，以及矿池和验证人为矿池传递奖励（或惩罚）给他们的参与者给予参与者参的动机。在DPOS中，奖励是不变的，选民的角色是投票给表现良好的人，但是有一个严重的缺陷，就是机制没有鼓励选民以这种方式投票，而仅仅投票给谁给的钱最多，没有考虑到绩效表现。惩罚在DPOS的也不存在，当然也没有惩罚会传递给选民，所以选民没有“游戏中的皮肤”（而在Casper池中，处罚是存在的，也确实会传递给参与者）。
