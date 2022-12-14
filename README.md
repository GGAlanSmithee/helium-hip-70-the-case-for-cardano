# Helium HIP 70 - The case for Cardano

Based on [this medium post](https://medium.com/helium-foundation/hip-70-evaluating-layer-1-blockchains-for-the-helium-network-15f81af6941c), which makes the case for Solana, I will address the same points to make the case for Cardano as Heliums L1. For some reason, Cardano was not in the comparison table of the linked article, which makes it seem like it was not considered by the Helium team as an alternative.

## TLDR

Cardano is an organically decentralized eco system with a large collection of single stake pool operators and a high Nakamoto Coefficient. It's predictably reliable and performant, with a clear roadmap for further decentralization with the upcoming Voltaire hard fork, as well as scaling solutions, Hydra, that will put the TPS far beyond the needs of Helium. Cardano has a strong developer community and a fast evolving developer tooling eco system. Continue reading to see why Cardano is a great choice for Helium as a L1.

## Compatible Wallet Cryptography

Cardano supports Ed25519 signatures, which is the same as Heliums wallet cryptography. This should make it easy to move helium wallets to Cardano. If there are any further need for additional crypto primitives, IOG has shown to be willing to add them, as is the case with secp, which was requested by the community for easier cross-chain integration. 

* https://iohk.io/en/blog/posts/2022/11/03/what-is-secp-and-how-it-drives-cross-chain-development-on-cardano/

## Credible Scalability Plan

Cardano recently released a new version of their chain, in a so-called hard fork combinator event (which allows the chain to continue to be fully operational while upgrading). This version, called Vasil, considerably increased performance and scalability of the chain. Many projects and dexes reported a hugh decrease in transaction size, and an equally large decrease in transaction settlement times.

More than this, Cardano has a clear scalability plan for the future, starting with their L2 scaling solution Hydra. Read more about this under the [High Transaction Throughput](#high-transaction-throughput) section.

* https://iohk.io/en/blog/posts/2022/07/04/cardano-s-approaching-vasil-upgrade-what-to-expect/

## DeFi Ecosystem

While Cardano has a relatively small DeFi eco system, and a comparatively low TVL, this is changing at a fast paste. Many dexes has released over the last year, using both AMMs, traditional order book models, yield farms and more. Below is a list of a few of them.

* https://muesliswap.com/
* https://minswap.org/
* https://sundaeswap.finance/

On top of this, because of Cardano's native token concept, there are a lot of NFT projects, NFT market places, and a handful of promising metaverse projects.

* https://www.jpg.store/
* https://www.cardanocube.io/collections/metaverse

## Transaction Cost

Cardano has a fixed base transaction cost for transactions and certain simple script executions (up to 340 Bytes), which is 0.17 ADA, or at the time of writing $0.06 per transaction. Helium has a $0.35 transaction cost, but they are able to handle a lot of transactions 'internally', without a fee at all, which Cardano, and AFAIK other L1 solutions, aren't able to.

When interacting with a smart contract, you have to pay a cost for CPU and memory depending on the complexity and size of the contract.

With Cardano, you can also send many different tokens in one transaction, making it very cost effective. For example, on Cardano, you could send 100 assets to different addresses in one transaction, for the same cost as sending one asset to one address on Helium. This is impossible on Solana, which makes the comparison unfair.

* https://cardano.stackexchange.com/a/6167
* https://www.binance.com/en/news/top/7082501
* https://iohk.io/en/blog/posts/2022/01/21/plutus-fee-estimator-find-out-the-cost-of-transacting-on-cardano/


## High Transaction Throughput

For the moment, Cardano is capped at 7 TPS (remember that you can send multiple assets to multiple addresses in one transaction). This is based on a blockchain parameter, `maxBlockSize`, which is currently set to 65536 bytes. One transaction is around 450 bytes, which means that a block can contain around 145 transactions. One block is processed every 20 seconds, making the TPS around 7. 

In a randomly selected epoch - five day period - during late 2022, Cardano processed 363,843 transactions over 432,000 "slots" making the effective TPS 0.84. This shows that there are plenty of room with current block parameters. Should there be a need for it, `maxBlockSize` can easily be increased to a low estimate of 50 TPS. To mitigate block size related centralization, Cardano is working on a technology called Mithril, which will make bootstrapping easier, and make it possible to run lightweight full nodes, even in hot wallets. Also, take into account that this was during the depths of a bear market, and that the number of transactions will increase as the price of ADA and market sentiment increases.

Here is a realistic Cardano block capacity example

![cardano block capacity example](cardano-block-capacity-example.png)

However, with the recent rollout and ongoing adoption of Vasil, the theoretical number is probably a lot higher since it added reference inputs which can reduce the size of a transaction by up to 90%. As a case study, Indigo - an advanced defi application dealing with synthetic assets and LP pools - are able to represent complex transactions in a 1kB transaction, probably using a combination of Vasil features and Plutarch, a "typed eDSL in Haskell for writing efficient Plutus Core validators".

_Another potential upgrade to Ouroboros, Cardano's proof-of-stake protocol, is Leios which aims to optimize the current implementations under-utilization of validator nodes CPU and bandwidth usage. See the linked documents regarding it below for details._

* https://www.quora.com/How-many-transactions-per-second-TPS-can-Cardano-do-and-what-does-this-mean-for-the-network
* https://explorer.cardano.org/en/epoch?number=374
* https://twitter.com/SundaeSwap/status/1580969361892085762
* https://docs.cardano.org/development-guidelines/scalability-solutions/mithril
* https://twitter.com/matiwinnetou/status/1596636514133413888
* https://github.com/Plutonomicon/plutarch-plutus
* https://indigoprotocol.io/
* [Leios PR](https://github.com/cardano-foundation/CIPs/pull/379)
* https://github.com/cardano-foundation/CIPs/blob/ouroboros-leios/CIP-XXXX/leios-design.pdf

### L2 Scaling Solutions

_Even though, this is outside of the scope of the comparison, it might be interesting to know that the Cardano ecosystem is working on many L2 solutions, one being Hydra, which will allow for a much higher TPS. Early tests shows that the TPS could go into the millions. In a real world scenario, this is yet to be proven though. Below is a twitter post of a PoC video transacting 1000 TPS in one stake pool (there are around 3000 stake pools on Cardano)._

## Access to Leaders or Senior Developers

Cardano has a very active developer community, often being the #1 blockchain by Github commits, and always in top 3. There has been an issue with finding talent, due to the design decision of going with Haskell (and the domain specific language Plutus) as their smart contract language. This is changing though, as the community is rolling out transpilation tools. For example, plu-ts is a typescript transpiler for Plutus, which allows developers to write smart contracts in typescript, and then transpile them to Plutus. This makes it easier for developers to get started, and also makes it easier to find talent.

Using Haskell, which is a pure functional language does come with a set of benefits, such as making code easier to prove correct, which - as we all know - is very important when dealing with user funds.

* https://github.com/HarmonicLabs/plu-ts
* https://www.cardanocube.io/cardano-ecosystem-interactive-map (see developer tools section)


## Credibly Decentralized

Cardano is one of the most decentralized Blockchains. This is due to their previously mentioned relatively low block size, making it easy to run your own full node and/or stake pool. There are users running a stake pool on a raspberry pi. However, in the case of running a stake pool, there is a cost of 340 ADA per epoch, with a yearly yield of about 4% of the ADA being staked. So in practice, you need around one million ADA delegated (by you or others) to your stake pool to be profitable, limiting the number of users able to do so.

There is also something called the "K parameter" which controls the saturation point of a stake pool, or how much ADA can be staked to a pool before it loses efficiency in terms of profitability, which further helps with decentralization.

All stake in Cardano is liquid, so as a regular user, I can delegate my ADA to a stake pool without a lockup period.

* https://datastudio.google.com/u/0/reporting/3136c55b-635e-4f46-8e4b-b8ab54f2d460/page/p_9vyfu6gorc
* https://iohk.zendesk.com/hc/en-us/articles/900004671183-Changes-on-k-parameter-on-epoch-234

## Stability / Predictability of the L1

There is no blockchain more stable than Cardano. Since it's conception, five years ago or so, it's never been down even once. The assertion in the Helium Medium post that "On downtime, the Helium Oracle architecture will be inherently tolerant of temporary L1 outages or disconnects without affecting data transfer or the earnings of Hotspot owners" is absurd. Fault tolerance is good, but reliable predictability is better.

* https://finbold.com/cardano-passes-the-20-million-transaction-mark-without-a-single-outage-in-4-years/
* https://u.today/cardano-reaches-new-milestone-1760-days-without-outages

## Developer Tooling

Cardano has traditionally had a high bar of entry, but this is changing with previously mentioned cross language compilation tools and also with new bootstrapping services emerging recently. Again, because of Cardanos native token system, some of the things requiring smart contracts on other chains can be done natively on Cardano.

Further more, IOG, the organization behind Cardano has proven that they are willing to work with the eco system and with important projects to help them succeed. On top of that, there is a treasury called Cardano Catalyst, which is a decentralized VC fund. This fund has already funded many projects, and has a lot of potential to fund more. It is, in it self, funded by a small % of transaction fees. It is self-governing and the community votes on proposals to be funded.

* https://developers.cardano.org/tools/
* https://projectcatalyst.org/

## Common or Popular Programming Language

As previously mentioned, Cardano uses Haskell, which I would be hard pressed to argue is either popular or common. I would, however, argue that it is a very good choice for a blockchain, as it is a pure functional language, which again makes it easier to prove code correctness.

Also, as previously mentioned, there is a lot of cross-compilation tools being developed, which will make it easier to use other languages. TypeScript is very popular and allows for developers to write both customer facing dApps (webb) and smart contracts in the same language. Down below is two projects that allows you to write both smart contracts and dApps in typescript; plu-ts (still in early development) and cardano-lucid.

As you can see on Stack Overflows yearly survey, JS is the most popular, and TS is the 5th most popular language. Rust is number 14.

* https://github.com/HarmonicLabs/plu-ts
* https://github.com/spacebudz/lucid
* https://survey.stackoverflow.co/2022/#technology

## Strong Exchange Support for Protocol Tokens

Since Cardano's native token ADA is a top ten coin, it has great exchange support. In regards to protocol tokens, any exchange who has ADA listed, can list any Cardano native token. This should be a huge advantage for Helium, as it will be able to easily be listed on any exchange that lists ADA if it's a native token, as it should be.

* https://www.binance.com/en/news/top/7162618

## Several Wallet Teams

There are many independent wallet teams on Cardano that produces both cold wallets, hot wallets and web 3 wallets. In many of these you can stake your ADA while keeping them liquid.

* https://namiwallet.io/
* https://ccvault.io/app/mainnet/welcome
* https://daedaluswallet.io/
* https://www.cardanowallet.io/
* https://www.lace.io/  
* https://yoroi-wallet.com/#/

## More Than One Validator Client

As far as I can find, there is only one validator client - cardano-node. There has been suggestions on this, one that made it in to code (Rust), but has since been discontinued.

* https://github.com/input-output-hk/rust-byron-cardano

## Cost to Run a Mainnet Node

The cost to run a mainnet node, or a full node - Daedalus - is practically 0, as you can run it on your home computer. According to a recent video from Charles Hoskinson, running a validator node cost you about $800 up front and with a minimal recurring cost of internet and powering a low-end computer.

* https://www.youtube.com/watch?v=oH5AZ5f43Qo

## Other Proof of Physical Work Projects

World Mobile, who are bringing affordable internet to Africa, has some common denominators with Helium in the sense that they are distributing infrastructure to previously uncovered areas. It doesn't provide LoraWAN or 5G coverage as helium does, but their work is no less technically challenging or important. Should serve as a really good case study for Helium were they to move to Cardano.

* https://worldmobiletoken.com/

## Mobile Wallet Platform and Phone Project

There is no phone project on Cardano that I know of, but there are plenty of mobile wallets like exodus, yorio, and more. 

* https://www.exodus.com/ada-cardano-wallet
* https://yoroi-wallet.com/#/

## Additional Points

Even though, not a part of the Medium post, there are some other points that I think are worth mentioning. Just like Solana has their phone project going for them so does Cardano in other aspects. Two recent, and very exciting news is the Cardano side chain Midnight, and the upcoming cardano era of Voltaire - governance.

### Midnight

Even though not too much is known about it right now, Midnight will be a Cardano privacy side chain that will allow companies, entities and individuals to integrate with Cardano while keeping sensitive data secret, using something called zero knowledge (zk) proofs. This could potentially be huge for Helium, who is looking to land a lot of real-world projects.

### Voltaire

Cardano is taking the step into true decentralization with Voltaire - the era of governance. There is a Cardano Improvement Proposal (CIP) being evaluated now, that will formally start Voltaire. There are some commonalities between how Cardano and Helium are governed, in regards to voting, that could make the transition easier. I suggest looking at the PR: https://github.com/cardano-foundation/CIPs/pull/380
