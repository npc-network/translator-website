---
title: Today's Crypto Asset Valuation Frameworks
tags:
---

原文链接：https://blockchainatberkeley.blog/todays-crypto-asset-valuation-frameworks-573a38eda27e


Over the past year, several leading cryptocurrency investors and thinkers have proposed a variety of frameworks, heuristics, and metrics that investors can apply to value crypto assets.

In this article, I summarize today’s crypto asset valuation frameworks. I intend to briefly explain the major frameworks and explore their limitations as well as discuss potential further areas of exploration. I conclude with thoughts about the best way to approach valuation for today’s market and the future.

* * *

![](https://cdn-images-1.medium.com/freeze/max/60/1*3syUZ8wO9FxNat9tZVSabQ.png?q=20)

![](https://cdn-images-1.medium.com/max/1600/1*3syUZ8wO9FxNat9tZVSabQ.png)

![](https://cdn-images-1.medium.com/max/1600/1*3syUZ8wO9FxNat9tZVSabQ.png)

1.  **“Store of Value” Thesis**

Main idea: A notable component driving value in digital currencies is an ability to provide a monetary store of value to users or investors. A token’s ability to serve as a store of value can drive notable value to these parties.

Main argument: Currencies have three characteristics: store of value, medium of exchange, and unit of account. Assets such as bitcoin (BTC) or stable coins may have valuable “store of value” features, making them highly attractive to investors. Digital currencies that have steady values by design (i.e., stable coins), or those whom the community expects to either be stable or grow in price, make for attractive “store of value” coins.

Observations:

Like any fiat currency or commodity without meaningful intrinsic utility, the ecosystem’s acceptance, collective belief, and confidence regarding the asset is foundational to its position as a “store of value” crypto asset.

For valuation, one could reference comparable store-of-value assets in the universe such as gold. The world’s total value of gold bullion at an approx. spot price of $1300 is about $8 trillion according to some estimates. If this is any indicator, and if a coin such as bitcoin replaces gold as a store of value (a very, very big \*if\*), then such a crypto asset has outstanding return prospects. In a simple quantification, if we use the example of bitcoin, at a capped supply of 21M BTC, each BTC could see a price of $380,000  if  it were to assume the same place in the world as a store of value as gold ($8T / 21M coins = $380,000 per coin).

**2\. Token Velocity Thesis**

Main idea: Token transaction velocity is one of the key levers that determines long-term token value.

Main Argument: Drawing from The Monetary Equation of Exchange (MV=PQ), which economists call The Quantity Theory of Money, velocity is a significant driver of token price, and the lower the velocity, the greater token price is via an appreciation of M on the left side of the identity. The implication of this thesis is that tokens with low velocity, i.e. those that sit longer in wallets for whatever reason (speculation, store of value, etc.), will see higher prices than other coins, all else equal.

Observations:

A key implication of this idea is that protocols and projects should give users a good reason to hold some coins beyond what they will spend in the system. Motivations could include holding the coin as speculative investment or store of value. Alternatively, the protocol/project could design features that force velocity reductions, such as staking functions (seen in FunFair) or balanced burn-and-mint mechanics (seen in Factom). Generally speaking, staking features such as those in PoS protocols should help support low velocity.

The thesis has fairly widely recognized criticisms, such as:

*   Velocity cannot be precisely defined or measured, whereas the model assumes that it can be defined/estimated and employed to model value.
*   The other factors in the equation, M, P, and Q can also not be easily measured or estimated. In fact, economists would say that you need models to estimate any one of these variables along with their correlations with one another.
*   When velocity changes, the choice to record the effect in M, P, or Q is arbitrary and yields different implications for token price. Further, V’s relationship and correlation with these factors is dynamic, and assuming a steady relationship with P,Q, or M is again arbitrary and problematic.
*   M itself is very difficult to measure in crypto land, as there can be locked up or un-mined currency that may or may not be reflected in the model’s M value.

Contributors: Fred Ehrsam, John Pfeffer, others who have expressed that velocity is one of the more important and useful drivers and indicators of valuation.

**3\. INET & Crypto J-Curve Thesis**

Main idea: The INET model, built by Chris Burniske, is a detailed financial model where token value is estimated using the Monetary Equation of Exchange (MV=PQ) introduced above. Note that INET is simply the name of a fictional token that the analyst is evaluating. Token price is further broken down into two components whose contributions evolve over time: “current utility value” (CUV), which represents value driven by utility and usage today, and “discounted expected utility value” (DEUV), which represents value driven by investment speculation.

Main argument: A token’s current market value can be modeled and projected using inputs including supply-side drivers, adoption and market saturation growth rates, token demand, and velocity. Further, CUV and DEUV and their respective dynamic influences on token price can be modeled and estimated.

Following the monetary equation of exchange (MV=PQ), the token price equals the projected monetary base (M) in the future divided by the number of coins in circulation in the future; M is calculated as equal to PQ/V, or the value of on-chain transaction volume (or “network GDP”) divided by token velocity.

Observations:

Velocity is a crucial assumption and input value, and the model suffers the same drawbacks related to token velocity and interactions with the other factors as described in the velocity thesis argument above.

Crypto J-curve thesis: As the project develops, CUV and DEUV take turns driving token prices as the projects and the market perceptions of them stabilize and mature. When a token is first launched, DEUV dominates as holders are excited about the tech and expect future price appreciation. When enthusiasm wanes with inevitable technical roadblocks, the price declines and is driven more by CUV from technical users and early adopters. As the team overcomes challenges, CUV quietly grows as the token becomes more widely adopted. DEUV then catches up as speculation and excitement follow developer interest. Ultimately in the steady state, CUV should drive token price.

**4\. Network Value-to-Transaction Ratio (NVT)**

Main idea: NVT = network value / daily trx volume. NVT is a valuation ratio that compares the network value (equals the market cap) to the network’s daily on-chain transaction volume.

Main argument: Similar to a the popular equity P/E valuation ratio (either stock price / earnings per share, or market cap / total earnings), NVT may indicate whether a network token is under or overvalued by showing the market cap relative to the network’s transaction volume, which represents the utility that users derive from the network. When the ratio becomes very high, it indicates potential token over-valuation.

Observations:

The ratio best applies to assets whose on-chain transaction volume closely represents utility to users. For instance, bitcoin’s on-chain transaction volume represents the utility it provides to users to send money internationally for very low fees and a degree of anonymity. For networks with high levels of transaction detail privacy such as Monero and Zcash, the ratio is undefined. For networks with staking rewards such as Dash, transaction activity resulting from staking would inflate the denominator, inadvertently causing the ratio to be underestimated. This effect could be corrected for by subtracting staking activity from transaction volume.

Criticisms:

*   Transaction volumes tend to follow changes in price, so the two variables have an endogenous and “reflexive” relationship, weakening the indicative power of the ratio.
*   Thought leaders have experimented with the time frame used to measure daily transaction volume. See the references below for some of this analysis.

Contributors: Chris Burniske, Willy Woo, Coinmetrics team, Dmitriy Kalichkin

**5\. Daily active addresses/users (DAA)**

Main idea: Daily active addresses is a metric and indicator of the number of users that employ the crypto network in transactions on a daily basis.

Main argument: Similar to daily active users (DAU) for software and apps, DAA can provide information about the number of users on a network, which can inform trends and complement other indicators such as NVT and on-chain transaction volume.

![](https://cdn-images-1.medium.com/freeze/max/60/1*m8VeJ-1Jrz5ahQjrHwOPcw.png?q=20)

![](https://cdn-images-1.medium.com/max/1200/1*m8VeJ-1Jrz5ahQjrHwOPcw.png)

### Areas of Future Exploration

1.  **Can we apply traditional valuation methodologies?**

*   **Crypto CAPM?**: It would be interesting to explore how a multi-factor CAPM model could be applied to crypto asset valuation. As with other ratios and quantitative models, since historic return periods are short, the model will be more effective in the future when the crypto asset market matures and we have more data to study the relationships of token prices and various drivers.

The traditional Carhart four-factor CAPM model includes factors for an asset’s expected excess return, a small-cap risk and liquidity premium, book-to-market ratio (value vs growth stocks), and momentum. A “crypto CAPM” model could be evaluated and explored for identifiable factors that could indicate future price return. Factors could include the following, among others. _Note that this information is a simple exploration and would need to be studied much more closely._

*   Momentum factor
*   Liquidity factor (potentially measured by trading volume, bid/ask spreads, or small-cap minus large-cap returns as in CAPM)
*   Token exchange and storage frictions (prevalence on centralized exchanges and decentralized exchange protocols, convenience to purchase, wallet quality, etc.)
*   Community size/strength factor
*   Value: low NVT vs high NVT factor
*   “FOMO” factor (beware of multicollinearity w/ momentum and other factors)
*   Global political or economic uncertainty

A specific crypto asset would have a “beta” coefficient that reflects past or future expected sensitivity to the various market factors. The multi-factor model could ultimately be applied to estimate the value of the overall market, sub-segments of the market, or specific assets, which have a set of betas to each factor.

**Discounted Cash Flow Analysis (DCF)?**: Generally speaking, DCF is not suitable because token investments do not generate cash flows or represent equity claims on cash flows. However, in some cases, a variation of a DCF model may be interesting to employ:

*   If crypto assets in the future evolve to provide equity features such as expected dividends or distributions.
*   If applied to returns from staking and masternode tokens that provide holders certain distributions. Staking tokens such as NEO and VeChain are candidates.

**Comparables valuation approach?**: In traditional equity valuation, the financial ratios and multiples of comparable companies can be used to imply share prices for a target company. Can we apply this approach to crypto assets?

Replace EV/EBITDA, P/E, EV/Sales and other metrics with token-relevant metrics such as NVT (or others as they develop in the future) for a select list of comparable peer token projects. Calculate median levels for comparison group, apply to token project to infer token price.

One challenge to applying this approach to tokens is the presence of strong network effects in digital assets. Few competitors delivering comparable services at once may be able to survive in the marketplace.

**Crypto-networks as small emerging economies?**

Main idea: An interesting, brief idea from the Placeholder VC thesis paper written by Chris Burniske and Joel Monegro stating that the criteria used to evaluate crypto assets is similar those you would use to evaluate the currencies of small EM countries. This could be interesting to explore further.

Main argument: For a crypto asset, the consensus protocol is like a country’s constitution, the community is similar to a constituency (miners are supply-side, users the demand-side), the core devs are like an executive branch who execute code once approved by the community, tokens are similar to an internal currency, and investors underwrite the currency and invest according to relative attractiveness versus other currencies and investments.

For both crypto tokens and a national currency, investors look for sound monetary policy, good governance, low corruption (more of a “nice to have”), low inequality, productivity, etc.

Perhaps one could work with economists to devise a “crypto macroeconomic attractiveness” index or set of indicators that could be applied to tokens, drawing from fundamental indicators in emerging market investments. It could include a crypto “Gini” coefficient as demonstrated in Balaji Srinivasan’s decentralization quantification work, a price stability and monetary policy score, governance score, corruption and transparency index, and more.

### Conclusions: Today and Tomorrow

Crypto markets are very new with limited data history pertaining to crypto asset behavior, returns, and correlations. **Many of today’s models are simplistic or limited, whether intrinsically (due to difficulty defining and measuring variables such as velocity and its counterparts, for instance) or extrinsically (due to limited applicability to different types of tokens, as seen with NVT and privacy coins, for instance).**

In the future when the markets mature and asset relationships and behaviors are more discoverable, valuation models and ratios should be more predictive and informative. However, because of the very diverse nature of crypto assets, which can have different features, structures, payouts, etc., we may never have metrics and models as universal as the P/E ratio and DCF analysis for public equities.

**Today, an effective crypto asset valuation approach should be rooted in a clearly articulated investment thesis and centered on evaluation of qualitative and fundamental criteria.** **The aforementioned valuation frameworks can and should be supplementary.**

**Key fundamental criteria to consider when analyzing crypto assets include factors relating to the project’s team, product, community, token mechanics, governance, market timing, and suitability.**

Today’s crypto asset thought leaders espouse various key investing criteria, such as favoring fair and equitable distribution models (Linda Xie among others), avoiding rent-seeking tokens (Joey Krug and others), and preferring projects that solve problems and align with today’s level of infrastructure and ecosystem development (Fred Ehrsam).

Crypto assets are an emerging alternative asset class, and much work is yet to be done studying valuation frameworks that can help investors estimate token prices. **The aforementioned frameworks and models have several limitations and should be applied only when useful and in company with qualitative analysis, today and tomorrow.**

_I hope you found this article helpful! I’m very happy to discuss further and receive any feedback below._

_Also, I’m on Twitter!_ [_https://twitter.com/ABLannquist_](https://twitter.com/ABLannquist)

References for this article:

*   John Pfeffer, [“An Institutional Investor’s Take on Crypto Assets”](https://s3.eu-west-2.amazonaws.com/john-pfeffer/An+Investor%27s+Take+on+Cryptoassets+v6.pdf)
*   Thomas Euler, “[The Token Classification Framework](http://www.untitled-inc.com/the-token-classification-framework-a-multi-dimensional-tool-for-understanding-and-classifying-crypto-tokens/)”
*   Balaji Srinivasan, “[Thoughts on Tokens](https://news.earn.com/thoughts-on-tokens-436109aabcbe)”
*   Balaji Srinivasan and Leland Lee, “[Quantifying Decentralization](https://news.earn.com/quantifying-decentralization-e39db233c28e)”
*   Nick Tomaino, “[On Token Value](https://thecontrol.co/on-token-value-e61b10b6175e)”
*   Nick Tomaino, “[Our Process for Evaluating Tokens](https://thecontrol.co/our-process-for-evaluating-new-tokens-4627ed97f500)”
*   Rodrigo Gomez-Grassi, “[Markowitz Portfolio Optimization for Cryptocurrencies in Catalyst](https://blog.enigma.co/markowitz-portfolio-optimization-for-cryptocurrencies-in-catalyst-b23c38652556)”
*   Chris Burniske, “[Cryptoasset Valuations](https://medium.com/@cburniske/cryptoasset-valuations-ac83479ffca7)”
*   Chris Burniske and Joel Monegro, “[Placeholder Thesis Summary](https://ipfs.io/ipfs/QmZL4eT1gxnE168Pmw3KyejW6fUfMNzMgeKMgcWJUfYGRj/Placeholder%20Thesis%20Summary.pdf)”
*   Alex Evans, “[On Value, Velocity and Monetary Theory](https://medium.com/blockchannel/on-value-velocity-and-monetary-theory-a-new-approach-to-cryptoasset-valuations-32c9b22e3b6f)”
*   Kyle Samani, “[The Blockchain Token Velocity Problem](https://www.coindesk.com/blockchain-token-velocity-problem/)”
*   Kyle Samani, “[Understanding Token Velocity](https://multicoin.capital/2017/12/08/understanding-token-velocity/)”
*   Brett Winton, “[How to Value a Crypto-Asset — A Model](https://medium.com/@wintonARK/how-to-value-a-crypto-asset-a-model-e0548e9b6e4e)”
*   Willy Woo, “[Is Bitcoin in a bubble? Check the NVT Ratio](https://www.forbes.com/sites/wwoo/2017/09/29/is-bitcoin-in-a-bubble-check-the-nvt-ratio/#6d8909fd6a23)”
*   Dr. Warren Weber, “[The Quantity Theory of Money for Tokens](https://blog.coinfund.io/the-quantity-theory-of-money-for-tokens-dbfbc5472423)”
*   Dmitriy Kalichkin, “[Rethinking Network Value to Transactions (NVT) Ratio](https://medium.com/cryptolab/https-medium-com-kalichkin-rethinking-nvt-ratio-2cf810df0ab0)”
*   Boris Polania, “[CryptoMarkets maturity and price volatility](https://medium.com/@Wholeonomics/cryptomarkets-maturity-and-price-volatility-12575125e919)”

*   [Bitcoin](https://blockchainatberkeley.blog/tagged/bitcoin?source=post)
*   [Cryptocurrency](https://blockchainatberkeley.blog/tagged/cryptocurrency?source=post)
*   [Blockchain](https://blockchainatberkeley.blog/tagged/blockchain?source=post)
*   [Token](https://blockchainatberkeley.blog/tagged/token?source=post)
*   [Investing](https://blockchainatberkeley.blog/tagged/investing?source=post)
