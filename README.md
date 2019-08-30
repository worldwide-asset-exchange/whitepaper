# WAX Protocol White Paper


> **August 30, 2019**

By William Quigley, CEO, WAX | Jonathan Yantis, COO, WAX | Lukas Sliwka, CTO, WAX | Malcolm CasSelle, Strategic Advisor, WAX

**Abstract**: The WAX Protocol is a DPoS blockchain designed to scale in conjunction with a microservice layer that provides specialized infrastructure for building digital goods marketplaces. The knowledge required to construct interconnected and highly sophisticated marketplace services comes from the team’s 20+ years’ experience building digital goods businesses,  including the hugely successful OPSkins.com. This document describes the WAX Protocol and how it fits within the WAX Platform. The WAX Platform is the combination of both the WAX Protocol and a microservice layer.

**PLEASE NOTE: THE CRYPTOGRAPHIC TOKENS REFERRED TO IN THIS WHITE PAPER REFER TO TOKENS CREATED ON THE WAX PROTOCOL BLOCKCHAIN. THEY DO NOT REFER TO THE ERC-20 TOKENS DISTRIBUTED IN THE PRIOR TOKEN GENERATION EVENT.**

Copyright © 2019 WAX, Worldwide Asset eXchange

*Disclaimer. This WAX Protocol White Paper is for information purposes only. WAX does not guarantee the accuracy of this white paper and is presented “as is.” WAX does not make and expressly disclaims all representations and warranties, express, implied, statutory or otherwise, whatsoever, including, but not limited to: (i) warranties of merchantability, fitness for a particular purpose, suitability, usage, title or noninfringement; (ii) that the contents of this white paper are free from errors and omissions; and (iii) that such contents will not infringe third-party rights. WAX and its affiliates shall have no liability for damages of any kind arising out of the use, reference to, or reliance on this white paper or any of the content contained herein, even if advised of the possibility of such damages. In no event will WAX or its affiliates be liable to any person or entity for any damages, losses, liabilities, costs or expenses of any kind, whether direct or indirect, consequential, compensatory, incidental, actual, exemplary, punitive or special, for the use of, reference to, or reliance on this white paper or any of the content contained herein, including, without limitation, any loss of business, revenues, profits, data, use, goodwill or other intangible losses or unrealized savings.*

**Contents**

<!-- TOC -->

- [WAX Protocol White Paper](#wax-protocol-white-paper)
- [Introduction](#introduction)
  - [WAX View of the State of Blockchain in 2019](#wax-view-of-the-state-of-blockchain-in-2019)
    - [Mainstream Companies Enter the Market](#mainstream-companies-enter-the-market)
    - [Centralized Models Compete with Blockchain](#centralized-models-compete-with-blockchain)
    - [Ethereum Almost Killed our Business](#ethereum-almost-killed-our-business)
    - [Blockchain is Still Expensive and Hard to Use](#blockchain-is-still-expensive-and-hard-to-use)
    - [Digital Goods = NFTs](#digital-goods--nfts)
    - [\$2.0 Trillion Market Potential](#20-trillion-market-potential)
    - [Fiat and Crypto try to Get Along](#fiat-and-crypto-try-to-get-along)
    - [The Massive Hidden Cost of Fiat Currency Conversion](#the-massive-hidden-cost-of-fiat-currency-conversion)
    - [Instantaneous Ownership Transfer](#instantaneous-ownership-transfer)
    - [The Global Liquidity Pool is a Barrier to Entry](#the-global-liquidity-pool-is-a-barrier-to-entry)
    - [eSports, Influencers, and Monetization of Attention](#esports-influencers-and-monetization-of-attention)
    - [The Dawn of Blockchain Gaming](#the-dawn-of-blockchain-gaming)
- [Solution: The Value Proposition of WAX](#solution-the-value-proposition-of-wax)
- [What is the W.A.S.P. Strategy](#what-is-the-wasp-strategy)
- [How the WAX Platform Works](#how-the-wax-platform-works)
  - [WAX Protocol Blockchain](#wax-protocol-blockchain)
    - [Consensus Model](#consensus-model)
    - [WAX Token Model](#wax-token-model)
      - [WAX Staking Rewards](#wax-staking-rewards)
      - [What functions can I perform by staking my WAX?](#what-functions-can-i-perform-by-staking-my-wax)
      - [How do I earn WAX Staking Rewards by staking my WAX Tokens?](#how-do-i-earn-wax-staking-rewards-by-staking-my-wax-tokens)
      - [WAX Guilds and WAX Guild Rewards](#wax-guilds-and-wax-guild-rewards)
    - [WAX Core Performance Metrics](#wax-core-performance-metrics)
    - [Delegated Proof of Stake (DPoS)](#delegated-proof-of-stake-dpos)
    - [Byzantine Fault Tolerance](#byzantine-fault-tolerance)
    - [Guilds, Block Producers, Staking, and Voting - Enhanced Governance Features](#guilds-block-producers-staking-and-voting---enhanced-governance-features)
      - [WAX Guilds](#wax-guilds)
      - [Standby Guilds](#standby-guilds)
      - [WAX Staking Rewards as a Solution for Voter Apathy](#wax-staking-rewards-as-a-solution-for-voter-apathy)
      - [WAX Staking Rewards](#wax-staking-rewards-1)
      - [Staking Rewards are Based on Performance / Penalties for Underperformance](#staking-rewards-are-based-on-performance--penalties-for-underperformance)
    - [Genesis Block Member Rewards](#genesis-block-member-rewards)
    - [Deflation / Inflation](#deflation--inflation)
    - [Transactions](#transactions)
      - [Providing Cost Efficiency in Terms of Fee Elimination](#providing-cost-efficiency-in-terms-of-fee-elimination)
    - [Smart Contracts + RNG](#smart-contracts--rng)
      - [WAX Random Number Generator (RNG) Smart Contract](#wax-random-number-generator-rng-smart-contract)
      - [How WAX RNG Native Blockchain Service Solves Important Problems](#how-wax-rng-native-blockchain-service-solves-important-problems)
  - [NFT Standards / NFT Integration with WAX ExpressTrade](#nft-standards--nft-integration-with-wax-expresstrade)
  - [Worker Proposal System](#worker-proposal-system)
    - [Why do we need the WWPS?](#why-do-we-need-the-wwps)
    - [Proposed WWPS Categories](#proposed-wwps-categories)
  - [NET, CPU, and RAM Resources on the WAX Blockchain](#net-cpu-and-ram-resources-on-the-wax-blockchain)
  - [Microservice Layer](#microservice-layer)
    - [WAX All Access](#wax-all-access)
    - [WAX Account (soon WAX Wallet)](#wax-account-soon-wax-wallet)
    - [WAX NFT Creator](#wax-nft-creator)
    - [WAX ExpressTrade](#wax-expresstrade)
    - [WAX Explorer](#wax-explorer)
    - [WAX Marketplace](#wax-marketplace)
- [WAX Technical Documentation](#wax-technical-documentation)
- [WAX Projects Showcase](#wax-projects-showcase)
  - [Marketplaces](#marketplaces)
    - [OPSkins](#opskins)
    - [WAXPeer](#waxpeer)
    - [WAXTrades](#waxtrades)
    - [dCart](#dcart)
    - [ByNoGame](#bynogame)
  - [Collectibles](#collectibles)
    - [vIRL](#virl)
    - [VGO](#vgo)
    - [Fnatic](#fnatic)
    - [Augmented Reality](#augmented-reality)
    - [Terra Virtua](#terra-virtua)
  - [E-commerce](#e-commerce)
    - [Fan Controlled Football League (FCFL)](#fan-controlled-football-league-fcfl)
  - [Games](#games)
    - [Z1BR](#z1br)
    - [The Godfather Game](#the-godfather-game)
    - [Animoca Brands](#animoca-brands)
    - [Santeria](#santeria)
    - [WAX.Wiki](#waxwiki)
- [WAX Roadmap](#wax-roadmap)
  - [WAX Developer Hive](#wax-developer-hive)
  - [Office of the Inspector General](#office-of-the-inspector-general)
  - [Ethereum Microservice](#ethereum-microservice)
  - [Public WAX Testnet](#public-wax-testnet)

<!-- /TOC -->





# Introduction 
With the advent of distributed ledger technology and [blockchain](https://en.wikipedia.org/wiki/Blockchain) projects in the past decade, many projects have built solutions in search of a market (the digital goods market) and customers. The Worldwide Asset eXchange’s approach, however, is the opposite. We started our endeavor with a market we understood deeply, as operators of a successful business and millions of registered customers. We had a long list of challenges that needed to be solved to grow the market for digital goods trading globally. We waited for several years to begin building WAX until blockchain was sufficiently mature enough to handle the many requirements for success. The most fundamental requirement was that it could handle the transactions per second necessary for our preexisting consumer demand, with room for significant growth. We designed WAX to solve a specific set of problems in the digital goods market that already has millions of consumers wanting to use it.

The market for digital goods is large and growing fast. What many don't realize is that the digital goods market includes **both** virtual items like [video games](https://en.wikipedia.org/wiki/Video_game_industry) and **tokenized consumer products**. Video games are a \$140 billion market, and tokenized consumer products are a \$1.8 trillion market. The combined market, nearly \$2 trillion, is the market that WAX addresses. In the 12 months of the WAX Protocol's testnet operation with its two largest dApps, VGO and vIRL, the combined trading volume exceeded \$150 million.

<a id="markdown-wax-view-of-the-state-of-blockchain-in-2019" name="wax-view-of-the-state-of-blockchain-in-2019"></a>

## WAX View of the State of Blockchain in 2019

Since the WAX project announcement in June of 2017, the market has evolved rapidly around digital goods. This section on the state of the industry gives some context on the decisions we made in designing the WAX Protocol.


<a id="markdown-mainstream-companies-enter-the-market" name="mainstream-companies-enter-the-market"></a>

### Mainstream Companies Enter the Market
Many have asked how to build a commercially viable business platform in the blockchain world, given the challenges from a regulatory standpoint. Most governmental agencies cannot agree on who regulates [cryptocurrencies](https://en.wikipedia.org/wiki/Cryptocurrency). Additionally, mainstream financial firms, tech companies, social networks, and other powerful institutions are now looking to compete or work with many companies in the blockchain industry.

With the announcement of blockchain initiatives by Facebook, JP Morgan, Fidelity, Bank of America, and others, the ecosystem is seen as rapidly legitimized in the last year. Visa and Mastercard have signed up to be nodes in the digital currency Project Libra. Who would have predicted that in 2017?

In this context, we observed several other important challenges.


<a id="markdown-centralized-models-compete-with-blockchain" name="centralized-models-compete-with-blockchain"></a>

### Centralized Models Compete with Blockchain
The transition from a centralized to a decentralized blockchain model for WAX was not without challenges. June 2018 was an important moment for WAX because we announced the launch of WAX ExpressTrade. It's a product free to use by anyone for the trading of digital goods and a prototype of the WAX Platform microservice layer. WAX ExpressTrade competed with Steam, the community marketplace operated by Valve (the game publisher for Counter-Strike: Global Offensive a.k.a. CS:GO). The problem was that CS:GO was the largest source of our virtual items at the time. Since the game publisher balked at our product announcement and threatened to ban our trading bots, we had to choose between launching into our blockchain future with that product and be banned by Valve, or hold back and stay beholden to Valve’s platform.

We made our choice and here we are today doing more volume than ever without the fear of Valve’s policies that at times appeared arbitrary to us. Going 100% independent was a tough decision for us, and yet an important one to separate WAX from the centralized control systems that dominated the skins market. Games like Fortnite, CS:GO, and many others have centrally controlled skins that either prevent trading or restrict it severely. However, we see this trend changing (more on that later).

As a side note, the vIRL dApp and other dApps like it can make any tradeable item on Steam also tradeable on WAX. In essence, WAX is the technology wrapper that encompasses all other virtual items that exist. Interoperability by design makes WAX very versatile.


<a id="markdown-ethereum-almost-killed-our-business" name="ethereum-almost-killed-our-business"></a>

### Ethereum Almost Killed our Business 
In 2018, after the split with Valve, developers from the community quickly launched a dApp for skins, VGO. VGO had been in the works already, but the unexpected rift with Valve caused us to work with the developers to launch it sooner than expected. Despite that, they anticipated it was all going to work well in theory...until we started to utilize the most-used blockchain at the time, Ethereum. Soon after launch, we woke up one day to find VGO was suddenly losing millions of dollars a day due to the chain's slowdown and costs. Yes, Ethereum almost killed the world's largest dApp (at the time). Don't get us wrong - we love Ethereum. Trying to build a viable commercial business on it, however, is a different matter altogether. However, during a spike in network usage that slowed confirmations from minutes to hours and drove up transactions fees 100x overnight, the dApp, VGO, was unusable. So VGO switched to a WAX alpha network. It was the only way to get that dApp to work because the WAX Protocol Blockchain was not ready yet.

<a id="markdown-blockchain-is-still-expensive-and-hard-to-use" name="blockchain-is-still-expensive-and-hard-to-use"></a>

### Blockchain is Still Expensive and Hard to Use
Today VGO runs cheaply and easily on the WAX Protocol Blockchain. A similar dApp to VGO can also do the same because the hard parts are handled by WAX. WAX's developers have worked relentlessly to address many unanswered questions and solve hard problems. Governance, voter apathy, interoperability, backward compatibility, security, and a long list of other challenges took an enormous amount of time and debate. We must congratulate our developer team for working through most of these this past year. We are proud of both our world-class developers and the blockchain they created. We also want to thank the core devs at EOS and the folks at [StrongBlock](https://strongblock.io/) for their guidance and input.

Overall the experience in building a business with a blockchain should cause anyone to conclude, like ourselves, that it is not easy. WAX developed solutions to solve several particular problems that we go into more detail below. However, a centralized system is always easier to build and manage. Accepting this design principle, it informed our choices to build the microservice layer that gives dApps a considerable advantage when operating on WAX.

As the blockchain market matures and projects need to achieve real financial results to sustain themselves, they need to acquire customers, so generating a profit becomes the highest priority. The transition from starting with a visionary "moonshot" idea into a real business is what makes WAX so important. Every day developers look at WAX and see an opportunity to expand their business with minimal work. WAX saves many types of businesses time in acquiring customers, ranking and understanding their value, accepting fiat (government-backed money) payments, acquiring digital item inventory, and addressing many other business-critical functions.

-   **How do dApps acquire customers when their interfaces are hard to use?** Customers find WAX easy to use, so dApps using WAX don't have that problem.

-   **How do dApps accept fiat payments or allow customers to bring their item inventory and account balances with them so they can use those items or spend balances?** WAX handles all of these functions, so dApps using WAX don't have that problem.

-   **How do dApps create truly provably fair random functions?** With WAX, the random number generator is on the blockchain, saving dApps a ton of effort to build their own while also proving the fairness of the random number generator to customers.

WAX was designed to make blockchain easy for dApps. We did the hard work, so dApps don’t have to.



<a id="markdown-digital-goods--nfts" name="digital-goods--nfts"></a>

### Digital Goods = NFTs
Unlike **fungible tokens**, like bitcoin and ethereum, where one token is indistinguishable from another, with **non-fungible tokens** (NFTs), like VGO, vIRL, and ERC-721/1155, each item is unique and is a particular item.

Digital goods, or NFTs, are popular topics of conversation in the blockchain world today. But not too long ago, in mid-2017, using tokens to secure, store, and send virtual items in video games was discussed by only a few projects and crypto enthusiasts — those who understood video games. With the overall popularity of video games and the idea that NFTs could replace the virtual items in a video game centrally controlled by game publishers, we have seen many protocol chains dedicate hundreds of millions of dollars of investment to NFTs and video games. With the Ethereum-based ERC-721 standard, which then led to the ERC-1155 standard, many video game developers started to look at this new opportunity to attract game players around the idea of real ownership of their virtual items. These protocol projects' recurring theme was to stimulate more game publishers to create NFTs to run on their chain because that would drive adoption.

Seeing some of the top 10 protocols discover and subsequently focus on video game assets was a satisfying moment from the WAX perspective because we have been focused on this market from the beginning and saying all along that it is the way forward. **WAX is a protocol chain singularly dedicated to digital goods**, and as we predicted, and others have concluded, video games are the gateway to mass adoption of blockchain technology. More consumers are likely to use virtual items from video games and digital goods based on the blockchain than any other applications available today. With 2.3 billion gamers worldwide and \$140 billion spent annually, it's a large enough audience spending enough money to propel blockchain technology into everyday usage. We see the beginnings of that adoption already based on the daily metrics on WAX.

Overall, we see several NFT marketplaces struggling because they are trying to interact directly with smart contracts and cryptocurrency. We fundamentally believe that approach only leads to customer attrition because it is so laborious and challenging. The small NFT marketplace customer base and low activity suggest, as we believe, customers want something easier, faster, and cheaper, as well as fiat payments. Since WAX has the most liquidity with fiat payments and is easy to use for customers, we believe all items will eventually end up connected to WAX.

All roads for digital goods lead to WAX.


<a id="markdown-\20-trillion-market-potential" name="\20-trillion-market-potential"></a>

### \$2.0 Trillion Market Potential
WAX's target market for digital goods is a superset comprised of virtual items from video games (\$140 billion in total sales, \$50 billion in secondary trading volume) and potentially tokenized products from consumer e-commerce (\$1.8 trillion of a global \$2.8 trillion e-commerce market). In our calculation, we add the primary sales of video games and video game items and secondary virtual item sales because the WAX Platform supports both. The subset of products we see tokenizable is \$1.8 trillion of the \$2.8 trillion e-commerce market. Today, taken together, that's about a \$2 trillion total market size for digital goods.

That’s big. Having processed \$550+ million worth of items on the testnet of the WAX Protocol Blockchain in the last 12 months, we are fairly certain customers like what we have built so far. But we have a long way to go to capture the potential we envision for WAX.



<a id="markdown-fiat-and-crypto-try-to-get-along" name="fiat-and-crypto-try-to-get-along"></a>

### Fiat and Crypto try to Get Along
Fiat and cryptocurrencies, for the foreseeable future, must co-exist so that platforms can take advantage of blockchain technology and also provide the convenience consumers expect using credit cards, debit cards, and ACH. Cryptocurrencies are not yet a primary payment method of choice in any major business segment and are generally considered an inconvenient way to pay. Although merchants are attracted to the idea of low fees and no chargebacks, volatile coin prices and the difficulty of the payment process itself impedes them from taking advantage of blockchain technology.


<a id="markdown-the-massive-hidden-cost-of-fiat-currency-conversion" name="the-massive-hidden-cost-of-fiat-currency-conversion"></a>

### The Massive Hidden Cost of Fiat Currency Conversion
Cross border trade accounted for \$25 trillion in value in 2018, representing 30% of global GDP. This trade is facilitated by 180 separate fiat currencies. Since most buyers and sellers conducting cross border commerce prefer their own native currency, a foreign exchange intermediary is needed to help settle the transaction. Of course, this help comes at a very steep - and often hidden - price. Currency conversion costs are embedded in the foreign exchange buy/sell spread. These currency conversion spreads are like a hidden tax amounting to hundreds of billions of dollars annually on global consumers and corporations. Where does this money go? It is captured by thousands of payment processors, banks, foreign exchange traders and other financial institutions.

Now imagine if there was just one currency. If all prices were denominated in the same currency, and everyone used that common currency for payment, it would amount to a global dividend to humanity in an amount equal to such currency conversion costs.

This ambitious (and unrealistic for the time being) idea is the inspiration for Facebook's stable coin. Facebook highlighted excessive transaction fees as one of the principal reasons for Libra Coin's creation. Facebook is well aware of the high payment processing costs consumers bear when making purchases, particularly small cross border purchases. These fees can sometimes exceed 50% for small transactions in less liquid currencies.

WAX identified the cross border consumer payment problem early on do to our experience operating Opskins, a digital goods exchange that serves a global audience. Most Opskins customer transactions involve a buyer and seller in different countries. And most transactions are sub \$25. We saw the opportunity to employ blockchain technology to make buying and selling digital goods with anyone in the world cheaper and faster.


<a id="markdown-instantaneous-ownership-transfer" name="instantaneous-ownership-transfer"></a>

### Instantaneous Ownership Transfer 
Marketplaces for physical goods today are subject to the inherent friction of physicality -- objects are heavy, take up space, and have to be handled, packaged, shipped on a boat/truck/plane, tracked physically, scanned, and paid for at customs. We usually think of receiving the delivery, and hence ownership, as the equivalent. Today, physical "ownership" (possession) via e-commerce typically takes hours, days, or weeks.

Yet, tokenized consumer goods in the vIRL dApp travel at the speed of networks between parties. That means customers can trade a pair of sneakers with someone in a different region globally and have possession of the tokenized good within seconds. No other technology allows the instantaneous transfer of ownership of consumer items no matter what the distance and jurisdiction. Possession is still subject to shipping, but as it turns out today, much commerce does not require possession, and more commerce is going in that direction.

In the case of vIRLs, this is especially true because they are tokenized physical collectibles, such as an expensive pair of sneakers. It is far more efficient to inspect and certify the sneakers once and to change hands many times digitally before the actual sneakers are pulled out of a warehouse and sent to the last person who redeems them. Rather than sending the item back and forth via mail each time it changes hands, the item stays put and ownership transfers digitally. vIRLs can change hands 200 times (or more) and accomplish in a week what would take more than a year to do if the sneakers had to move each time physically. In the case of collectors for expensive items, vIRLs are even more attractive because each time the item it touched or moved it can incur a cost for authentication, packaging and insurance, or add wear and tear to the item, degrading its value. viRLs help collectible items stay valuable and makes it easy for collectors to trade, sell, and ultimately increase the value of their inventory.



<a id="markdown-the-global-liquidity-pool-is-a-barrier-to-entry" name="the-global-liquidity-pool-is-a-barrier-to-entry"></a>

### The Global Liquidity Pool is a Barrier to Entry
Because vIRL digital goods are so easy to transfer on WAX, the frequency of trades increases and makes the marketplace more "liquid." That means items sell faster and, in turn, more items are attracted to the marketplace.

The other advantage to WAX's model is the global supply of items that everyone gets access to when launching a dApp. Getting inventory immediately from anywhere in the world is very valuable for a store. Likewise, new stores continually add new products for sale that might end up selling on some other marketplace. Buyers and sellers benefit each other and the larger the liquidity pool, the greater the network effect and the harder it is to replicate what WAX has built.


<a id="markdown-esports-influencers-and-monetization-of-attention" name="esports-influencers-and-monetization-of-attention"></a>

### eSports, Influencers, and Monetization of Attention
A significant source of video content related to video games comes from eSports events, as well as individual YouTube and Twitch influencers playing games or talking about games. The magnitude of time spent watching video games is a staggering 84.7 billion hours per year. Based on a 2017 report by SUPERDATA, roughly 670 million people are watching video game content instead of primetime TV. The staggering amount of attention consumers give to video content creators presents a potentially lucrative and untapped opportunity for WAX.

One revenue stream for content creators comes from selling merchandise. The integration of merchandise and streaming content is still growing, while digital items appear to sell very fast and drive significant engagement. We have found with our partnerships that using WAX for digital items, as well as vIRLs, excites viewers because they can trade them instantly. Streamers using vIRLs on WAX can sell much more merchandise faster, attract and engage more viewers, and ultimately make money at higher margins than they can with traditional e-commerce.

Secondary markets create revenue that didn't exist before. When an audience member sells an item again to someone else, the content creator or primary seller can earn another transaction fee from the seller. Never before could merchandise sellers make a share of the money when their products resell later because they never had an opportunity to participate directly in secondary
markets.

WAX gives game publishers a way to monetize their customers who usually don't buy or spend money in their games. While non-paying players in free-to-play games spend enormous amounts of time in the game, publishers can start to offer vIRLs through WAX. Similar to a [Supreme drop](https://www.supremecommunity.com/season/spring-summer2019/droplists/), limited amounts of merchandise are available to a select group of customers. For instance, imagine a Fortnite player who has a chance to buy a limited-edition Fortnite keyboard, mousepad, mobile phone case, sneakers, and hoodie after spending hours playing the game.

The brand affinity is high for players who then look for merchandise that reflects their interest. Different from an ad, this is a direct integrated shopping experience that can tie to game activity, promotions, or interact with streamers who create content related to the game. We believe this model, when proven through well-executed trials, will sweep through the entire video game industry to capture revenue from "non-performing" customers not spending money in their games. Currently, there are several game publishers currently working to roll out tests with WAX and vIRLs within their games.


<a id="markdown-the-dawn-of-blockchain-gaming" name="the-dawn-of-blockchain-gaming"></a>

### The Dawn of Blockchain Gaming
NFTs in blockchain games are not yet an extensive ecosystem in terms of the trading volume. However, there is significant interest and investment to create the next video game hit that uses blockchain technology.

We remain excited about new classes of games from talented independent game publishers that have customer-owned assets in them and encourage trading and creating scarcity in their items. These game publishers include, but not limited to, Animoca Brands, Pixowl, Mythical Games, and Neon District. We estimate that we are probably a year or more away from seeing a smash hit that embraces blockchain.

After it happens, the larger, older, more established game publishers will look to adopt it in their own way. In the meantime, we are working with smaller publishers with very dedicated audiences. The benefit of these audiences is that they are very loyal, and customer acquisition is easier because they are tightly-knit through influencer channels.


# Solution: The Value Proposition of WAX 
The WAX Platform solves a problem for businesses and entrepreneurs who want to make money and participate in the rapidly growing global digital goods market. The global digital goods market continues to expand because people's time and attention continue to go towards online forms of entertainment, such as video games, social media, movies, music, and digital books. Also, another 3+ billion people are expected to come online to the internet in the next five years.


# What is the W.A.S.P. Strategy
On the WAX Platform, the **W.A.S.P.** Strategy captures the power a dApp can access and quickly build to reach existing WAX customers while also making new ones. The WAX Platform consists of:

**W**AX Blockchain +

decentralized marketplace (similar to **A**mazon) +

decentralized virtual item trading and generation (similar to **S**team) +

decentralized wallets (similar to **P**ayPal)

The WAX Blockchain provides a token-based economy that operates on resources provided by the consumers of those resources. In that way, the ecosystem pays for itself, and the participants guide its development and benefit directly from its growth.

The WAX microservice layer delivers on all the functions that a well-designed marketplace needs to grow and scale without a massive investment in infrastructure.

We describe the entire WAX Platform, i.e., WAX Protocol Blockchain functions and the microservice layer in the next section.


# How the WAX Platform Works
With the combination of the WAX Protocol Blockchain and the microservices layer, the WAX Platform provides customers with a full suite of blockchain-based tools. WAX Platform is safe and convenient for creating, buying, selling, and trading virtual items to anyone, anywhere.


<a id="markdown-wax-protocol-blockchain" name="wax-protocol-blockchain"></a>

## WAX Protocol Blockchain 


<a id="markdown-consensus-model" name="consensus-model"></a>

### Consensus Model
WAX uses a [Delegated Proof of Stake (DPoS)](#delegated-proof-of-stake-dpos) consensus algorithm which relies upon a group of WAX Guilds (also known as block producers) to manage block production.


<a id="markdown-wax-token-model" name="wax-token-model"></a>

### WAX Token Model 
The WAX Token model is designed to drive several activities to grow the WAX ecosystem: staking, rewards, and voting.


<a id="markdown-wax-staking-rewards" name="wax-staking-rewards"></a>

#### WAX Staking Rewards
WAX Staking Rewards is the voting and rewards system we designed to increase community participation in the selection of guilds and blockchain improvement proposals. Here is what token holders can do with their WAX Tokens:

1.  **Stake WAX Tokens.** If token holders have unstaked WAX Tokens, they need to stake them using a Lynx, Sqrl, Scatter or another compatible wallet. [Genesis WAX Protocol Tokens](https://wax.io/blog/introducing-the-genesis-block-member-program-join-and-receive-daily-token-rewards-for-3-years) are automatically staked.

2.  **Vote via a compatible wallet.** If token holders have Genesis WAX Protocol Tokens in a WAX Blockchain account, they must connect their compatible wallet to the account to vote. All WAX Token holders can vote for up to 30 WAX Guilds. The strength of their vote for any particular guild depends on the number of WAX Tokens they stake.

3.  **Earn WAX Staking Rewards.** WAX Token holders who stake their tokens and then vote with them earn additional WAX Tokens. These earnings are called WAX Staking Rewards and are issued directly from the WAX Blockchain.

dApp developers also benefit from staking their WAX Tokens because it helps reserve system resources (CPU and Network). RAM allocation can be purchased and sold to meet the needs of the developer. The staking mechanism and WAX Staking Rewards combination make no-fee transactions possible. We don't charge dApp developers for running the infrastructure that enables the processing of transactions due to Guild Rewards. So by staking tokens, dApp developers claim the RAM allocation necessary. It also prevents network spam from locking out legitimate transactions because everyone is rate-limited, and based on their allocation.


<a id="markdown-what-functions-can-i-perform-by-staking-my-wax" name="what-functions-can-i-perform-by-staking-my-wax"></a>

#### What functions can I perform by staking my WAX?
Staking WAX Tokens allows token holders to vote on the WAX Blockchain, and earn WAX Staking Rewards for doing so. Token holders must vote weekly to maintain the strongest vote strength and earn maximum rewards (find more details on vote strength in the next section). There are three types of voting on WAX:

-   **Guild voting:** Stake a fixed amount of WAX Tokens to vote for guilds. For example, if staking 1,000 WAX Tokens, token holders may assign 1,000 votes each for up to 30 different guild candidates.

-   **Proxy voting:** Designate a proxy, who then votes on token holders’ behalf using their staked WAX, which earns them WAX Staking Rewards. If a proxy does not vote, it does not affect the token holder’s vote strength. However, they need to keep their proxied vote updated to retain full voting strength similar to guild voting.

-   **Worker Proposal voting (post-mainnet launch):** Stake WAX Tokens to vote for proposals that are put forth by other WAX Token holders.


<a id="markdown-how-do-i-earn-wax-staking-rewards-by-staking-my-wax-tokens" name="how-do-i-earn-wax-staking-rewards-by-staking-my-wax-tokens"></a>

#### How do I earn WAX Staking Rewards by staking my WAX Tokens?
Token holders can earn more WAX Tokens every day with WAX Staking Rewards just by voting. Each day, a set number of WAX Tokens get set aside for WAX Staking Rewards. The number of tokens each WAX Token holder receives daily depends on their stake weight, relative to other stakers. For example, if a token holder’s stake weight amounts to 0.5% of the aggregate stake weight on any given day, they receive 0.5% of the WAX Staking Rewards amount. The voter's current stake weight determines the amount of WAX Staking Rewards given to them.

![Voter's stake weight determines the amount of WAX Staking Rewards given to them](media/voters-stake-weight-calculation.png)

-   **Stake weight** is the number of WAX Tokens currently staked multiplied by vote strength.

-   **Vote strength** is a number between 0 and 1, for example, 0.08 or 0.25, with 1 being full strength. If a token holder votes weekly, then they maintain the highest possible vote strength. If they don’t vote weekly, their vote strength decays. Stake weight starts at and remains at 0 until they vote, at which point it increases to 1.

For example, if a token holder votes in any given week, their vote strength is then 1. If they do not vote again, then their vote strength decays until it reaches zero. They can increase it back to 1 just by voting.

![Voter strength](media/voter-strength.png)

Therefore, voting maximizes WAX Staking Rewards. Additionally, token holders contribute to the selection of quality guilds and proposals - supporting the overall health of the WAX Blockchain. We plan to introduce additional types of WAX Staking Rewards in the future.


<a id="markdown-wax-guilds-and-wax-guild-rewards" name="wax-guilds-and-wax-guild-rewards"></a>

#### WAX Guilds and WAX Guild Rewards
The WAX Blockchain has 21 WAX Guilds who earn rewards for producing blocks. These WAX Guild Rewards are granted based on the number of blocks produced by each WAX Guild. Standby Guilds, or reserve guilds, operate as "backup operators" that earn a share of WAX Guild Rewards for participating and demonstrating their ability to process a block when randomly requested.


<a id="markdown-wax-core-performance-metrics" name="wax-core-performance-metrics"></a>

### WAX Core Performance Metrics 
WAX produces a block precisely every 0.5 seconds, and one WAX Guild is authorized to produce a block at a time. If a block does not get produced at the scheduled time, the block for that time slot gets skipped. The transactions remain in the memory pool waiting for the next guild to include them. Similar blockchains have achieved 3,000 transactions per second, which exceed the average transactions per second that Visa processed by nearly 2x. WAX is capable of the same speed and as such, WAX is one of the fastest, potentially highest-throughput blockchains on the market.


<a id="markdown-delegated-proof-of-stake-dpos" name="delegated-proof-of-stake-dpos"></a>

### Delegated Proof of Stake (DPoS)
WAX utilizes the DPoS decentralized consensus algorithm to optimize the performance of applications on the blockchain. DPoS also optimizes the nominal condition of 100% participation of honest nodes with robust network connections. Incentives for WAX Guilds help keep them honest, which results in the trustworthiness of the network. Otherwise, the WAX Guild risks losing its position in the network and missing out on earning WAX Guild Rewards. 

DPoS is secure in the face of the corruption of a significant minority of producers. Token holders may select WAX Guilds through a continuous approval voting system. To get an opportunity to produce blocks, token holders can persuade other token holders to vote for them.

Every 0.5 seconds, blocks get produced on the WAX Blockchain, and one WAX Guild gets authorized to produce a block at any given point in time. If a block does not get produced at the scheduled time, the block for that time slot gets skipped. When one or more blocks get skipped, there is a 0.5 or more second gap in the blockchain. To decentivize skipping blocks, WAX Guilds don’t receive their WAX Guild Rewards if they produce 50% or less of their scheduled blocks.


<a id="markdown-byzantine-fault-tolerance" name="byzantine-fault-tolerance"></a>

### Byzantine Fault Tolerance
[Byzantine Fault Tolerance (BFT)](https://en.wikipedia.org/wiki/Byzantine_fault) is achieved by a rule that strongly discourages WAX Guilds from signing two blocks at the same block height or timestamp. Since a central authority does not control blockchains, the absence of BFT poses a risk of a peer transmitting and posting false transaction, nullifying the blockchain's reliability. Bottom line, BFTs guard against catastrophic failures and mitigate against the influence of these malicious nodes.

Any WAX Guild signing two blocks at the same block height or timestamp is likely voted out by the WAX Token holders. Fifteen guilds signing a block makes a block permanent and immutable.


<a id="markdown-guilds-block-producers-staking-and-voting---enhanced-governance-features" name="guilds-block-producers-staking-and-voting---enhanced-governance-features"></a>

### Guilds, Block Producers, Staking, and Voting - Enhanced Governance Features


<a id="markdown-wax-guilds" name="wax-guilds"></a>

#### WAX Guilds
The WAX Blockchain has 21 WAX Guilds at any given time, with one guild being selected to produce a block at a scheduled time. The 21 WAX Guilds are chosen to produce blocks in rounds of 126, based on six blocks for each of the 21 WAX Guilds. WAX Token holders vote for WAX Guilds to determine which qualified guilds become a part of the top 21. Those who vote for WAX Guilds that miss blocks are incentivized to vote these producers out since missed blocks result in a missed monetary opportunity for their voting constituents.



<a id="markdown-standby-guilds" name="standby-guilds"></a>

#### Standby Guilds
Standby guilds are critical to ensuring a robust network with maximum block production capacity. WAX allocates 1% of all blocks to be produced by standby guilds. These blocks get allocated in a pseudorandom manner to the standby guilds. Unlike EOS, where anyone can represent themselves as a standby block producer, WAX takes a different approach. In the WAX ecosystem, standby guilds are compelled to maintain 24/7 uptime since they cannot predict when they are assigned to produce a block. It also allows for voting on standby guild members.

We also recognized that EOS doesn't have a mechanism to determine if all producers qualify to produce blocks. For example, if a lower quality standby producer gets voted in, this producer may be unable to produce its assigned blocks, resulting in lower performance. This standby producer would still get paid a share of the block reward. EOS block producers and standby producers share 0.75% inflation based on the number of votes they receive. It's likely to give incentive for lower quality producers to promote themselves as a producer without having sufficient block producing capabilities.

To address this, the WAX Blockchain uses three mechanisms:

-   WAX standby guilds must prove their ability to produce blocks to be included in the pool of 57 qualified guilds (21 WAX Guilds + 36 standby guilds).

-   As with WAX Guilds, WAX standby guilds get penalized if they cannot produce at least 50% of the blocks assigned to them.

-   Because staking incentives get tied to guild performance, WAX Token holders are economically encouraged to direct their votes to higher performing WAX Guilds.


<a id="markdown-wax-staking-rewards-as-a-solution-for-voter-apathy" name="wax-staking-rewards-as-a-solution-for-voter-apathy"></a>

#### WAX Staking Rewards as a Solution for Voter Apathy
Voter apathy is a concern for DPoS blockchains because other DPoS blockchains have been adversely affected by lack of voting. Systemic low voting rates on a chain prevent achieving decentralization, for which the chain was designed. We developed WAX Staking Rewards to drive community interest in the voting process. WAX Token holders who stake their WAX Tokens and vote for WAX Guilds receive these staking rewards. These rewards get maximized when voting is done regularly and for the top-performing guilds.


<a id="markdown-wax-staking-rewards" name="wax-staking-rewards"></a>

#### WAX Staking Rewards
WAX Token holders who stake their tokens and then vote with them earn additional WAX Tokens, called WAX Staking Rewards. These rewards are issued directly from the WAX Blockchain.

These rewards are beneficial for dApp developers because it helps reserve their system resources (CPU and Network). RAM allocation can be purchased and sold to meet the needs of the dApp developer. The staking mechanism and WAX Staking Rewards combination make no-fee transactions possible. We don’t charge dApp developers for running the infrastructure that enables the processing of the transactions due to WAX Guild Rewards. By staking tokens, dApp developers claim their necessary allocation. Staking also prevents network spam from locking out legitimate transactions because everyone is rate-limited based on what they are allotted.


<a id="markdown-staking-rewards-are-based-on-performance--penalties-for-underperformance" name="staking-rewards-are-based-on-performance--penalties-for-underperformance"></a>

#### Staking Rewards are Based on Performance / Penalties for Underperformance
To encourage WAX Token holders to vote for the highest quality WAX Guilds to produce blocks, WAX Staking Rewards are tied to the performance of the WAX Guilds. If a WAX Guild that a WAX Token holder voted for is underperforming, their WAX Staking Rewards decrease:

![WAX Staking Rewards decrease](media/math3.jpg)


WAX Staking Rewards are scaled by the performance of the WAX Guilds voters vote for:

![WAX Staking Rewards are scaled by the performance of the WAX Guilds voters vote for](media/math2.jpg)


The function to determine a voter’s WAX Staking Rewards proportion:

![he function to determine a voter’s WAX Staking Rewards proportion](media/math1.jpg)


Therefore, if the token holder votes for the WAX Guilds that only produce 90% of blocks scheduled to them, the voter's WAX Staking Rewards are 90% of the minimum possible amount. If the voter votes for the WAX Guilds that produces 50% or less of blocks scheduled to them, the voter does not receive WAX Staking Rewards in exchange for voting for them. Also, these guilds that produce 50% or less of their scheduled blocks do not get paid their WAX Guild Rewards.

The formula applies to standby guilds as well. That means the vote cast for a standby guild receives the same potential reward as the vote cast for a guild that has become one of the top 21 (i.e., a WAX Guild). It makes the voter agnostic as to whether a guild that the voter votes for is likely (or not) to be one of the 21 WAX Guilds. We want WAX Token holders to cast their vote for the guild they believe best represents them, without being penalized.

A voter can proxy a vote to anyone voting for underperforming WAX Guilds. In that case, the WAX Staking Rewards for those voting for underperforming WAX Guilds get diminished because their rewards are calculated based on the WAX Guilds that end up getting selected. A proxy cannot refresh a voter's vote weight when its votes on the voter’s behalf. Instead, the voter must refresh its vote for the proxy it chooses to regain full vote weight capacity and full WAX Staking Rewards capacity.



<a id="markdown-genesis-block-member-rewards" name="genesis-block-member-rewards"></a>

### Genesis Block Member Rewards
As part of the WAX Token Swap, we created the **Genesis Block Member** (GBM) program. Broad community participation is essential for a well-functioning delegated proof of stake blockchain. The GBM program is designed to encourage civic engagement and reward our long-term-oriented WAX community members who take part in the WAX blockchain’s healthy development.

To incentivize token holders in keeping their tokens invested with WAX, we have developed the Genesis Block Member Rewards Program. GBM participants receive daily token rewards for 3 years (July 1, 2019, to July 1, 2022). WAX Tokens earned from the WAX Token Swap, WAX Guild Rewards, and WAX Staking Rewards are all eligible for the GBM tokens.

-   Genesis WAX Protocol Tokens continue to produce WAX Protocol Token GBM rewards every day as long as they remain staked.

-   By leaving Genesis WAX Protocol Tokens staked uninterrupted for 3 years, WAX Token holders double their WAX Protocol Tokens. If a WAX Token Holder ceases staking its WAX Tokens before three years have elapsed, then rewards are prorated.

-   If a Genesis WAX Protocol Token is unstaked, it permanently stops producing WAX Protocol Token GBM rewards. When this happens, it cannot be undone.

-   A WAX Token holder may unstake all or a portion of its Genesis WAX Protocol Tokens at any time. The unstaked tokens become WAX Protocol Tokens and permanently stop producing daily GBM rewards.

-   The GBM rewards get burned instead of earned, creating a deflationary effect on the token supply as indicated below.


<a id="markdown-deflation--inflation" name="deflation--inflation"></a>

### Deflation / Inflation
Due to the GBM program described above, there is a 50% deflation potential from the WAX Token Swap, as detailed in the following chart:

| Token Description                        | Initial Token Supply |
|------------------------------------------|----------------------|
| Number of ERC-20 WAX Tokens              | 1.85 billion         |
| System resources                         | 200,000,000          |
| Pre-minted GBM Tokens for WAX Token Swap | 1.85 billion         |
| Max. total supply (excluding inflation)  | 3.72 billion         |
| Min. total supply (excluding inflation)  | 1.87 billion         |
| Total potential deflation %              | 50%                  |

> **Note:** Future GBM unearned rewards from unstaking WAX Token holders get burned, on a proportionate basis, when WAX Token holders unstake their GBM tokens.

At the same time, there is an inflation model from Token Rewards, as detailed in the following chart:

![Inflation Model Token Rewards](media/inflation-model-token-rewards.png)



<a id="markdown-transactions" name="transactions"></a>

### Transactions
For e-commerce to work, transactions must be free to prevent bottlenecks that would otherwise occur due to fee markups during times of token price inflation and increased volume. With free transactions, however, spam becomes a problem. To prevent spam on the WAX Blockchain, transaction senders must stake system resources required to process the transaction. The system resources to stake are NET (network), CPU, and RAM. By staking WAX for CPU and NET (bandwidth), a user gets a proportionate share of the overall blockchain resources, which guarantees that transactions get processed at a corresponding rate.

In a recent upgrade, staking system resources to have a transaction processed has moved from the sender to another party, for example, a dApp maintainer. Doing this facilitates onboarding users into the system because the users don't need to understand staking for resources. Depending on the transaction, a customer may require ownership of a certain amount of RAM. In this case, the customer can purchase more RAM from a WAX Blockchain-powered marketplace that exchanges WAX for RAM according to the Bancor algorithm.



<a id="markdown-providing-cost-efficiency-in-terms-of-fee-elimination" name="providing-cost-efficiency-in-terms-of-fee-elimination"></a>

#### Providing Cost Efficiency in Terms of Fee Elimination
WAX offers a free, flexible platform for sending transactions where customers don’t pay for transactions. The idea behind this more straightforward usage policy is to create a higher rate of adoption. It’s also possible for organizations, businesses, and developers to create a wide range of monetization strategies.



<a id="markdown-smart-contracts--rng" name="smart-contracts--rng"></a>

### Smart Contracts + RNG
Contracts in business are meant to ensure an agreement between the parties for a specific service or to meet a set of standard requirements. Contracts are a set of conditions or rules to be adhered to by both parties. As long as these requirements get met, execution is possible.

WAX Smart Contracts are similar in that they provide a structure for obligations between all participants to process financial transactions on the WAX Blockchain. WAX Smart Contracts get executed when the set of conditions, or rules, get met, but the records for legal transfer and activity get stored on the WAX Blockchain with transparency.

WAX Smart Contracts reside on a WAX Account and have a 12-character, human-readable label chosen by the creator of the account. Within the WAX ecosystem, any account can send actions to other accounts where the transaction gets handled by the smart contract code residing on the target account. Multiple accounts can receive multiple actions for a single transaction.

WAX Smart Contracts define:

-   obligations

-   parameters

-   required actions

-   information structure

-   interface code



<a id="markdown-wax-random-number-generator-rng-smart-contract" name="wax-random-number-generator-rng-smart-contract"></a>

#### WAX Random Number Generator (RNG) Smart Contract
In generic terms, a [random number generator (RNG)](https://en.wikipedia.org/wiki/Random_number_generation) is an algorithm that generates random values. In blockchain terms, dApp developers use RNGs to introduce a random outcome, such as generating a digital collectible or NFT. Currently, integrating random values into smart contracts has process flaws, which create potential vectors for unfair, or non-random values, reducing a customer's confidence in using dApps.

The **three** main problems that developers experience when trying to generate and ingest random values into their dApps include:

1.  Blockchain-native RNG services don’t exist, leaving dApp developers to build their own. This reduces the time the dApp developers can spend on other areas of their dApps, such as designs and features that would improve the customer experience.

2.  It's not uncommon that most dApp developers are not experts with the RNG, so there are design weaknesses with most dApp-specific RNG services. 

3.  Sometimes dApp customers have difficulty determining whether a dApp's RNG service is generating a random result or not, which diminishes customer confidence.


<a id="markdown-how-wax-rng-native-blockchain-service-solves-important-problems" name="how-wax-rng-native-blockchain-service-solves-important-problems"></a>

#### How WAX RNG Native Blockchain Service Solves Important Problems
The open-source WAX RNG Native Blockchain Service allows dApp developers to integrate the service into their dApps easily. We chose [Signidice algorithm](https://github.com/gluk256/misc/blob/master/rng4ethereum/signidice.md) and [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)) verification for this service because:

-   **Signidice algorithm:** Excellent randomization, non-gameable characteristics, cleaner workflow for dApp developers, and provably fair.

-   **RSA verification:** Ensures uniqueness of the signature and removes the ability for the results to be manipulated. Note, using other types of signing algorithms may allow many valid signatures for the same signing value, which could result in manipulation.

The self-verifying WAX RNG Native Blockchain Service confirms that the RSA signature that comes back from the WAX RNG oracle is valid and authentic before being utilized by the dApp. When dApp customers can quickly establish fairness, they have a higher degree of confidence in using the dApp.


<a id="markdown-nft-standards--nft-integration-with-wax-expresstrade" name="nft-standards--nft-integration-with-wax-expresstrade"></a>

## NFT Standards / NFT Integration with WAX ExpressTrade
WAX supports non-fungible tokens using the [Simple Assets](https://github.com/CryptoLions/SimpleAssets) open-source standard. WAX ExpressTrade leverages the WAX Blockchain via a microservice called WAX-On to generate, mint, and store the NFTs it manages. With this, we have the WAX-On microservice:

1.  All users see their transactions on the chain.

2.  Customers can prove to themselves that they have been chosen for random selections fairly.

3.  dApp developers have access to a large user base of OPSkins customers.

4.  The service leverages open-source Simple Assets NFT implementation.

Full integration with other NFT standards such as dGoods on EOS, Ethereum, and Tron is part of the roadmap. Interoperability maximizes the liquidity for buyers and sellers and is the essential value proposition of the WAX Protocol.


<a id="markdown-worker-proposal-system" name="worker-proposal-system"></a>

## Worker Proposal System 
The WAX Worker Proposal System (WWPS) is a proposed program that’s designed to incentivize and compensate community developers who build upon the WAX Blockchain. The WWPS would allocate WAX Tokens (denominated in WAX Tokens and paid in WAX Tokens) to be distributed to developers who work on community needs, patches, and upgrades. In exchange for their time and effort contributing to the development of WAX, these developers would become eligible to receive WAX Tokens from the WWPS.

One percent (1%) WAX annual inflation would fund the WWPS and would not be eligible for GBM Rewards, to encourage the active distribution of the funds to developers.


<a id="markdown-why-do-we-need-the-wwps" name="why-do-we-need-the-wwps"></a>

### Why do we need the WWPS?
WAX has several improvements to be made, and some desired features are still missing. In the decentralized nature of blockchains, there are not enough incentives for community developers to spend their time contributing patches and upgrades needed for efficient and scalable advancements.

To make sure WAX remains up-to-date with the changing needs of the community, we will soon introduce a Work Proposal System (WPS). The planned WPS will allow for an allocation of funds to reserve for incentivizing developers to work on the community needs, such as critical patches or forward-looking upgrades. The idea behind WPS is to utilize the strengths of a decentralized community going forward, reducing the reliance on a single source for new additions. The WPS also would allow the community to nurture and grow the tool.


<a id="markdown-proposed-wwps-categories" name="proposed-wwps-categories"></a>

### Proposed WWPS Categories
1.  **Oversight:** Supports the underlying code base of the blockchain, which includes security audits, Distributed Denial of Service (DDoS) protection, bug patches, and mainnet repository maintenance.

2.  **Infrastructure:** Supports the underlying code base of the blockchain, which includes security audits, Distributed denial of service (DDoS) protection, bug patches, and mainnet repository maintenance.

3.  **Community:** Supports the resources and spaces that bring people together, such as meetups, educational content and platforms, public relations, lawyers, advocates, and lobbyists.

4.  **Development:** Supports developers and ideas, such as dApps and applications that may be necessary for underserved minorities.

5.  **Miscellaneous:** Supports swag, burning, and projects that may not fit into other categories.

A percentage of the WWPS funds would be allocated to each category, ensuring that no category would have an oversized impact on the WPS. The fund, however, would require oversight to screen out non-legitimate proposals and possible abuse.


<a id="markdown-net-cpu-and-ram-resources-on-the-wax-blockchain" name="net-cpu-and-ram-resources-on-the-wax-blockchain"></a>

## NET, CPU, and RAM Resources on the WAX Blockchain
Since the WAX Blockchain mainnet and protocol token launched, we’ve been thrilled to see the level of participation in staking and voting among WAX Token holders who have [swapped](http://tokenswap.wax.io/) their tokens. As we’ve [mentioned](https://wax.io/blog/earn-more-wax-introducing-wax-block-rewards-staking-and-voting-guilds-and-more), staking and voting is crucial for DPoS blockchains such as WAX because the more involved the community, the better the blockchain operates for everyone. Now we’d like to explain what the NET (Network), CPU, and RAM is that the community is staking.

In the WAX ecosystem, the following resources get consumed by dApps:

-   **NET** - throughput capacity of the WAX network, measured in bytes

-   **CPU** - processing time of an action, measured in microseconds

-   **RAM** - stores data of dApps in the blockchain

In this ecosystem, *bandwidth,* which consists of NET and CPU, is flexible. That means WAX Token holders can have more bandwidth allocated than the ratio they have staked vs. the total stake pool. Minimum resource allocation is the fraction: 'your stake' divided by 'total stake.' Bandwidth is consumed at the block height that a transaction is included and then regenerates for future usage.

Since RAM is limited and necessary to hold a dApp's state, which must persist over time, RAM must be allocated. Therefore, RAM is not based on staking; rather, it is purchased and sold. Realize that one can sell deallocated RAM at any time back to the blockchain's native RAM market, or allocate it for usage at any future point in time.

More information about NET, CPU and RAM on the WAX Blockchain can be found here:
[https://wax.io/blog/what-is-net-cpu-and-ram-on-the-wax-blockchain](https://wax.io/blog/what-is-net-cpu-and-ram-on-the-wax-blockchain)


<a id="markdown-microservice-layer" name="microservice-layer"></a>

## Microservice Layer
The WAX Service Layer is a full suite of blockchain-based tools and services that allow the community to build projects on WAX. From dApps developers to marketplace owners, video game creators, collectible traders and more, the following microservices are available:

-   **WAX All Access:** A single sign-on (SSO) and OAuth service.

-   **WAX Account (soon WAX Wallet):** Similar to a wallet, except that it doesn’t store private keys, and provides more utility than a standard wallet. WAX Wallet, the next iteration of the WAX Account, is coming soon and will offer more features. Details to follow.

-   **WAX NFT Creator:** A self-service tool that allows anyone to create a NFT on the WAX Blockchain for free.

-   **WAX ExpressTrade:** A free, instant peer-to-peer trading service.

-   **WAX Explorer:** Unlike any block explorer, featuring a user-friendly design, a visual representation of every item traded, and multiple 3D viewing and interactive features.

-   **WAX Marketplace:** Create a WAX Marketplace with our APIs.



<a id="markdown-wax-all-access" name="wax-all-access"></a>

### WAX All Access
WAX All Access simplifies the login process because it allows access to any WAX-powered site by logging in with Facebook, Google, Wechat, Steam, or a WAX All Access username and password. The SSO and OAuth services let account holders link these other accounts to their WAX Blockchain account for easier access to their WAX account. To create an account, visit [all-access.wax.io](all-access.wax.io).

Only specific permissions are received from these third parties and do not involve WAX Blockchain account information.



<a id="markdown-wax-account-soon-wax-wallet" name="wax-account-soon-wax-wallet"></a>

### WAX Account (soon WAX Wallet) 
A WAX Account is similar to a wallet, except that it doesn’t store private keys. WAX Account provides more utility than a standard wallet because it can view many kinds of non-fungible assets as well as integrate with functions like vote and staking.

WAX Account will soon be WAX Wallet. More features about WAX Wallet will be available in the near future.

WAX Account Token holders can perform the following activities directly from their WAX Account.

-   **Swap** ERC-20 WAX Tokens for [Genesis WAX Protocol Tokens](https://wax.io/blog/introducing-the-genesis-block-member-program-join-and-receive-daily-token-rewards-for-3-years)

-   **Stake** any WAX Protocol Tokens acquired or earned through [Staking Rewards](https://wax.io/blog/earn-more-wax-introducing-wax-block-rewards-staking-and-voting-guilds-and-more) and Genesis Block Member Rewards using Scatter wallet

-   **[Vote](https://wax.io/blog/earn-more-wax-introducing-wax-block-rewards-staking-and-voting-guilds-and-more)** with WAX Protocol Tokens

-   **Claim** Staking Rewards and Genesis Block Member Rewards

-   **Track** WAX Token balances and Staking Rewards

-   **View** NFTs

WAX Accounts can be made at [accounts.wax.io](http://accounts.wax.io).

WAX Accounts are free for customers. An existing WAX Blockchain account must generate WAX Accounts. Each WAX Account requires 3KB of RAM and a minimal amount of WAX (\~1 WAX) to provide bandwidth for CPU and NET system resources, which WAX covers the cost of for most accounts.

By requiring 2FA and account scoring, WAX prevents account creation spam.



<a id="markdown-wax-nft-creator" name="wax-nft-creator"></a>

### WAX NFT Creator
WAX Creator is a self-service tool that allows anyone to create NFTs like collectible cards, stickers, and digital art on the WAX Blockchain in just minutes, and for free. It requires zero technical knowledge on the part of the creator. Hundreds of thousands of NFTs have been created on the WAX Blockchain using the WAX Creator since launching in June 2019.

NFTs are minted on the WAX Blockchain and sent to the creator’s WAX ExpressTrade Inventory. Owners of these NFTs can sell them, gift them, trade them, or collect them. They can also be used to create dApps, such as a card game that’s played using custom WAX Collectable Cards.

NFTs can have generic attributes, unique attributes including random integers, descriptions, and more.


<a id="markdown-wax-expresstrade" name="wax-expresstrade"></a>

### WAX ExpressTrade
WAX ExpressTrade enhances the experience for a rapidly growing global community of digital item buyers, sellers, and collectors. This free and instant peer-to-peer service lets digital item traders buy, sell, and trade digital items on the WAX Blockchain.

The WAX ExpressTrade API gives independent marketplaces a pipeline into the multi-billion dollar digital item trading industry. Marketplaces of any size and in any geography can use WAX ExpressTrade to create a thriving market for their digital items like video game skins and other tradable items, or physical items like electronics or sneakers. WAX ExpressTrade provides  marketplaces a way to give their customers access to the global WAX item trading market; and not just the limited inventory available in their marketplace. Buyers can find those coveted rare items easier, and sellers can match with suitable customers faster.


<a id="markdown-wax-explorer" name="wax-explorer"></a>

### WAX Explorer
The WAX Explorer is unlike any that the blockchain world has seen before.

Most block explorers were originally designed for commodity-style, fungible tokens like Bitcoin and Litecoin. They exist to simply provide relevant information about the tokens being traded. For generic tokens like BTC and LTC, the information anyone is interested in tracking is pretty limited to just metadata - what block the transaction is in, the milliseconds it took, the address it was sent to, etc.

But WAX is a different type of blockchain, and the products that are traded on it are very different from what’s viewed on other block explorers. As we usher in the new era of consumer-friendly mass adoption of blockchain technology, we saw that it was necessary to invent a new type of block explorer that was different from everything else out there. If the types of items that are trading on the beta WAX Blockchain are different from the items trading on other blockchains, then it’s logical that the WAX Explorer should be different as well.

Like other block explorers for other chains, the WAX Explorer shows details for all transactions taking place on the beta WAX Blockchain and other important data. But that’s where the similarities to other block explorers end. We’ve completely re-imagined what a block explorer should do and look like with the WAX Explorer.

The difference between seeing Ethereum traded on Etherscan versus VGO skins traded on the WAX Explorer is that ETH transactions are just a string of characters whereas non-fungible tokens (NFTs) like VGO and CryptoKitties are all completely unique from one another. They’re unique collectibles and therefore e-commerce products, not store-of-value commodities like other tokens. For this reason, a block explorer that shows transactions of these NFTs must include merchandising data relevant to someone searching for and trading them. That’s what we built with the WAX Explorer.

The appearance of the items traded on WAX is extremely important to traders of them. WAX Stickers and WAX Digital Art are custom designed by their creators. Features like the wear value on a VGO skin can significantly affect the price. So why hide these visuals behind an ugly stream of letters and numbers, when customers want to see the items that they’re trading?

Designing the WAX Explorer in the same way that block explorers were designed for commodity-style token trading would be like Amazon having just SKU numbers and weight information for its products instead of photos and videos showing shoppers what the product looks like.

In addition to showing the visuals for all items traded on WAX, we also included a 360 degree rotating animation for WAX Stickers and VGO items, and the WAX 3D Item Viewer Service that allows anyone to click and drag on the item to view it
at any angle (not all VGO items have the 3D Item Viewer Service enabled now, but all eventually will).

The WAX Explorer also shows relevant information outside of traditional block explorer data like the description and creator of WAX Stickers or WAX Digital Art, or which vCase the item came from, because that matters to the consumers of these items who are buying products - not commodities.

Our overall goal was to make the WAX Explorer as user-friendly as possible. If the blockchain community’s goals is mass adoption of blockchain technology among general consumers, then block explorers - and blockchain-based products overall - shouldn’t be designed so that only blockchain-savvy people can easily use and understand. People should be able to use a blockchain-based service like the WAX Explorer without realizing they’re interacting with the blockchain. Consumers shouldn’t have to actively think about using the blockchain when searching for an item’s sale history in the same way they don't have to actively think about using the internet when asking Google Home to turn up the volume on Pandora. NFT traders should be able to easily view the items that they're trading or interested in trading, see the price of the items in USD instead of calculating crypto, and use all of the visual features on the block explorer that exist on other sites.


<a id="markdown-wax-marketplace" name="wax-marketplace"></a>

### WAX Marketplace
WAX supports a growing ecosystem of marketplaces. With WAX Marketplace, third-parties can list, purchase, and settle the transaction all through a smart contract. Anyone can operate a fully functioning virtual marketplace with blockchain trust and transaction verification.

# WAX Technical Documentation
In the [WAX Technical Documentation on GitHub](https://github.com/worldwide-asset-exchange), developers can find information about the WAX Blockchain, WAX System Contracts, WAX RNG, and WAX Contract Development Toolkit. Soon, developer-specific technical documentation will be available, called the WAX Developer Hive, that developers can use to build projects using the WAX suite of microservices. These tools include services to support e-commerce operations, such as:

-   Interactive block explorer

-   Wallet

-   SSO and OAuth

-   Item creation

-   RNG service

-   Interactive item viewers

-   Marketplace creation


# WAX Projects Showcase
For the past 12 months, hundreds of sites have built dApps integrating WAX microservices. Their feedback has been immensely useful to help refine the microservice platform. Here, in this section, we cover a select group of dApps and other projects that utilize the WAX Platform in whole or in part.


<a id="markdown-marketplaces" name="marketplaces"></a>

## Marketplaces


<a id="markdown-opskins" name="opskins"></a>

### [OPSkins](https://opskins.com/)
OPSkins is one of the world’s largest and most successful digital items trading marketplaces and is powered by WAX. Millions of customers use OPSkins, totaling hundreds of millions of transactions since 2015. OPSkins features WAX All Access, WAX ExpressTrade, WAX Seller Central, and more.


<a id="markdown-waxpeer" name="waxpeer"></a>

### [WAXPeer](https://waxpeer.com/)
WAXPeer is a peer-to-peer CS:GO skins marketplace.



<a id="markdown-waxtrades" name="waxtrades"></a>

### [WAXTrades](https://waxtrades.com/)
Customers use this marketplace for buying, selling, and trading VGO or vIRL items with many different payment methods.



<a id="markdown-dcart" name="dcart"></a>

### [dCart](https://dcart.io/)
dCart is a decentralized ecommerce platform for digital assets trading, built on
Blockchain technology.



<a id="markdown-bynogame" name="bynogame"></a>

### [ByNoGame](https://www.bynogame.com/en) 
ByNoGame is a marketplace serving Turkey and the Middle East. They implemented WAX ExpressTrade in 2018 and have continued to expand their usage of [WAX keys and VGO](https://www.bynogame.com/skin/vgo/wax-key).


<a id="markdown-collectibles" name="collectibles"></a>

## Collectibles

<a id="markdown-virl" name="virl"></a>

### [vIRL](https://govirl.io/)
To make a digital twin of a physical item and tokenizing is a novel idea. Like the stable coin Tether, imagine a token backed by a real-world object, such as a pair of high-end collectible sneakers. vIRL demonstrated by launching its dApp in November 2018, to immediate commercial success. Tens of millions of vIRLs have been created - all trading on the WAX Blockchain.



<a id="markdown-vgo" name="vgo"></a>

### [VGO](https://vgo.gg/) 
VGO is blockchain-based items, designed for collecting and trading. VGO items are designed to mimic the trading experience of popular games but without onerous trading restrictions.



<a id="markdown-fnatic" name="fnatic"></a>

### [Fnatic](https://www.fnatic.com/)
WAX and Fnatic, one of the world’s leading global eSports brands, partnered to gift authentic digital collectibles and branded physical merchandise to global eSports fans in real-time. Fans can sell, swap, store and gift limited-edition items on their [WAX ExpressTrade account](https://wax.io/expresstrade/) - instantly and for free. That means that for the first time, eSports fans can acquire branded physical merchandise from a team and its players, then trade those items with anyone else in the world without ever having to take physical ownership of it.


<a id="markdown-augmented-reality" name="augmented-reality"></a>

### Augmented Reality 
[RTFKT](https://www.rtfkt.net/), the world’s first Augmented Reality (AR) e-commerce inspired by two of the most popular consumer trends – streetwear fashion and video gaming. Blending the obsession of sneaker collecting with designs and attributes inspired by skin drops in video games.

At E3 2019, WAX demonstrated AR e-commerce with the custom shoe brand, RTFKT, on Snapchat with members of the FaZe Clan team. The demo showed how virtual items purchased in AR could link to physical items on the WAX Blockchain for redeeming for the physical version in just a few clicks. See a demo here:

[https://www.youtube.com/watch?v=YZSDpQcJlXg&feature=youtu.be](https://www.youtube.com/watch?v=YZSDpQcJlXg&feature=youtu.be)



<a id="markdown-terra-virtua" name="terra-virtua"></a>

### [Terra Virtua](https://terravirtua.io/)
Owners of the millions of [VGO skins](https://wax.io/blog/vgo-items-will-trade-on-the-wax-blockchain) trading on the WAX Blockchain can interact with their digital items in augmented reality [Terra Virtua](https://terravirtua.io/), the immersive AR/VR platform for collectibles and a [WAX partner](https://wax.io/blog/wax-x-terra-virtua-a-new-partnership), has released its [AR app for Android devices](https://play.google.com/store/apps/details?id=com.bim.terravirtua&hl=en_US) featuring WAX integration. See a demo of VGO skins in AR here:

[https://www.youtube.com/watch?v=uH9fu5eNICk](https://www.youtube.com/watch?v=uH9fu5eNICk)


App users can [download the Terra Virtua app](https://play.google.com/store/apps/details?id=com.bim.terravirtua&hl=en_US) on the Google Play store, then login with WAX. Terra Virtua will read its WAX ExpressTrade inventory and let the users select which VGO skins to interact with. The iOS app is coming soon, in addition to the virtual reality Terra Virtua app and vIRL integration.



<a id="markdown-e-commerce" name="e-commerce"></a>

## E-commerce

<a id="markdown-fan-controlled-football-league-fcfl" name="fan-controlled-football-league-fcfl"></a>

### [Fan Controlled Football League (FCFL)](https://www.fcfl.io/)
FCFL is the first league to let the fans call the shots, like real-life Madden. Fans can watch all FCFL games live-streamed on Twitch. The FCFL is the first professional sports league built on top of the Twitch platform. 

The partnership between WAX and FCFL pushes the envelope for what's possible with merchandise through the virtualization of each piece of FCFL merch. Buyers receive their FCFL merchandise virtually in the form of vIRL, the dApp that virtualizes physical items. They can also redeem the vIRL for the physical version whenever they want and have it shipped to their address.

WAX and FCFL celebrated the addition of Mike Tyson to the league by giving away memorabilia autographed by the legendary boxer.


<a id="markdown-games" name="games"></a>

## Games


<a id="markdown-z1br" name="z1br"></a>

### [Z1BR](https://store.steampowered.com/app/433850/Z1_Battle_Royale/)
Z1 Battle Royale (Z1BR) recently released limited-edition skins on WAX to commemorate the historic relaunch of H1Z1, the battle royale favorite that paved the way for titles like Fortnite and PUBG.



<a id="markdown-the-godfather-game" name="the-godfather-game"></a>

### [The Godfather Game](https://play.google.com/store/apps/details?id=com.dipan.feelingtouch.godfather&hl=en_US)
The hit mobile game The Godfather Family Dynasty gave away tens of thousands of in-game currency on WAX. As with other in-game items, Godfather Gold can be traded on WAX ExpressTrade for anything that trades on the WAX Blockchain, instantly and for free. It can also be sold on OPSkins Marketplace or stored in the owner’s WAX Inventory.



<a id="markdown-animoca-brands" name="animoca-brands"></a>

### [Animoca Brands](https://www.animocabrands.com/)
The WAX and Animoca Brands partnership drive market adoption of blockchain-based collectible digital items on a well-established platform for global digital commerce. As part of the partnership, Pixowl, a game studio recently acquired by Animoca Brands, allows NFTs created on its platform to be bought, traded, and sold on the WAX Marketplace. This provides additional visibility and liquidity for its creators.


<a id="markdown-santeria" name="santeria"></a>

### [Santeria](https://santeriagame.com/)
Santeria is a fantasy "mini" MMO game where players can explore different locations ranging from castles to wizard towers, fighting arenas, and barns. This game integrates WAX ExpressTrade and allows players to enhance their gameplay experience by purchasing NFTs on OPSkins and using them in the game. Players are automatically equipped with a Magic Hat and Wand, and upgraded equipment in the form of NFTs includes Wizard Staffs and more. 



<a id="markdown-waxwiki" name="waxwiki"></a>

### [WAX.Wiki](https://www.wax.wiki/home/)
WAX.Wiki a simple website design created using WAX Creator that lets anyone play games, watch videos, complete surveys, and more to earn collectible cards, stickers, and digital art. These collectibles get stored in their WAX ExpressTrade inventory.


There are an additional 100+ sites using WAX ExpressTrade, WAX All Access, WAX Creator and other microservices. 


# WAX Roadmap
For the look ahead, we have some crucial developments planned not already mentioned above:


<a id="markdown-wax-developer-hive" name="wax-developer-hive"></a>

## WAX Developer Hive
WAX Developer Hive will provide an overview of our technical services along with explanations, examples, tutorials. The WAX Developer Hive also offers other resources to ease implementation on the WAX Platform.


<a id="markdown-office-of-the-inspector-general" name="office-of-the-inspector-general"></a>

## Office of the Inspector General
Office of the Inspector General will provide ongoing transparency for the community in voting by evaluating the contribution of guild candidates to the WAX community.


<a id="markdown-ethereum-microservice" name="ethereum-microservice"></a>

## Ethereum Microservice
Interoperability with other chains for NFTs and other services requires microservices that can interact with the WAX Platform. That allows WAX to work with Ethereum-based NFTs. In the future, we plan to integrate with other popular chains.


<a id="markdown-public-wax-testnet" name="public-wax-testnet"></a>

## Public WAX Testnet
WAX plans to enable a public WAX testnet so that dApps can build their applications safely before launching on the mainnet.
