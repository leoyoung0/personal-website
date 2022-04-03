---
title: "加密资产 | Erasure 数据交易市场"
date: 2020-06-10
draft: false
author: "楊小猴"
toc: true
tags:
  - crypto
  - 中文
---

![Erasure_home](/inserted-images/Erasure_home.jpg)

> *“信息是种独特的商品：其创造方式不可预知，只有拥有后才能判断是好是坏。只要拥有的人就可以无成本复制。这就造成市场难以对其进行定价并传播价值。”*
>                    -- [Joel Monegro](https://www.placeholder.vc/blog?author=5a479edd5e0ed81e5677b589)，Placeholder*

在社交网络或使用即使通讯工具，随时都有无数信息传播。面对海量信息，我们又无暇验证每条看到的信息真实性。之所以假消息或误导性信息泛滥，就是因为制造成本低。那么有没有一种方式可以遏制不实或假消息的制造，并增加传播成本？去中心化数据交换协议 Erasure 就是要做这样的事情。

### Numerai 的开放式金融数据社区

[Erasure](https://erasure.wolrd) 由 Numerai 构建。Numerai 是一家匿名数据科学家社区组成的量化交易对冲基金，2015 年底由数据科学家 Richard Craib 创办。得到对冲基金文艺复兴科技 ([Renaissance Technologies](https://www.rentec.com/)) 联合创始人 Howard Morgan，天使投资人 [Naval Ravikant](https://en.wikipedia.org/wiki/Naval_Ravikant) 和风投 USV 投资。2017 年在以太坊发行代币 Numeraire ([NMR](https://etherscan.io/token/0x1776e1f26f98b1a5df9cd347953a26dd3cb46671))，用以股市数据预测抵押和奖励。

传统对冲基金掌握金融市场大量关键数据，以文艺复兴为例每年处理上 PB 数据。这些数据对这些基金来讲就是金矿，数据分析方法和工具就是炼金术。这是它们保持优势所在。随着开源工具 [Theano](http://deeplearning.net/software/theano/) 和 [TensorFlow](https://www.tensorflow.org) 的应用，各领域数据科学研究更加开放。在加密学领域同态加密 ([homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption)) 的发展，可以保护机密信息同时向数据科学家公开数据用以机器学习和数据分析。

Numerai 因此而诞生。Numerai 开放股票市场数据，数据科学家应用机器学习算法预测股票未来价格。参与者抵押一定 NMR 代币，智能合约锁定。抵押代币多少代表对自身预测结果的信心程度。预测结果越准确，获得相应的奖励越高。相反，如预测结果偏差过大，Numerai 可以对其进行惩罚。按照预设比例，以一定小金额价值代币燃烧对方大金额代币。例如惩罚比例是 `0.1` ，Numerai 可自己燃烧 `1` 个 NMR 燃烧对方 `10` 个 NMR。燃烧就是“删除键”，将你我的钱都消失。 

> *二十一实际最有价值的对冲基金会将网络效应融入到资本分配中。*
>              *-- Richard Craib，Numerai 创始人*

**Numerai 的创新之处就是有“价值抵押的数据”能更加保证数据质量**。数据科学家通过挖掘数据结果获得奖励，提供数据行为更像是一种共识行为，或者可以称为“智力证明” (Proof of intelligence)。自 2017 开始 Numeraire 就是以太坊应用最多的代币之一。数据科学家不仅愿意用自己的有价值数据换得加密货币，也愿意对自己的信息进行价值抵押。保证信息质量同时，更有利于基金在匿名网络分配资金。如果有人愿意对自己的数据结果进行抵押，会有人更放心购买，**风险共担的市场促进优质信息传播**。

但 Numerai 只是基于以太坊的专为数据科学家所参与的一个数据应用，完全中心化。Numeraire 代币也没有治理作用。因此，Erasure 协议应运而生。

### Erasure 为信息创造价值

> *“过去已被抹除，抹除的已被忘记，谎言变成真相。”*
>                 *-- 《1984》,乔治·奥威尔*

Erasure 是全新一代去中心化数据交易市场。 Erasure 协议基础有三种经济关系要素：支付、记录追踪和追索。有人想要付费获得某只股票预测结果，抵押支付金额。有人打算提供预测结果也提供抵押一定金额表示对自己提供信息的信心程度。双方抵押金额锁定在智能合约。预测结果可设定经过加密，只有买方可以看到。待答案公开，买方对结果满意，合约完成，卖方获得付费和自己抵押的代币。如果不满意，买方可按照之前设定的比例决定互相燃烧一定金额代币。以上所有信息，包括智能合约抵押、交易、提交答案信息，都自动记录在以太坊链上有据可查，不可篡改。

Erasure 协议支持任何以太坊原生代币，目前可使用 NMR 和 Dai。支付是区块链最闪光之处，让互联网上价值交换更便捷。也是智能合约得以实现的基础。

记录追踪即是 Erasure 记录所有信息的历史记录。向 Erasure 提交的信息数据上传到 IPFS (去中心化文件存储网络)，Erasure 将存储相应数据的哈希函数发送到以太坊链上得到时间戳 (timestamp)，一旦在链上得到确认再也无法更改。时间戳是区块链应用的最关键技术，可以让你确信某条信息的发生时间。交易信息都可在以太坊链上查询，抵押多少代币，智能合约是否执行，代币是否燃烧，燃烧多少… 所有都公开可查。

追索是 Erasure 最重要的功能，即是如果买方对某个信息不满意，买方可以按比例燃烧卖方的钱。例如我看到有人的股市预测准确率达到 70% 以上，而且对自己的预测抵押一万块。这说明他对自己的预测结果信心很高。但是万一预测准确度低于 50%，你既付钱买了信息，又因此在交易种亏损。那么在 Erasure 上交易前，卖方可以设定一个“惩罚比例”。例如 1 : 10 表示买方可用 1 块燃烧卖方 10 块。这样就能保证卖方更大概率提供更优质的预测结果。

### Erasure 的应用

根据 Defipulse 的数据，目前 Numerai 在以太坊应用排名第 17。抵押代币总额 270 万美元，276 BTC等值。

![Erasure_pulse](/inserted-images/Erasure_pulse.jpg)

[Erasure Bay](https://erasurebay.org/) 是去中心化信息交易平台。可以交易预测、机密、咨询等信息。交易时需要卖方抵押一定金额代币。例如当前开放的交易有“按地区邮编分类搜集 3 月 20 日之前的美国全国的失业 csv 数据表，报价 100 美元”。

![Erasure_twitter](/inserted-images/Erasure_twitter.jpg)

![Erasure_bay trade](/inserted-images/Erasure_bay_trade.jpg)

[Erasure Quant](https://erasurequant.com/) 是 Numerai 的另一个预测比赛。参赛者预测罗素 3000 成分股价格。所有预测都需要抵押，根据预测结果准确度决定获得奖励还是燃烧抵押。

未来，从体育比赛到股市到天气预测，甚至匿名爆料新闻都可以在 Erasure 进行。在社交网站、论坛、贴吧充斥大量无效信息，可以通过抵押来进行过滤。文章开头的假消息问题可以通过 Erasure 轻松解决。

在信息流动的互联网世界，Erasure 要帮助大家实现去中心化无需第三方仲裁的信息过滤系统。

----------

Numeraire 概况：

NMR 总量：1,100 万；

流通量：2,620,231 

- 2020 年 6 月初 Union Square Ventures、Placeholder、CoinFund、Dragonfly Capital 和 Numerai 创始人 Richard Craib 融资 300 万用于 Erasure 协议开发
- 2019 年 3 月 Paradigm 和 Placeholder 为 Numerai 提供融资 1100 万

--------------

*参考：*

https://medium.com/numerai/numerais-master-plan-1a00f133dba9

https://medium.com/numerai/numerai-reveals-erasure-unstoppable-peer-to-peer-data-feeds-4fbb8d92820a

https://medium.com/numerai/the-erasure-protocol-awakens-48a34cc4b5d0

https://medium.com/numerai/a-new-cryptocurrency-for-coordinating-artificial-intelligence-on-numerai-9251a131419a

https://github.com/erasureprotocol/erasure-protocol

https://en.wikipedia.org/wiki/Skin_in_the_game_(phrase)

https://www.placeholder.vc/blog/2020/4/9/erasure

https://twitter.com/ErasureBay

--------------

##### *Tipping (交易即交流)*
*BTC: 13B1egteYRnEsTA7mY5AdqUT3DhACmqiyL*
*ETH: 0x19DB3775ce48A0f96CD8D9C9E2d30B23705a35f5*
*XLM: GBS4WDJBP2MQYTYHESCEVO2WTOPEN22XDTMTKTK4GO4OPQ3O36RZOHZM*
*Grin: 2wcagjgl7j2koe57trfjpylx2qum7qr6f65evbldl7vh2wrrmkdi6zyd*