---
title: Why You Probably Shouldn’t Use a Single Private Key to Secure Your Assets
tags:
---

_Reasons why it is unreasonable to expect yourself and everyone else in the world to only have one fragile layer of security for their assets_

![](https://cdn-images-1.medium.com/freeze/max/60/1*W65-DR2esMrCvm0Ig8pMpg.jpeg?q=20)

![](https://cdn-images-1.medium.com/max/1600/1*W65-DR2esMrCvm0Ig8pMpg.jpeg)

![](https://cdn-images-1.medium.com/max/1600/1*W65-DR2esMrCvm0Ig8pMpg.jpeg)

#### Let me tell you a story….

Matthew Mellon \[1\] was a guy who had high hopes for the cryptocurrency Ripple (XRP). He saw Ripple as a great step forward for the future of American banking. Matthew was one of the first investors in Ripple, and would buy more over the years as the popularity (and price) grew.

As Matthew acquired more XRP, he separated his holdings into a few different accounts.

> Matthew Mellon held almost all of his fortune in Ripple in cold wallets all around the country, with no one else knowing the codes to the wallets. A cold wallet is a vault that is not connected to the internet for safety measures, to avoid hacks or breaches.

Matthew is a smart guy! He is a millionaire who made sure he knew how to manage his crypto holdings himself, keeping his access codes in his head to stay safe from pesky hackers stealing them from a bank.

His XRP will never get taken by anyone! Even himself!

…

huh? himself?

…

Oh yeah. I forgot to mention that Matthew Melon died of a heart attack on April 16th. And when he died, his $500 million in XRP essentially died with him. The XRP is still there! But unfortunately, anyone who wants to access it will need those access codes that are only stored in electrical signals in Matthew’s brain, which disappeared in April.

While Matthew’s story might be the first instance of an extremely rich family losing all their cryptocurrency because of a death, it is by no means the first time anyone has been burned from relying on a single private authorization key to secure an account on a blockchain. Unsurprisingly, this is one of the biggest causes of lost or stolen cryptocurrency.

According to The Anti-Phishing Working group’s research, over **$1.2 billion of crypto-assets have been stolen or lost since the beginning of 2017.**

This is unacceptable! How could all of this value have been lost? Lets look at some of the reasons.

**Lost private keys:** Someone stores their private key either in their brain, on a piece of paper, locally on their computer, or in a hardware wallet. Through one reason or another, it is forgotten, deleted, or lost and nobody can ever access the funds ever again.

**Phishing attacks:** A very bad person gains the trust of the owner of the private key and somehow convinces them to reveal the key. The very bad person then uses the key to steal all of the victim’s assets secured by that key.

**Deaths:** Like Matthew’s case above, the only person who knows the keys dies and the knowledge, and therefore access, to the cryptoassets is lost forever.

**Private key hacks:** An unsuspecting victim stores their private key insecurely on one of their devices and a clever hacker finds a way in and steals the key. With this key, the hacker can access the victim’s account and steal all their cryptoassets.

![](https://cdn-images-1.medium.com/freeze/max/60/1*tOESAZSkdh01dgSKSs6flQ.gif?q=20)

![](https://cdn-images-1.medium.com/max/1600/1*tOESAZSkdh01dgSKSs6flQ.gif)

![](https://cdn-images-1.medium.com/max/1600/1*tOESAZSkdh01dgSKSs6flQ.gif)

There is definitely a pattern here!

### The single-key problem

All of these issues happen because of some unfortunate or irresponsible circumstance that takes advantage of the fact that there is only one layer of security protecting a user’s assets, and there are no take-backs in this world.

Now, some of you might be reading this thinking, “Hrmph! I am incorruptible, invincible, and unable to ever make a mistake!”

Let me be clear, there are plenty of people in the world who are perfectly capable of controlling their own private key and managing it completely on their own, be that with a hardware wallet, cold wallet, or some other solution. And in a perfect world, we all would be able to do that and nobody would try to steal from anyone!

Unfortunately, we live in a world where the vast majority of the population has more important things to worry about than using a bunch of extra brain power and work to secure their keys.

You might be the kind of person who wants complete control, and that is completely fair, but I think we can all agree that most humans (including myself) can be irresponsible, forgetful, or simply too busy to be bestowed with this kind of responsibility.

#### It is obvious that it is unreasonable to expect everyone to have one authorization key and be able to keep it safe and secure themselves.

This indroduces an issue though. Ethereum is based around accounts being associated with just one key, so adding additional layers of security complexity could be risky and challenging.

### How are existing solutions solving this issue?

There are a few offerings out there that acknowledge this issue and look to provide solutions that are safer and easier than a single key solution. Unfortunately, they mostly aren’t good enough to satisfy all the security requirements that users need while also providing complete and a good user experience.

**Solution #1: Centralized storage**

**Company controls your crypto account on your behalf, similar to a traditional bank.** You sign into a centrally managed system with a traditional password and tell the company to sign transactions for you.

**Pros:**

*   OK approach for simply passively holding financial assets
*   Can be secure when done correctly (but rarely is)
*   Simplifies some of the blockchain technical aspects

**Challenges:**

*   Requires trust in third party. If they lose access to your account (private keys) or are hacked, you lose your assets
*   Limited to no management functionality — difficult to use assets outside of just holding them

**Solution #2: Multi-Sig Wallets Controlled by multiple people**

**You and other friends/colleagues each have Ethereum accounts controlled by one private key which are used as authorization signatures in a multisig wallet.** You each control your accounts single private key in the normal way, but don’t hold any funds besides what is needed to execute transactions.

**Pros:**

*   Only a subset of the signatures is required, protecting against death or lost signatures.
*   Control lies with the owners and not a third party.
*   Lost or stolen keys can be changed to protect against theft

**Challenges:**

*   Smart contracts required to implement this can be complicated, which can introduce complexity and unintended behavior that might cause a vulnerability.
*   Hard to interact with decentralized applications when multiple people are required to execute transactions.
*   User experience is still suboptimal, requiring technical knowledge to handle

As you can see, the existing solutions can work in certain situations, but all have drawbacks. Is there a way we can have all the pros of these solutions, but none of the cons?

![](https://cdn-images-1.medium.com/freeze/max/60/1*ttxBTM5pgIzdL0N1kSQfUg.gif?q=20)

![](https://cdn-images-1.medium.com/max/1600/1*ttxBTM5pgIzdL0N1kSQfUg.gif)

![](https://cdn-images-1.medium.com/max/1600/1*ttxBTM5pgIzdL0N1kSQfUg.gif)

Musn’t be afraid to dream a little bigger, darling….

Challenging problems require novel solutions

### EIP-191 and Our Solution

The answer is yes, and it involves an interesting contract standard you might have heard of called [EIP-191: Signed Data Standard](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-191.md). This is a standard that separates the signing of transactions from the sending, allowing for some novel ways to interact with the Ethereum blockchain. This standard allows a contract to accept presigned data by the different keys associated with it and it is the central technology that underpins our upcoming cryptoasset custody application.

We are building a desktop wallet application which uses a unique protocol that requires messages to be signed by multiple private keys. This protocol pieces messages together using an enhanced version of EIP-191. Additionally, we enact transactions through a custom smart contract assigned to each user which understands this protocol. The user’s assets are maintained within this contract and can only be accessed by the requisite private keys assigned to it.

Unlike other multisigs though, this contract/account is only managed by one person! This is because we want to keep this level of security, but also give our users options for how they secure their keys, while never taking complete control of it ourselves.

These private keys can be maintained in a variety of configurations which run the spectrum from decentralization to centralization, depending on the level of responsibility the user is comfortable with:

1.  **Total Control:** The user maintains complete control of all private keys: These keys are encrypted and stored locally on the users device. The password that the user enters to sign into the application is used to decrypt the user profile that is stored locally.
2.  **Partial Control with 2FA:** The user maintains primary private keys and the applicatin maintains supporting private keys utilizing our 2-Factor Authentication. The 2-Factor Authentication code is what authorizes the second key to sign a transaction.
3.  **Partial Control with Third-Party**: The user maintains the primary private key and stores a secondary key with a trusted third-party which automatically authorizes transactions.

**With all of these solutions, the keys are always encrypted, stored locally, and handled by the application, removing the need for users to worry about handling their keys at all.**

A unique feature of our contracts is that all message signing takes place off -chain, with the final message being forwarded to the contract afterward. This gives us the flexibility for users to maintain private keys themselves in several locations distributing signing mechanisms throughout an intranet of personal contacts, for instance, enhancing ownership and security.

![](https://cdn-images-1.medium.com/freeze/max/60/1*r96qkipf_j6cu7OG47P4hw.png?q=20)

![](https://cdn-images-1.medium.com/max/1600/1*r96qkipf_j6cu7OG47P4hw.png)

![](https://cdn-images-1.medium.com/max/1600/1*r96qkipf_j6cu7OG47P4hw.png)

Users sign transactions with their multiple keys, which are then forwarded through their account’s smart contract and posted to the blockchain

**How does this solve the problems of the other solutions?**

As you can see, the flexibility of control this setup offers to users is unparalleled by current offerings. Our solution uses this technology to provide users with an even more secure and user friendly wallet experience.

Since we separates transaction signing and spending, users do not have to worry about specifying and paying for transaction fees within the system, thus alleviating a technical hurdle that many wallet users are very confused about in other solutions. The application actively monitors, manages, and pays for transactions fees under the hood in order for transactions to be sent and processed in a timely manner.

Additionally, Because of the power of multisig wallets, there’s no problem if one of the private keys is lost or exposed. Using the other keys, the compromised key can be recovered or changed to protect against user error and unexpected deaths.

And lastly, this multisig wallet setup is a very low-complexity smart contract, meaning that the attack surface is very small with almost no room for possible vulnerabilities.

### The path forward

As opportunities in blockchain and cryptoassets have grown significantly, more and more people and businesses are entering the space. There is a real threat of technical inexperience resulting in lost funds, and the average user cannot be trusted to manage their own private keys. Modular is working diligently to give businesses and users the management tools to solve these and other challenges.

If Matthew Mellon and more users had a sophisticated tool like what is described here, maybe we wouldn’t have already lost so much money!

This was just a small taste of the security and functionality features that we will offer. Stay tuned and subscribe for more updates and product announcements from Modular. We’ll be detailing more features we offer in upcoming posts in the Modular publication, so make sure to follow in order to receive updates!