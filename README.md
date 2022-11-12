# Helium HIP 70 - The case for Cardano

Based on [this medium post](https://medium.com/helium-foundation/hip-70-evaluating-layer-1-blockchains-for-the-helium-network-15f81af6941c), which makes the case for Solana, I will address the same points to make the case for Cardano as Heliums L1. For some reason, Cardano was not in the comparison table of the linked article, which makes it seem like it was not considered by the Helium team as an alternative.

## TLDR

Cardano is a organically decentralized eco system with a large pool of single stake pool operators and a high Nakamoto Coefficient. It's predictably reliable and performant, with a clear roadmap for further decentralization with upcoming the Voltaire hard fork as well as scaling solutions, Hydra, that will put the TPS far beyond the needs of Helium. Cardano has a strong developer community and a fast evolving developer tooling eco system. Continue reading to see why Cardano is a great choice for Helium as a L1.

## Compatible Wallet Cryptography

While Cardano doesn't use the same key algorithms as Helium, it has shown to be willing to create primitives to ease cross chain interoperability, by adding support for secp by popular request. I would not be surprised if they would be able to do the same for ed25519.

* https://iohk.io/en/blog/posts/2022/11/03/what-is-secp-and-how-it-drives-cross-chain-development-on-cardano/

## Credible Scalability Plan

Cardano recently released a new version of their chain, in a so-called hard fork combinator event (which allows the chain to continue to be fully operational while upgrading). This version, called Vasil, considerably increased performance and scalability of the chain. Many projects and dexes reported a hugh decrease in transaction size, and an equally large decrease in transaction settlement times. 

* https://iohk.io/en/blog/posts/2022/07/04/cardano-s-approaching-vasil-upgrade-what-to-expect/

## DeFi Ecosystem

While Cardano has a relatively small DeFi eco system, and a low TVL, this is changing at a fast paste. Many dexes has released over the last year, using both AMMs, traditional order book models, yield farms and more. Below is a list of a few of them.

* https://muesliswap.com/
* https://minswap.org/
* https://sundaeswap.finance/

On top of this, because of Cardano's native token concept, there are a lot of NFT projects, NFT market places, and a handful of promising metaverse projects.

* https://www.jpg.store/
* https://www.cardanocube.io/collections/metaverse

## Transaction Cost

Cardano has a fixed transaction cost, which is 0.17 ADA, or at the time of writing $0.06 per transaction. This is compared to Heliums $0.35 transaction cost. This will however increase as the price of Cardano does. With Cardano, you can also send many different tokens in one transaction, making it very cost effective.

* https://cardano.stackexchange.com/a/6167

## High Transaction Throughput

For the moment, Cardano is capped at 7 TPS. This is based on a blockchain parameter, `maxBlockSize`, which is currently set to 65536 bytes. One transaction is around 450 bytes, which means that a block can contain around 145 transactions. One block is processed every 20 seconds, making the TPS around 7. There is a lot of complexity. However, with the latest rollout of Vasil, this number is probably higher since it added reference inputs which can reduce the size of a transaction by up to 90%. In the case of Cardano

Last epoch - five day period - Cardano processed 363,843 transactions over 432,000 "slots" making the effective TPS 0.84. This shows that there are plenty of room with current blok parameters. Should there be a need for it, `maxBlockSize` can easily be increased to a low estimate of 50 TPS. To mitigate block size related centralization, Cardano is working on a technology called Mithril, which will make bootstrapping easier, and make it possible to run lightweight full nodes, even in hot wallets.

Cardano are working on a L2 scaling solution called Hydra which will allow for a much higher TPS. Early tests shows that the TPS could go into the millions. In a real world scenario, this is yet to be proven though. Below is a twitter post of a PoC video transacting 1000 TPS in one stake pool (there are around 3000 stake pools on Cardano).

* https://www.quora.com/How-many-transactions-per-second-TPS-can-Cardano-do-and-what-does-this-mean-for-the-network
* https://explorer.cardano.org/en/epoch?number=374
* https://twitter.com/SundaeSwap/status/1580969361892085762
* https://docs.cardano.org/development-guidelines/scalability-solutions/mithril

## Access to Leaders or Senior Developers

Cardano has a very active developer community, often being cited as being the #1 blockchain by Github commits, and always in top 3. There has been an issue with finding talent, due to the design decision of going with Haskell (and the domain specific language Plutus) as their smart contract language. This is changing though, as the community is rolling out transpilation tools. For example, plu-ts is a typescript transpiler for Plutus, which allows developers to write smart contracts in typescript, and then transpile them to Plutus. This makes it easier for developers to get started, and also makes it easier to find talent.

## Credibly Decentralized

Cardano is one of the most decentralized Blockchains. This is due to their previously mentioned relatively low block size, making it easy to run your own full node and/or stake pool. There are users running a stake pool on a raspberry pi. However, in the case of running a stake pool, there is a cost of 340 ADA per epoch, with a yearly yield of about 4% of the ADA being staked. So in practice, you need one million ADA delegated to your stake pool to be profitable, limiting the number of users able to do so. All stake in Cardano is liquid, so as a regular user, I can delegate my ADA to a stake pool without a lockup period.

* https://datastudio.google.com/u/0/reporting/3136c55b-635e-4f46-8e4b-b8ab54f2d460/page/p_9vyfu6gorc

## Stability / Predictability of the L1

There is no blockchain more stable than Cardano. Since it's conception, five years ago or so, it's never been down even once. The assertion in the Helium Medium post that "On downtime, the Helium Oracle architecture will be inherently tolerant of temporary L1 outages or disconnects without affecting data transfer or the earnings of Hotspot owners" is absurd. Fault tolerance is good, but reliable predictability is better.

* https://finbold.com/cardano-passes-the-20-million-transaction-mark-without-a-single-outage-in-4-years/
* https://u.today/cardano-reaches-new-milestone-1760-days-without-outages

## Developer Tooling

Cardano has traditionally had a high bar of entry, but this is changing with previously mentioned cross language compilation tools and also with new bootstrapping services emerging recently. Again, because of Cardanos native token system, some of the things requiring smart contracts on other chains can be done natively on Cardano.

Further more, IOG, the organization behind Cardano has proven that they are willing to work with the eco system and with important projects to help them succeed. On top of that, there is a treasury called Cardano Catalyst, which is a decentralized VC fund. This fund has already funded many projects, and has a lot of potential to fund more. It is, in it self, funded by a small % of transaction fees. It is self-governing and the community votes on proposals to be funded.

* https://developers.cardano.org/tools/

## Common or Popular Programming Language

## Strong Exchange Support for Protocol Tokens

Since Cardano's native token ADA is a top ten coin, it has great exchange support. The only major exchange not wanting to list ADA was FTX.

## Several Wallet Teams

Nami, eternl, Daedalus, Lace, Yoroi, and many more.

## More Than One Validator Client

## Cost to Run a Mainnet Node

Daedalus 

## Other Proof of Physical Work Projects

World Mobile

## Mobile Wallet Platform and Phone Project