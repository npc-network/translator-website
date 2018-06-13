---
title: Celer Network cChannel Part 1 Generalized State Channel Walkthrough
tags:
- Celer
---

> 原文地址：
https://medium.com/@CelerNetwork/celer-network-cchannel-part-1-generalized-state-channel-walkthrough-20a87b390335


Previously on Celer Network….

[**Celer Network MVP: The Most Advanced State Channel Full-Stack Solution**](https://medium.com/@CelerNetwork/celer-network-mvp-the-most-advanced-state-channel-full-stack-solution-21df46234e42)

[**Celer Network Off-Chain Crypto Economics**](https://medium.com/@CelerNetwork/celer-network-off-chain-crypto-economics-13999b11e635)

After the initial release of [our full-stack MVP](https://medium.com/@CelerNetwork/celer-network-mvp-the-most-advanced-state-channel-full-stack-solution-21df46234e42) with cGomoku game, Celer Network has gained extremely positive feedback among technical community. Many developers are asking about the details of cChannel construct, how we use cChannel to build cGomoku and whether we are using side-chain or state channels for that.

**First, we want to clarify that Celer Network’s cChannel is a common abstraction on top of different off-chain scalability solutions including side chains and state channels.** For the initial releases, we are indeed focusing on building out cChannel with generalized state channel as the underlying off-chain scaling foundation.

In this blog, we release our cChannel generalized state channel specification and also provide some educational materials on the key ideas of how cChannel works.

### cChannel State Channel Specification

The community has been asking us about a white paper. Though we have a comprehensive technical white paper describing both cStack and cEconomy, we want to share with the community about the underlying technology innovations little by little.

**We aim to raise the awareness that off-chain scaling platform is not an optimization that is optional but an indispensable abstraction and an entry point for mass adoption of blockchain technology.**

As such, we will try to execute the strategy of releasing bite-sized portion of our white paper accompanying with the explainer blog like this. In this blog, we attach our technical specification for cChannel State Channel and then explain the key concepts through the concrete example of our cGomoku game.

We hope that after reading this blog post, you will have a much better understanding of how cChannel’s state channel component works and why it is powerful. In case you missed the MVP demo video in our previous blog post:

![](https://i.embed.ly/1/display/resize?url=https%3A%2F%2Fi.ytimg.com%2Fvi%2FGoFnWPyEJ18%2Fhqdefault.jpg&key=a19fcc184b9711e1b4764040d3dc5c07&width=40)

### Review of the basics

**Skip this part if you already know what simple payment channel is.**

To understand _generalized_ state channel, the best place to start is simple payment channels. This simple version of state channel is what is used in Lightning Network and Raiden. Just to recap, the simplest bi-directional payment channel works like this:

![](https://cdn-images-1.medium.com/freeze/max/60/1*JyOfBa8n0zhGxCintF_SZA.png?q=20)

![](https://cdn-images-1.medium.com/max/1600/1*JyOfBa8n0zhGxCintF_SZA.png)

![](https://cdn-images-1.medium.com/max/1600/1*JyOfBa8n0zhGxCintF_SZA.png)

Three phases of simple payment channel

First, two (or more) parties who want to frequently transfer each other cryptocurrency initiate deposits to an on-chain smart contract. This smart contract is the on-chain portion of a payment channel. You can think of this smart contract as a “special escrow”. It holds the fund and can distribute the fund based on a mutually signed “agreement” between the two parties. In the above picture, if A and B both sign an “agreement” saying that A has 11BTC and B has 9BTC, anyone can submit this agreement to this escrow contract and they will receive the corresponding BTC amount. This kind of “agreement” is called state proof (proof of the newest state in the state channel). The actual implementation of this state proof may vary.

Next, with this payment channel contract on-chain, both parties can send each other $$$ by just mutually signing state proofs each of which contains their balances and a monotonically increasing sequence number without actually incurring any on-chain delay. This is the core reason why state channel can be horizontally scalable. The communication protocol for this kind of off-chain transactions is also a key part of the off-chain operating network. The protocol is very simple in payment channel cases but can be complex when we move to cChannel’s generalized state channel model.

Finally, whenever any party wants, she can submit the most recent state proof to the on-chain contract and the contract will distribute the money accordingly. In the earlier implementation of payment channels, there is always a “dispute period”, where the counterparties can submit state proof with the higher sequence number (“newer state proof”) to override the pending settlement. However, in the cChannel model, it is only needed in the worst case.

As opening every channel requires on-chain deposits, it is simply not possible to open channel with all peers in the blockchain. To make the approach feasible, the construct of multi-hop payment is proposed initially in the context of Hash Time Lock (HTL) for bitcoin Lightning Network. What HTL trying to achieve here is essentially _trust-free_ payment relay. Take an example in the above picture, as there is no direct channel between A and C, A would like to have a way to pay C via the mutual connection B (middle) without trusting B for any fund custodian responsibility. The implementation of HTL varies, but the high-level idea is basically an atomic lock with synchronized timeout abstraction across all hops in the relay path.

The immediate question comes: okay you have a network, how do you choose a path to relay payments between senders and receivers? Super important question. **Wait for our cRoute blog post.**

### Let’s start with a simple example of generalized state channel

Now let’s move on to generalized state channel. Though the number of articles talking about generalized state channel is very small to start with, almost all of them use the following example to represent the state-of-art:

Great, now you know how payment channel works, so we can generalize the payment states to _arbitrary program states._ Let’s say Alice and Carl want to play a board game while betting on the result of such game in a trust-free manner: Alice will pay Carl $1 if Carl wins and vice versa. This is a simple logic to implement on-chain. One could build a smart contract that holds Alice’s and Carl’s deposits before the game starts. Alice and Carl will just play that game by calling on-chain smart contract’s functions. When one of them loses the game, surrender or simply timeout, the winner gets the loser’s deposit. Unfortunately, on-chain smart contract operations are extremely slow and expensive so no one will want to play such kind of game.

Generalized state channel is here for the rescue. Instead of playing each chess move, Alice and Bob can just deploy the chess game on blockchain with the initial pieces’ state and play the game entirely off-chain by exchanging the signed board states off-chain. When needed, one can inject the most recent board state on-chain. The chess can be played without the long delay of block confirmation and when the chess game is done, they can submit the final result to the contract and contract will give the winner the reward.Voila! Now you have generalized state channel.

“Wait!” you may ask, “**_where is the off-chain logic running?”_** Good question! We will have a **post about cOS to talk about how Celer Network approaches that.**

### cChannel: the power of conditional state dependency

#### Though the above proposal is technically correct and captures many fundamentals of generalized state channel, it is a very primitive form of generalized state channel and **can cause a lot of misconceptions, because it misses the key building block for generalized state channel applications.** Just to list a few misconceptions in the context of this game:

1.  For each game, you have to deploy one on-chain game contract first and then start to play.
2.  For each game, at minimal four on-chain transactions are needed: two deposits, one settle, and one close.
3.  The contract logic has to integrate the payment logic.
4.  Chess game bytecode has to be deployed on blockchain no matter what.
5.  There has to be a direct on-chain state channel between the involved players.
6.  State channel deposits can only be used in this single game.

#### **Well, none of them is true !!!**

### **🙀 🙀 🙀**🙀 🙀 🙀🙀 🙀 🙀

If you think about it, the above chess game example really involves two kinds of states: one is payment and the other is the chess game. The reason they are mingled into one single contract is that we want to realize the semantic of “conditional payment” by requiring each party to do a deposit into this game contract. That is “Alice will pay Bob _on the condition_ that Bob wins the game”.

**Is there any other better way to express the concept of conditional payment?**

**Yes!** For that, we introduce the concept of **off-chain conditional state dependency.**

Let’s consider the following implementation.

Alice and Bob open a special cChannel Generalized Payment Channel (cGPC). cGPC is much more powerful than simple payment channel we mentioned in the above sections. cGPC has the capability to support off-chain conditional payment. Please refer to our technical specification for details, but from a high-level, cGPC has the capability to resolve a state proof with dependency to some other on-chain verifiable states. For the simple example of a boolean condition, Alice can send Bob a signed off-chain message essentially saying “I will pay Bob $5 if _the result of a particular chess game contract_ shows Bob as the winner.”

How is “_a particular chess game contract_” referenced then?

The most straight-forward way is to still have an on-chain contract governing the rule of the board game and that contract’s address and relevant function pointers are referenced in the conditional payment message. All the states are still exchanged off-chain.

But in fact, since there is no requirement for any kind of value bond for program states, the entire game contract and the associated states can all stay off-chain as long as every party is collaborative. The only requirement is that the relevant game states are on-chain verifiable when needs to be. An on-chain verifiable state means other contracts or off-chain messages can refer to it with no ambiguity. To realize that, we need to have an Off-chain Address Translator (OAT) contract that translates off-chain address (such as the hash of contract code, constructor parameters, and nonce) to on-chain references (Ethereum contract address).

Now, this implementation is a much better than the primitive one, because Alice and Bob can just open one single cGPC between them and play many rounds of the game without requiring any on-chain transaction at all (not even need to deploy any game contract). **Just to review, the limitations numbered 1,2,3,4 are all gone!** 😸😸😸😸😸😸

In fact, this kind of conditional state dependency is the core building block of any complex state channel applications. Above example is the most specialized and simple example of off-chain design patterns and it can be much more sophisticated. The conditional payment can be more complicated than just simple Boolean conditions it can be designed in a way to redistribute locked up liquidity based on arbitrary contractual logic. In fact, conditional payment is just a special case of a more generalized conditional state transition.

Sigh, but there are still some limitations 😢 (5 and 6 in above list). It seems that for any state channel applications, all involved parties still need to open dedicated cGPCs. This is really bad.

#### We want Celer Network to serve as entry point for scalable decentralized applications with the look and feel of using the Internet.

How do you use Internet really?

1.  Call Comcast, get a line open.
2.  Use it.

😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅😅

You will think that I am crazy if I tell you that you need to call Comcast every time when you switch your browser tab from Google to Youtube.

![](https://cdn-images-1.medium.com/freeze/max/60/1*zIyJ2qnjGHPmXus-WPTfHA.png?q=20)

![](https://cdn-images-1.medium.com/max/1600/1*zIyJ2qnjGHPmXus-WPTfHA.png)

![](https://cdn-images-1.medium.com/max/1600/1*zIyJ2qnjGHPmXus-WPTfHA.png)

A network of cGPC to enable “Internet-like” easy of use

We want Celer Network to also have that level of ease of use. To realize that, we enable cGPC to be connected as a network. We do not use HTL in the traditional form. We implement the similar semantic of HTL under the powerful building block of conditional state dependency and the resulting “HTL” does not only relay simple payment but also relay arbitrary bonded states such as contractual logic payment.

#### With all these innovations and actual implementations, cChannel can serve as the entry point of scalable blockchain applications and push blockchain into mass adoption.

All these are still simple examples and tons of details regarding state communication and resolution protocols are omitted. Celer Network’s cChannel can enable much more flexible state dependency, aggregation, and resolution semantics. Please refer to our technical specification for details.

### Follow Us

To stay updated about our technical and application releases, follow us via:

Website: [https://www.celer.network/](https://www.celer.network/)

Telegram: [https://t.me/celernetwork](https://t.me/celernetwork)

Github: [https://github.com/celer-network](https://github.com/celer-network)

Twitter: [https://twitter.com/CelerNetwork](https://twitter.com/CelerNetwork)