---
title: On Medium-of-Exchange Token Valuations
tags:
---

原文地址：https://vitalik.ca/general/2017/10/17/moe.html

One kind of token model that has become popular among many recent token sale projects is the “network medium of exchange token”. The general pitch for this kind of token goes as follows. We, the developers, build a network, and this network allows you to do new cool stuff. This network is a sharing-economy-style system: it consists purely of a set of sellers, that provide resources within some protocol, and buyers that purchase the services, where both buyers and sellers come from the community. But the purchase and sale of things within this network _must_ be done with the new token that we’re selling, and this is why the token will have value.

If it were the developers themselves that were acting as the seller, then this would be a very reasonable and normal arrangement, very similar in nature to a Kickstarter-style product sale. The token actually would, in a meaningful economic sense, be backed by the services that are provided by the developers.

We can see this in more detail by describing what is going on in a simple economic model. Suppose that N people value a product that a developer wants to release at $x, and believe the developer will give them the product. The developer does a sale, and raises N units for $w < x each, thus raising a total revenue of $N * w. The developer builds the product, and gives it to each of the buyers. At the end of the day, the buyers are happy, and the developer is happy. Nobody feels like they made an avoidable mistake in participating, and everyone’s expectations have been met. This kind of economic model is clearly stable.

Now, let’s look at the story with a “medium of exchange” token. N people value a product that will exist in a decentralized network at $x; the product will be sold at a price of $w < x. They each buy $w of tokens in the sale. The developer builds the network. Some sellers come in, and offer the product inside the network for $w. The buyers use their tokens to purchase this product, spending $w of tokens and getting $x of value. The sellers spend $v < w of resources and effort producing this product, and they now have $w worth of tokens.

Notice that here, the cycle is not complete, and in fact it never will be; there needs to be an ongoing stream of buyers and sellers for the token to continue having its value. The stream does not strictly speaking _have to be_ endless; if in every round there is a chance of at least `v / w` that there will be a next round, then the model still works, as even though _someone_ will eventually be cheated, the risk of any individual participant becoming that person is lower than the benefit that they get from participating. It’s also totally possible that the token would depreciate in each round, with its value multiplying by some factor `f` where `v / w < f < 1`, until it eventually reaches a price of zero, and it would still be on net in everyone’s interest to participate. Hence, the model is theoretically feasible, but you can see how this model is more complex and more tenuous than the simple “developers as seller” model.

  

* * *

  

Traditional macroeconomics has a [simple equation](https://en.wikipedia.org/wiki/Equation_of_exchange) to try to value a medium of exchange:

MV = PT

Here:

*   M is the total money supply; that is, the total number of coins
*   V is the “velocity of money”; that is, the number of times that an average coin changes hands every day
*   P is the “price level”. This is the price of goods and services _in terms of_ the token; so it is actually the _inverse_ of the currency’s price
*   T is the transaction volume: the economic value of transactions per day

The proof for this is a trivial equality: if there are N coins, and each changes hands M times per day, then this is M * N coins’ worth of economic value transacted per day. If this represents $T worth of economic value, then the price of each coin is T / (M * N), so the “price level” is the inverse of this, M * N / T.

For easier analysis, we can recast two variables:

*   We refer to 1/V with “H”, the time that a user holds a coin before using it to make a transaction
*   We refer to 1/P with “C”, the price of the currency (think C = cost)

Now, we have:

M/H = T/C

MC = TH

The left term is quite simply the market cap. The right term is the economic value transacted per day, multiplied by the amount of time that a user holds a coin before using it to transact.

This is a steady-state model, assuming that the same quantity of users will also be there. In reality, however, the quantity of users may change, and so the price may change. The time that users hold a coin may change, and this may cause the price to change as well.

Let us now look once again at the economic effect on the users. _What do users lose_ by using an application with a built-in appcoin rather than plain old ether (or bitcoin, or USD)? The simplest way to express this is as follows: the “implicit cost” imposed by such a system on users _the cost to the user of holding those coins for that period of time, instead of holding that value in the currency that they would otherwise have preferred to hold_.

There are many factors involved in this cost: cognitive costs, exchange costs and spreads, transaction fees, and many smaller items. One particular significant factor of this implicit cost is expected return. If a user expects the appcoin to only grow in value by 1% per year, while their other available alternatives grow 3% per year, and they hold $20 of the currency for five days, then that is an expected loss of roughly $20 * 2% * 5 / 365 = $0.0054.

One immediate conclusion from this particular insight is that **appcoins are very much a multi-equilibrium game**. If the appcoin grows at 2% per year, then the fee drops to $0.0027, and this essentially makes the “de-facto fee” of the application (or at least a large component of it) 2x cheaper, attracting more users and growing its value more. If the appcoin starts falling at 10% per year, however, then the “de-facto fee” grows to $0.035, driving many users away and accelerating its growth.

This leads to increased opportunities for market manipulation, as a manipulator would not just be wasting their money fighting against a single equilibrium, but may in fact successfully nudge a given currency from one equilibrium into another, and profit from successfully “predicting” (ie. causing) this shift. It also means there is a large amount of path dependency, and established brands matter a lot; witness the epic battles over which fork of the bitcoin blockchain can be called Bitcoin for one particular high-profile example.

Another, and perhaps even more important, conclusion is that the market cap of an appcoin **depends crucially on the holding time H**. If someone creates a very efficient exchange, which allows users to purchase an appcoin in real time and then immediately use it in the application, then allowing sellers to immediately cash out, then the market cap would drop precipitously. If a currency is stable or prospects are looking optimistic, then this may not matter because users actually see no disadvantage from holding the token instead of holding something else (ie. zero “de-facto fee”), but if prospects start to turn sour then such a well-functioning exchange can acelerate its demise.

You might think that exchanges are inherently inefficient, requiring users to create an account, login, deposit coins, wait for 36 confirmations, trade and logout, but in fact hyper-efficient exchanges are around the corner. [Here](https://www.reddit.com/r/ethereum/comments/55m04x/lets_run_onchain_decentralized_exchanges_the_way/) is a thread discussing designs for fully autonomous synchronous on-chain transactions, which can convert token A into token B, and possibly even then use token B to do something, _within a single transaction_. Many other platforms are being developed as well.

What this all serves to show is that relying purely on the medium-of-exchange argument to support a token value, while attractive because of its seeming ability to print money out of thin air, is ultimately quite brittle. Protocol tokens using this model may well be sustained for some time due to irrationality and temporary equilibria where the implicit cost of holding the token is zero, but it is a kind of model which always has an unavoidable risk of collapsing at any time.

  

* * *

  

So what is the alternative? One simple alternative is the etherdelta approach, where an application simply collects fees in the interface. One common criticism is: but can’t someone fork the interface to take out the fees? A counter-retort is: someone can also fork the interface to replace your protocol token with ETH, BTC, DOGE or whatever else users would prefer to use. One can make a more sophisticated argument that this is hard because the “pirate” version would have to compete with the “official” version for network effect, but one can just as easily create an official fee-paying client that refuses to interact with non-fee-paying clients as well; this kind of network effect-based enforcement is similar to how value-added-taxes are typically enforced in Europe and other places. Official-client buyers would not interact with non-official-client sellers, and official-client sellers would not interact with non-official-client buyers, so a large group of users would need to switch to the “pirate” client at the same time to successfully dodge fees. This is not perfectly robust, but it is certainly as good as the approach of creating a new protocol token.

If developers want to front-load revenue to fund initial development, then they can sell a token, with the property that all fees paid are used to buy back some of the token and burn it; this would make the token backed by the future expected value of upcoming fees spent inside the system. One can transform this design into a more direct utility token by requiring users to use the utility token to pay fees, and having the interface use an exchange to automatically purchase tokens if the user does not have tokens already.

The important thing is that for the token to have a stable value, it is highly beneficial for the token supply to have **sinks** \- places where tokens actually disappear and so the total token quantity decreases over time. This way, there is a more transparent and explicit fee paid by users, instead of the highly variable and difficult to calculate “de-facto fee”, and there is also a more transparent and explicit way to figure out what the value of protocol tokens should be.



论基于媒介交换的token价值
 

近期，基于网络媒介交换的token在项目代币售卖中变得越来越流行。该token售卖的大体模式如下：开发者开发出了一个网络系统，提供用户在该系统上进行创作。该网络是一个共享经济风格的系统：它由一组通过某种协议提供资源的卖家和购买服务的买家组成，其中买家和卖家都来自社区。在该网络中的买卖必须通过我们（开发者）售卖的token进行, 这是该种类型token有价值的原因。

本质上和kickstarter风格的产品销售模式类似，如果开发者自身作为token的销售者，一切将会变得很合理，因为token实际上能在开发者的保障支持下，被赋予实际的经济意义。

通过一个简单的经济模型我们能看出更多的细节。假设有N人对一款产品进行估值，并认为开发者将会以x美元的价格对该产品标价。接着开发者开始了发售，筹集到了N笔资金，而每笔金额小于$x（假设为$w），总筹集到的金额为$N*w。开发者开发了产品并把产品提供给每一个购买者。最终，开发者和购买者愉快地完成了交易。没人感觉到自身在参与过程中犯了本可以避免的错误，因为每一方的预期都得到满足，这种类型的经济模型显然是稳定的。

现在，让我们了解作为”交易媒介“token的故事。N人对去中心化网络中存在的产品的估值是$x;该产品将以 $w < $x的价格进行售卖。这N人以$w的价格购买token 。 开发者建立网络， 一些卖家加入并且在该网络中以$w的价格提供产品。买家使用token去购买卖家提供的产品，花费价值$w的token获取估值$x的产品， 卖家花费价值$v < w的资源成本生产产品并且得到价值$w的token作为回报。

我们注意到，这个过程并不是完整闭环的，事实上，它永远不会成为完整的闭环; 它需要持续不断地有买家和卖家流加入以延续该token的价值。该“流”并不一定要严格意义上的无界（永不停止）; 如果在每一轮存在至少v / w的几率进入下一轮，那么这种模型依然能运作, 即使某些人最终会被骗，个体参与的风险也小于参与带来的可能利益， token在每一轮中完全可能贬值，即每一轮的价格都在上一轮的基础上乘以一个f因子（v / w < f < 1）, 直到价格最终归零， token在网络存在依然满足参与者的利益。 因此, 这套模型理论上是可行的, 但是您可以发现这种模型相比于简单的“开发者为卖家”模型更加复杂和脆弱。

传统的宏观经济学有一个简单的方程来估算货币价值：

MV = PT

这里：

M是货币供应总量;
V是“货币流通速度”;也就是说，货币平均每天换手的次数
P是“价格水平”。这是商品和服务以token结算的价格;所以它实际上与货币价格负相关
T是交易量：每天交易的经济价值
该等式的证明可以通过简单的等价交换：如果有N个硬币，并且每个人每天换手M次，那么每天交易的是M * N个硬币的经济价值。如果这代表了价值T元的经济价值，那么每个硬币的价格是T /（M * N），所以“价格水平”是它的倒数：M * N / T。

为了便于分析，我们可以重新定义两个变量：

我们将 1/V 称为 “H”，即用户在使用硬币进行交易之前持有硬币的时间
我们用 1/P 表示货币价格 “C”（认为C = 成本）
现在，我们有：

M/H = T/C

MC = TH

左边的等式很简单，就是市值。右边的等式是每天交易的经济总量乘以用户在使用硬币进行交易之前持有硬币的时间。

这是一个稳态模型，假设总是有相同数量的用户在市场中。虽然实际上，用户数量可能会发生变化，价格也可能会发生变化。用户持有硬币的时间可能会改变，这也可能导致价格改变。

现在让我们再看看对用户的经济影响。如果应用程序内置的是appcoin，而不是传统的ETH（或比特币或USD），用户会损失什么？解释这一点最简单的方法如下：这种系统对用户施加的“隐性成本”是用户在花费appcoin之前持有它们，和相比持有其它货币成本的差值。

这种成本涉及很多因素：认知成本，交换成本和价差，交易费用以及许多较小的项目。这种隐性成本的一个特别重要占比是预期收益。如果用户预计appcoin每年仅增值1％，而其他可用替代品每年增长3％，并且他们在5天内持有20美元货币，那么预计损失约为20美元* 2％* 5/365 = 0.0054美元。

从这个角度得出的一个直接结论是，appcoins非常适合多重均衡游戏。如果appcoin每年增长2％，那么费用就会下降到0.0027美元，这实际上使得应用程序（或者至少它的一大部分）的“事实上的费用”降低了2倍，从而吸引更多的用户并使appcoin增值。然而，如果appcoin开始以每年10％的速度贬值，那么“事实上的费用”增长到0.035美元，驱动许多用户离开进而加速贬值。

这导致操纵市场的机会增加，因为操纵者不会浪费他们的资金来对抗单一均衡，而实际上可能成功地将某种货币从一种均衡推动到另一种均衡中，并从成功“预测”（或者说“引起”）转移中获利。这也意味着(市场）有很大的路径依赖性，并且建立品牌很重要;比特币区块链的分叉就是一个特别明显，史诗般的斗争的例子。

另一个，也许更重要的结论是，appcoin的市场上限主要取决于持有时间H.如果有人创建了一个非常有效的交易所，它允许用户实时购买一个appcoin，然后立即使用它申请，然后允许卖家立即兑现，那么市值将急剧下降。如果货币稳定或前景看起来乐观，那么这可能并不重要，因为用户实际上没有持有令牌而没有持有其他东西（即零“事实上的费用”），但如果潜在客户开始变酸那么这样一个运作良好的交易所可以激化它的消亡。

您可能会认为这种交易方式本身效率低下，需要用户创建账户，登录，存入硬币，等待36次确认，交易和注销，但实际上超高效的交易方式即将到来。这里有一个帖子，讨论全自治同步的链上交易，它可以将令牌A转换为令牌B，甚至可能使用令牌B在单个交易中执行某些操作。许多其他平台也在开发中。

这一切都表明，单纯依靠货币交换理论来支持一种token的价值，尽管看上去很有说服力，因为能够凭空发行货币，但最终却非常脆弱。由于市场的非理性和暂时的均衡状态，使用这个模型的token可能会生存一段时间，毕竟持有这种token的隐性成本为0。然而，它始终是一种具有不可避免的随时崩溃风险的模型。

那么有什么其他的方案呢？一个简单方案的是etherdelta的方式，应用程序只是简单地在接口中收取费用。一个普遍的争论是难道不能有人通过修改接口来拿走费用吗？其中一个反驳的观点是有人也可以通过修改接口将协议token替换为ETH，BTC，DOGE或其他任何用户喜欢使用的token。另一个观点认为这很难做到，因为“盗版”版本必须与“官方”版本竞争网络效应，但我们又可以轻松创建一个拒绝与非付费客户端交互的官方付费客户端;这种基于网络效应的实施方式类似于欧洲和其他地方通常执行增值税的方式。官方客户端的买家不会与非官方客户端的卖家交互，而官方客户端的卖家不会与非官方客户端的买家交互，因此大量用户需要切换到“盗版”客户端来减少费用。这并不完全可靠，但它确实与创建一种新的协议token的方式一样好。

如果开发者想要将收入预先用于项目初期开发，那么他们可以出售token，并且所有支付的费用都用于回购一些token并将其销毁;这将使得token的价值会被预计将来在系统内消费的费用所支撑。通过要求用户使用功能性的token来支付费用，并且如果用户没有令牌的话有一个接口通过交易所自动购买token，则可以将该方案转化为一个更直接的功能性token。

一件重要的事情就是为了让token拥有稳定的价值，使token的供给有一个“黑洞”(用来让token永久消失以致随着时间的增长token的数量是递减的)会非常有益。通过这种方式，我们就会得到一种更透明和更明确的被用户支付的费用，而不是高度变化并且很难计算的"实际费用", 并且会得到一种计算协议token价值的更透明和更明确的方法。

