---
title: cryptocurrencies-looking-beyond-the-hype
tags:
---


from page 13 to page 19，the rest of the article is endnotes and references.
Forking and the instability of decentralised consensus in the blockchain（Box V.A）

区块链的分叉和分布式共识的不稳定性（Box V.A)

Forking has contributed to the explosive growth in the number of cryptocurrencies (Graph V.6, right-hand panel). For example, the month of January 2018 alone brought to the fore the Bitcoin ALL, Bitcoin Cash Plus, Bitcoin Smart, Bitcoin Interest, Quantum Bitcoin, BitcoinLite, Bitcoin Ore, Bitcoin Private, Bitcoin Atom and Bitcoin Pizza forks. There are many different ways in which such forks can arise, some permanent and others temporary. One example is termed a “hard fork” (Graph V.A). It arises if some of the miners of a cryptocurrency coordinate to change the protocol to a new set of rules that is incompatible with the old one. This change could involve many aspects of the protocol, such as the maximum permitted block size, the frequency at which blocks can be added to the blockchain or a change to the proof-of-work required to update the blockchain. The miners who upgrade to the new rules start from the old blockchain, but subsequently add blocks that are not recognised by the miners who have not upgraded. The latter continue to build on the existing blockchain following the old rules. In this way, two separate blockchains grow, each with its own transaction history.

分叉带来了加密数字货币种类的爆炸式增长（如图V.6右侧显示（位于第十一页））。举例来说，仅仅2018年一月份就有Bitcoin ALL, Bitcoin Cash Plus, Bitcoin Smart, Bitcoin Interest, Quantum Bitcoin, BitcoinLite, Bitcoin Ore, Bitcoin Private, Bitcoin Atom and Bitcoin Pizza通过分叉脱颖而出。分叉有很多种发生的方式，有些分叉是永久的，有些是暂时的，其中有一种被称为“硬分叉”（图V.A），它是由一些矿工联合改变某个加密数字货币的协议，形成与原生加密数字货币不兼容的一组新的规则而出现的。这些改变包括这个协议的很多方面，如允许的最大区块大小、出块速度、改变用于同步区块链的工作量证明机制等等。升级到新规则的矿工会从旧的区块链开始，在后面添加没有升级的矿工不能识别的区块，而没有升级的矿工会继续在原有的区块链中遵循旧的规则出块，这样就形成了两条独立的区块链，每一条都有完全属于自己的交易历史数据。

Frequent episodes of forking may be symptomatic of an inherent problem with the way consensus is formed in a cryptocurrency’s decentralised network of miners. The underlying economic issue is that this decentralised consensus is not unique. The rule to follow the longest chain incentivises miners to follow the computing majority, but it does not uniquely pin down the path of the majority itself. For example, if a miner believes that the very last update of the ledger will be ignored by the rest of the network of miners, it becomes optimal for the miner to also ignore this last update. And if the majority of miners coordinates on ignoring an update, this indeed becomes a new equilibrium. In this way, random equilibria can arise – and indeed frequently have arisen, as indicated by forking and by the existence of thousands of “orphaned” (Bitcoin) or “uncle” (Ethereum) blocks that have retroactively been voided. Additional concerns regarding the robustness of the decentralised updating of the blockchain relate to miners’ incentives to strategically fork whenever the block added last by a different miner includes high transaction fees that can be diverted by voiding the block in question via a fork.

加密货币的分布式矿工网络形成共识的方式天然就会带来频繁发生的分叉问题。这里背后的经济学问题在于这个分布式共识并不是唯一的。“遵循最长链”这一规则引导矿工去跟从大多数算力的行为，但是它并没有唯一地确定大多数矿工自己的选择。比如，如果一个矿工相信账本最新一次的更新将会被网络中的其他矿工忽略，那么对他来说最优的选择是和其他矿工一样忽略这一次最新的更新。而如果大多数矿工联合起来忽略某次更新，这确实会出现一种新的均衡状态。通过这样的方式，可能、并且确实会出现一些随机的均衡状态，毕竟已经有了那么多的分叉，还有无法追溯的数千个孤块（比特币）和叔块（以太坊）。而关于去中心化的区块同步稳定性的其他问题，则涉及到矿工战略性分叉的动机。当其他矿工最新添加的区块中包含高手续费的交易时，矿工能够通过分叉废除那个区块并将这笔交易转移。

Overall, decentralised cryptocurrencies suffer from a range of shortcomings. The main inefficiencies arise from the extreme degree of decentralisation: creating the required trust in such a setting wastes huge amounts of computing power, decentralised storage of a transaction ledger is inefficient and the decentralised consensus is vulnerable. Some of these issues might be addressed by novel protocols and other advances.27 But others seem inherently linked to the fragility and limited scalability of such decentralised systems. Ultimately, this points to the lack of an adequate institutional arrangement at the national level as the fundamental shortcoming.

总的来说，去中心化的加密货币有一系列的缺陷。其主要的低效来源于极端的权力下放：在这样的体系下消耗大量算力资源和（交易账本的）分布式的存储空间来建立所需要的信任是非常低效的，并且分布式的共识也是很脆弱。在这里某些问题能够通过新的协议和其他研究来解决，但是其他问题似乎和这种去中心化系统的脆弱性和有限可扩展性之间有内在的联系。最终，这指向在国家层面上缺乏合适的体制安排这一根本缺陷。

Beyond the bubble: making use of distributed ledger technology

超越泡沫：利用分布式账本技术

While cryptocurrencies do not work as money, the underlying technology may have promise in other fields. A notable example is in low-volume cross-border payment services. More generally, compared with mainstream centralised technological solutions, DLT can be efficient in niche settings where the benefits of decentralised access exceed the higher operating cost of maintaining multiple copies of the ledger.

虽然加密货币并不能用做金钱，但是其背后的技术能够在很多领域有应用前景。一个值得一提的例子是小批量的跨境支付服务。一般来说，相比于主流的中心化技术解决方案，分布式账本技术在分散式访问的好处超过维护多个账本副本的成本的小众环境中能够高效运行。

To be sure, such payment solutions are fundamentally different from cryptocurrencies. A recent non-profit example is the case of the World Food Programme’s blockchain-based Building Blocks system, which handles payments for food aid serving Syrian refugees in Jordan. The unit of account and ultimate means of payment in Building Blocks is sovereign currency, so it is a “cryptopayment” system but not a cryptocurrency. It is also centrally controlled by the World Food Programme, and for good reason: an initial experiment based on the permissionless Ethereum protocol resulted in slow and costly transactions. The system was subsequently redesigned to run on a permissioned version of the Ethereum protocol. With this change, a reduction of transaction costs of about 98% relative to bank-based alternatives was achieved

可以肯定的是，这类支付解决方案与加密货币是全然不同的。最近的一个非盈利的例子是世界粮食计划署的基于区块链的Building Block系统，这个系统用于处理为约旦叙利亚难民提供粮食援助的付款。Building Block系统的账户单元和最终的支付方式还是主权货币，所以这是一个“加密支付方式”而不是加密货币。并且这个系统是由世界粮食计划署中心化控制的，这有一个合理的理由：基于无权的以太坊协议会导致交易速度慢、费用高。这个系统随后被重新设计，运行在一个有权版本的以太坊协议中。在经过改版之后，比原来用银行处理交易的方式在交易成本上减少了98%。

Permissioned cryptopayment systems may also have promise with respect to small-value cross-border transfers, which are important for countries with a large share of their workforce living abroad. Global remittance flows total more than $540 billion annually (Graph V.8, left-hand and centre panels). Currently, forms of international payments involve multiple intermediaries, leading to high costs (right- hand panel). That said, while cryptopayment systems are one option to address these needs, other technologies are also being considered, and it is not clear which will emerge as the most efficient one.

有权的加密支付系统能够运行小额跨境交易，对于那些在海外有大量的劳动力的国家来说这是非常有用的。每年全球汇款流动超过5400亿美元（如图V.8，左图和中间的图所示），目前国际支付的方式涉及多个中介，带来了很高的成本（如右图所示）。虽然加密支付系统是解决这个需求的一种选择，但是还有其他的技术也纳入了考虑范围内，并且哪一个会成为最有效的方式到现在也不清楚。

More important use cases are likely to combine cryptopayments with sophisticated self-executing codes and data permission systems. Some decentralised cryptocurrency protocols such as Ethereum already allow for smart contracts that self-execute the payment flows for derivatives. At present, the efficacy of these products is limited by the low liquidity and intrinsic inefficiencies of permissionless cryptocurrencies. But the underlying technology can be adopted by registered exchanges in permissioned protocols that use sovereign money as backing, simplifying settlement execution. The added value of the technology will probably derive from the simplification of administrative processes related to complex financial transactions, such as trade finance (Box V.B). Crucially, however, none of the applications require the use or creation of a cryptocurrency.

更重要的应用场景可能是结合复杂的自执行代码和数据许可系统的加密支付方式。一些去中心化的加密货币协议已经能够让智能合约自动执行衍生工具的支付流程，比如以太坊。目前来看，这些产品的效率被低流动性和无权的加密货币自有的低效率所限制。但是，以主权货币为支持的已注册交易所能够在有权协议中使用加密货币背后的技术，来简化结算执行流程。这项技术附加的价值将可能来自简化复杂金融交易相关的行政程序，比如交易金融（详情请见Box V.B）。然而，重点是没有一个应用需要使用或者创建一个加密货币。

Policy implications

政策影响

The rise of cryptocurrencies and related technology brings to the fore a number of policy questions. Authorities are looking for ways to ensure the integrity of markets and payment systems, to protect consumers and investors, and to safeguard overall financial stability. An important challenge is to combat illicit usage of funds. At the same time, authorities want to preserve long-run incentives for innovation and, in particular, maintain the principle of “same risk, same regulation”.29 These are largely recurrent objectives, but cryptocurrencies raise new challenges and potentially call for new tools and approaches. A related question is whether central banks should issue their own central bank digital currency (CBDC).

加密货币和相关技术的兴起带来了一系列的政策问题。当局正在寻找确保市场和支付系统完整性的方法，来保护消费者和投资者，维护整个金融体系的稳定性。其中一个重大的挑战是打击非法集资。同时，当局希望能够长期鼓励创新，特别是维持“风险相同，监管相同”的原则。这些主要是经常性的目标，但是加密货币带来了新的挑战并且可能带来新的工具和手段。另一个相关的问题就是，央行们是否会发行他们自己的数字货币（Central Bank Digital Currency，CBDC）。


Regulatory challenges posed by cryptocurrencies

加密货币带来的监管挑战

A first key regulatory challenge is anti-money laundering (AML) and combating the financing of terrorism (CFT). The question is whether, and to what extent, the rise of cryptocurrencies has allowed some AML/CFT measures, such as know-your- customer standards, to be evaded. Because cryptocurrencies are anonymous, it is hard to quantify the extent to which they are being used to avoid capital controls or taxes, or to engage in illegal transactions more generally. But events such as Bitcoin’s strong market reaction to the shutdown of Silk Road, a major marketplace for illegal drugs, suggest that a non-negligible fraction of the demand for cryptocurrencies derives from illicit activity (Graph V.9, left-hand panel).

首当其冲的监管挑战就是反洗钱（Anti-money Laundering，AML）和打击恐怖主义融资（Combating the financing of terrorism，CFT）。而这里问题在于加密货币技术的出现是否让原有的反洗钱和打击恐怖主义融资的方式（如KYC标准）被不法分子所躲避开来？如果有，那么有多少？因为加密货币的匿名特性，它们在多大范围内被用在躲避资金监管、避税，或者更普遍的说用在不合法交易等事情上我们并不知道。但是一些重大事件（如“丝绸之路”被关闭）之后比特币市场的强烈反应表明，非法交易是加密货币需求中不可忽视的一部分。（图V.9,左图）

A second challenge encompasses securities rules and other regulations ensuring consumer and investor protection. One common problem is digital theft. Given the size and unwieldiness of distributed ledgers, as well as high transaction costs, most users access their cryptocurrency holdings via third parties such as “crypto wallet” providers or “crypto exchanges”. Ironically – and much in contrast to the original promise of Bitcoin and other cryptocurrencies – many users who turned to cryptocurrencies out of distrust in banks and governments have thus wound up relying on unregulated intermediaries. Some of these (such as Mt Gox or Bitfinex) have proved to be fraudulent or have themselves fallen victim to hacking attacks.

第二项挑战包括证券规则和其他的保护消费者和投资者的法规。一个普遍的问题就是数字窃贼。考虑到分布式账本的规模和不实用性，以及高昂的交易手续费，大部分用户通过第三方如加密货币交易所或加密货币钱包提供商来获得加密货币。很讽刺的是，很多用户是出于对银行和政府的不信任而转向加密货币的，却因此依靠不受监管的中介机构，这也与比特币和其他加密货币的初衷相违背。一些这类机构如Mt Gox、Bitfinex等已经被证明在欺骗用户或者遭到过黑客攻击。

Fraud issues also plague initial coin offerings (ICOs). An ICO involves the auctioning of an initial set of cryptocurrency coins to the public, with the proceeds sometimes granting participation rights in a startup business venture. Despite warnings by authorities, investors have flocked to ICOs even though they are often linked to opaque business projects for which minimal and unaudited information is supplied. Many of these projects have turned out to be fraudulent Ponzi schemes (Graph V.9, right-hand panel).

欺诈问题也困扰着首次代币发售（Initial coin offerings，ICOs）。一次首次代币发售涉及向公众出售一套初始的加密货币，在这个过程中会让用户获得初创公司的参与权。即使有了当局的警告，投资者还是涌向ICo，并且经常参与到不透明的商业项目中，因为这些项目提供的是最低限度和未经审计的信息。很多这类项目最后被证明是庞氏骗局。（图V.9，右图）

A third, longer-term challenge concerns the stability of the financial system. It remains to be seen whether widespread use of cryptocurrencies and related self- executing financial products will give rise to new financial vulnerabilities and systemic risks. Close monitoring of developments will be required. And, given their novel risk profiles, these technologies call for enhanced capabilities of regulators and supervisory agencies. In some cases, such as the execution of large-value, high- volume payments, the regulatory perimeter may need to expand to include entities using new technologies, to avoid the build-up of systemic risks.

第三个、长期的挑战，则是关于金融系统的稳定性的。广泛使用加密货币以及相关的自执行的金融产品是否会带来新的金融脆弱性和系统性分险还有待考察，并还需要密切监控发展状况。而且由于它们带来的新的风险状况，这些技术需要监管机构增强监管的能力。在某些场景中，比如在执行大额支付时，监管机构需要扩大监管范围来囊括这些使用新技术的实体，来避免系统性风险的积累。

The need for strengthened or new regulations and monitoring of cryptocurrencies and related cryptoassets is widely recognised among regulators across the globe. In particular, a recent communiqué of the G20 Finance Ministers and Central Bank Governors highlights issues of consumer and investor protection, market integrity, tax evasion and AML/CFT, and calls for continuous monitoring by the international standard-setting bodies. It also calls for the Financial Action Task Force to advance global implementation of applicable standards.

世界各地的监管机构都开始认识到，对加密货币与相关加密资产需要加强执法和监管，甚至需要一套新的法律法规体系。特别是最近在G20峰会上（各国的）财政部长和央行行长强调了消费者和投资者保护、市场完整性、避税、反洗钱、反恐怖主义募资等议题，呼吁全球标准制定机构的持续监管。同时他们也呼吁金融行动特别工作组在全球范围内推动适用标准的实施。

However, the design and effective implementation of strengthened standards are challenging. Legal and regulatory definitions do not always align with the new realities. The technologies are used for multiple economic activities, which in many cases are regulated by different oversight bodies. For example, ICOs are currently being used by technology firms to raise funds for projects entirely unrelated to cryptocurrencies. Other than semantics – auctioning coins instead of shares – such ICOs are no different from initial public offerings (IPOs) on established exchanges, so it would be natural for securities regulators to apply similar regulation and supervision policies to them. But some ICOs have also doubled as “utility tokens”, which promise future access to software such as games. This feature does not constitute investment activity and instead calls for the application of consumer protection laws by the relevant bodies.

然而，加强标准的设计和有效的推进是非常具有挑战性的。法律法规的定义并不总是适应新的现实。加密货币技术应用在很多经济行为中，在很多情况下，这些经济行为被不同监管机构监管。举例来说，ICO现在被技术公司用来为他们那些完全和加密货币无关的项目融资的。除了在语义上用拍卖代币替换了股权，这些ICO和现有交易所中的首次公开募资没有任何差别，因此它自然会被证监会用类似的法规和监管条例监管。但是一些ICO称自己发行的令牌为“效用令牌”，承诺在未来能够用这些令牌访问如游戏等的软件。这样就不构成投资活动，而是需要相关机构应用消费者保护法。

Operationally, the main complicating factor is that permissionless cryptocurrencies do not fit easily into existing frameworks. In particular, they lack a legal entity or person that can be brought into the regulatory perimeter. Cryptocurrencies live in their own digital, nationless realm and can largely function in isolation from existing institutional environments or other infrastructure. Their legal domicile – to the extent they have one – might be offshore, or impossible to establish clearly. As a result, they can be regulated only indirectly. 

在操作层面上，主要的复杂因素是无权的加密货币并不能简单地融入现有的框架中，特别是它们缺少一个法律实体或者个人来让加密货币纳入监管范围。加密货币们活在他们自己的数字化、无国界的疆域中，并且能很大程度在与现有制度环境或者其他基础设施的隔离开来。它们的合法住所-只要他们有一个-就只可能是离岸的，或者不可能明确建立起来。最后结果是它们只能够被间接地监管。

How can authorities implement a regulatory approach? Three considerations are relevant. 

那么当局如何贯彻监管方案？这里有三个相关的要点需要考虑。

First, the rise of cryptocurrencies and cryptoassets calls for a redrawing of regulatory boundaries. The boundaries need to fit a new reality in which the lines demarcating the responsibilities of different regulators within and across jurisdictions have become increasingly blurred.34 Since cryptocurrencies are global in nature, only globally coordinated regulation has a chance to be effective.

首先，随着加密货币与加密资产的出现，监管的范围需要重新调整。监管范围需要适应新的现状，因为现在划分不同管辖范围的监管者之间责任的界限已经越来越模糊了。由于加密货币天生就是全球化的，只有全世界监管机构合作起来才能有机会实现有效的执法。

Second, the interoperability of cryptocurrencies with regulated financial entities could be addressed. Only regulated exchanges can provide the liquidity necessary for DLT-based financial products to be anything but niche markets, and settlement flows ultimately need to be converted into sovereign currency. The tax and capital treatment rules for regulated institutions wanting to deal in cryptocurrency-related assets could thus be adapted. Regulators could monitor whether and how banks deliver or receive cryptocurrencies as collateral. 

其次，加密货币与受监管的金融实体之间的互操作性是可以解决的。只有合规的交易所才能提供基于分布式账本技术的金融产品需要的流动性，而不是在利基市场。在最后，结算的流量都要转化为主权货币。因此对于要处理加密货币相关资产的合规机构，税收和资产处理规则是可以调整的。监管者也可以监管银行是否交付或者接受了加密货币作为抵押，并且监控这些银行是如何执行的。

Third, regulation can target institutions offering services specific to cryptocurrencies. For example, to ensure effective AML/CFT, regulation could focus on the point at which a cryptocurrency is exchanged into a sovereign currency. Other existing laws and regulations relating to payment services focus on safety, efficiency and legality of use. These principles could also be applied to cryptocurrency infrastructure providers, such as “crypto wallets”.36 To avoid leakages, the regulation would ideally be broadly similar and consistently implemented across jurisdictions. 

第三，监管能够针对专门提供加密货币相关服务的机构。比如，为了保证能够有效地反洗钱/打击恐怖主义集资，监管需要着重关注加密货币兑换为主权货币的点。其他现存的关于支付服务的法律法规着重于安全、效率和合法使用等方面。这些规则也能被用在加密货币基础设施提供商上，比如加密钱包。为了避免遗漏，这些法规最理想的是在不同辖区里都大致相似并且都能够得到一致地执行。

Distributed ledger technology in trade finance （Box V.B)


贸易金融中的分布式账本技术（Box V.B）

The World Trade Organization estimates that 80–90% of global trade relies on trade finance. When an exporter and an importer agree to trade, the exporter often prefers to be paid upfront due to the risk that the importer will not make a payment after receiving the goods. Conversely, the importer prefers to reduce their own risk by requiring documentation that the goods have been shipped before initiating payment. 

据世界贸易组织估计，有80-90%的全球贸易依赖于贸易融资。当一个出口商和进口商对一笔交易达成合作时，由于担心进口商收到货物后不会付款，出口商常常希望对方提前支付。而反过来看，进口商则希望在看到货物运输文件之后才开始支付，这样他们自己的风险能够降低。

Trade financing offered by banks and other financial institutions aims to bridge this gap. Most commonly, a bank in the importer’s home country issues a letter of credit guaranteeing payment to the exporter upon receipt of documentation of the shipment, such as a bill of lading. In turn, a bank in the exporter’s country might extend credit to the exporter against this pledge, and collect the payment from the importer’s bank to complete the transaction. 

银行和其他的金融机构提供的贸易金融服务希望能够弥补这条缝隙。最普遍的情况是，在进口商所在国家的银行发行信用凭证，保证在收到如提单等能够证明收到货物的文件之后向出口商付款。反过来，在出口商所在国家的银行可以根据这个信用凭证向出口商提供额外的信用贷款，并从进口商的银行那收取付款来完成这笔交易。

In its current form (Graph V.B, left-hand panel), trade finance is cumbersome, complex and costly. It involves multiple document exchanges between the exporter, the importer, their respective banks, and agents making physical checks of shipped goods at each checkpoint, as well as customs agencies, public export credit agencies or freight insurers. The process often involves paper-based administration. DLT can simplify the execution of the underlying contracts (right-hand panel). For example, a smart contract might automatically release payment to the exporter upon the addition of a valid bill of lading to the ledger. And the better availability of information on which shipments have already been financed could also reduce the risk that exporters illegally obtain credit multiple times for the same shipment from different banks. 

按照目前的形式（图V.B，左边），贸易融资过程十分繁琐而且成本高昂。它涉及到出口商，进口商，双方各自的银行，在验货点的检查货物的代理人，以及海关机构、公共出口信贷机构或货运保险公司之间多份文件的交换。这个过程经常涉及到纸质文件的管理。分布式账本技术能够简化这些合同的执行流程（如右图所示）。比如，一个智能合约能够自动在货物提单记录在账本上之后把货款释放给出口商。并且对于已经融资的货物信息更容易获得，从而降低出口商从不同银行非法获得同一批货物贷款的风险。

Should central banks issue digital currencies? 

中央银行是否该发行数字货币？

A related medium-term policy question concerns the issuance of CBDCs, including who should have access to them. CBDCs would function much like cash: the central bank would issue a CBDC initially, but once issued it would circulate between banks, non-financial firms and consumers without further central bank involvement.37 Such a CBDC might be exchanged between private sector participants bilaterally using distributed ledgers without requiring the central bank to keep track and adjust balances. It would be based on a permissioned distributed ledger (Graph V.2), with the central bank determining who acts as a trusted node. 

一个与话题相关的、中期的政策问题是央行发行自己的数字货币的问题（Central Bank Digitial Currency，CBDC），包括谁能够获得它们。央行数字货币会和法币一样波动。最初会是央行发布数字货币，一旦发布，这些货币会在银行、非金融公司和消费者之间流通起来，不需要央行更多的干涉。这样的央行数字货币可能会在私营部门参与者双边使用分布式账本，而不需要央行来跟踪交易记录和调节余额。它会基于有权分布式账本（如图V.2所示），由央行决定谁能够作为授信节点。

While the distinction between a general purpose CBDC and existing digital central bank liabilities – reserve balances of commercial banks – may appear technical, it is actually fundamental in terms of its repercussions for the financial system. A general purpose CBDC – issued to consumers and firms – could profoundly affect three core central banking areas: payments, financial stability and monetary policy. A recent joint report by the Committee on Payments and Market Infrastructures and the Markets Committee highlights the underlying considerations.38 It concludes that the strengths and weaknesses of a general purpose CDBC would depend on specific design features. The report further notes that, while no leading contenders have yet emerged, such an instrument would come with substantial financial vulnerabilities, while the benefits are less clear. 

虽然通用的央行数字货币和现有的数字央行负债（商业银行的储备金余额）的区别可能在于技术层面上，但它实际上会对金融体系带来根本性的影响。一个通用的、向消费者和公司发行的央行数字货币，会深刻影响三个中央银行的核心业务：支付、金融稳定性和货币政策。最近一份由支付与市场技术设施委员会和市场委员会发布的联合报告强调了一些底层的考虑。它总结道，通用的央行数字货币的优势和劣势会取决于具体的设计特性。这份报告进一步指出，虽然目前尚未出现主要竞争者，但是这种方法会带来巨大的金融脆弱性，况且这样做带来的好处也不是很明显。

At the moment, central banks are closely monitoring the technologies while taking a cautious approach to implementation. Some are evaluating the pros and cons of issuing narrowly targeted CBDCs, restricted to wholesale transactions among financial institutions. These would not challenge the current two-tier system, but would instead be intended to enhance the operational efficiency of existing arrangements. So far, however, experiments with such wholesale CBDCs have not produced a strong case for immediate issuance (Box V.C). 

目前，央行在密切监视这些技术，同时在谨慎地采取一些实施方案。一些央行权衡了发行细分领域数字货币的利与弊，把央行数字货币的应用限制在金融机构之间的大规模交易中。这样并不会挑战现有的双层体系，反而会提高现有安排的运作效率。然而到目前为止，这类用于大规模交易的央行数字货币的实验并并没有得出需要立刻发行数字货币的有力证据。（详情请见BOX V.C）

Wholesale central bank digital currencies(Box V.C)

大规模交易央行数字货币（Box V.C）

In recent decades, central banks have harnessed digital technologies to improve the efficiency and soundness of payments and the broader financial system. Digital technology has enabled central banks to economise on liquidity provision to real-time gross settlement (RTGS) systems. Linking these systems through Continuous Linked Settlement (CLS), commercial banks around the world settle trillions of dollars of foreign exchange around the clock every day. CLS helps to remove Herstatt risk – the risk that a correspondent bank in a foreign exchange transaction runs into financial trouble before paying the equivalent foreign currency to the designated recipient – which had previously posed a significant financial stability risk. More recently, faster retail payments have spread across the world, and central banks are actively promoting and facilitating this trend.

最近几十年，央行利用数字技术提升支付手段和更广泛的金融系统的效率和稳定性。数字化技术让央行能够节约流动性来提供给实时全额结算（RTGS）系统。世界各地的商业银行通过持续联结结算（CLS）来连接这些系统，每天全天候处理数以万亿的外汇结算。持续联结结算帮助消除了赫斯特风险（外汇交易中代理银行在向指定收款人支付等值外币之前遇到财务问题的风险），此前这给金融稳定性带来了严重的风险。最近，更快的零售支付方式已经遍布全球，央行也在积极推动这个趋势。

As part of their broader ventures into new payment technology, central banks are also experimenting with wholesale CBDCs. These are token-based versions of traditional reserve and settlement accounts. The case for wholesale DLT-based CBDCs depends on the potential for these technologies to improve efficiency and reduce operational and settlement costs. The gains could be substantial, to the extent that many current central bank- operated wholesale payment systems rely on outdated and costly-to-maintain technologies.

作为更广泛的新支付技术的一部分，央行们也在实验大规模央行数字货币。这些是基于令牌版本的传统储备和结算账户。最终是否使用大规模的、基于分布式账本技术的央行数字货币取决于这些技术在提高效率以及降低运营和结算成本方面的潜力。若目前很多央行运营的大规模支付系统依赖过时且维护成本高昂的技术，那么这样做的收益会很大。

There are two key challenges for the implementation of wholesale CBDCs. First, the limitations of permissionless DLT also apply to CBDCs, meaning that they need to be modelled on permissioned protocols. Second, the design choices for the convertibility of central bank reserves in and out of the distributed ledger need to be implemented carefully, so as to sustain intraday liquidity while minimising settlement risks.

实施大规模的央行数字货币有两个主要的挑战。首先，无权分布式账本技术的局限性在央行数字货币中也会显现出来，也就是说他们需要被修改为有权的协议。其次，央行储备进出分布式账本的可兑换性的设计选择需要谨慎实施，以维持日内流动性，同时降低结算风险。

A number of central banks, including the Bank of Canada (Project Jasper), the ECB, the Bank of Japan (Project Stella) and the Monetary Authority of Singapore (Project Ubin), have already run experiments operating DLT-based CBDC wholesale RTGS systems. In most cases, the central banks have chosen a digital depository receipt (DDR) approach, whereby the central bank issues digital tokens on a distributed ledger backed by and redeemable for central bank reserves held in a segregated account. The tokens can then be used to make interbank transfers on a distributed ledger.

很多央行，包括加拿大银行（贾思伯项目），欧洲央行，日本央行（斯特拉项目）以及新加坡金融管理局（乌宾项目），都已经在进行运营基于分布式账本技术央行数字货币大规模实时总额结算系统的试验。在多数情况下，央行选择了数字存管收据（DDR）的方法，即央行在分散账户中发行数字令牌，这些分散账户由分离账户中的央行储备支持并可以赎回。这些令牌能够在分布式账本中进行银行间的转账。

Central banks are now publishing the results. In their initial stages, each of the experiments largely succeeded in replicating existing high-value payment systems. However, the results have not been clearly superior to existing infrastructures.

央行现在在公布结果。在他们的初始阶段，每一个试验在很大程度上成功地复制了现有的高价值支付系统。但是，这些结果并没有显示出央行数字货币比现有的基础设施更加优秀。
