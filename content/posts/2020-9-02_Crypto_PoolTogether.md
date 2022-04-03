---
title: "加密资产 | 无损彩票"
date: 2020-09-02
draft: false
author: "楊小猴"
tags:
  - crypto
  - 中文
  - DeFi
---

![](/inserted-images/pooltogether.jpg)



根据 [Research and Market 数据](https://www.researchandmarkets.com/reports/4912162/global-lottery-market-2020-2024?utm_source=dynamic&utm_medium=GNOM&utm_code=5ff7lv&utm_campaign=1403482+-+Global+Lottery+Market+Forecast+to+Grow+by+USD+220.52+Billion+During+2020-2024%2c+Progressing+at+a+CAGR+of+10%25&utm_exec=cari18gnomd "彩票业数据")，全球彩票业 2020 年至 2024 年之间预计增长 2,205.2 亿美元，复合年增长率 (CAGR) 10%。目前市场规模大概在五千亿美元。

但目前彩票业对参与者不是最优选。购买者获奖机会微乎其微，而损失本金确实大概率事件。最大的赢家就是彩票公司或发行者。

为何因此还有人买彩票？彩票利用大多数人的认知偏见。多数人不理解根本的风险回报机制。购买彩票前只考虑到巨额回报，而忽视了低赢率。多数人参与其中损失也是自然的事情。

而 PoolTogether 便是利用去中心化网络解决这个问题。**让参与者参与到奖池，有机会获得大奖，而不损失投资**。



### 什么是 PoolTogether？

PoolTogether 就是无损失彩票。相像可以买彩票有机会赢得奖金，而且始终有机会拿回你的本金。

用户通过智能合约存入 Dai 或 USDC 到 PoolTogether 资金池。PoolTogether 会将钱存入开放式货币市场 [Compound.Finance](https://compound.finance)。Compound 会将这些资金借出给货币市场用户。这些资金借贷的利息累积到资金池作为奖励。奖金还包括由个人或公司为生态发展存入 Dai 叫做“赞助资金”(Sponsored Dai) 这些资金产生的利息也用于资金池奖励。

用户每存入一个  DAI 或 USDC 便获得一张彩票 (ticket)。加入资金池有 1,000 Dai，其中你存入 1 Dai，那么你就有一张彩票，获奖概率是 0.1%。

资金池每周开奖。用户资金可以随时取出。只要存款一直在资金池，便可是从参加抽奖。

![stat](/inserted-images/pooltogether-stat.jpg)



### 货币乐高

事实上，PoolTogether 这种机制并不新鲜，与[中奖储蓄 (Prize-linked savings, PLS)](https://en.wikipedia.org/wiki/Prize-linked_savings_account) 类似。PLS 是传统银行用存款获得大额奖金抽奖鼓励用户存款的方式。

通过智能合约部署 PLS 可以保证资金安全性和抽奖公平性。无需 KYC/AML，无需许可，全球用户无障碍参与。

PoolTogether 可以利用无损彩票吸引用户，同时可为 DeFi 下游提供资金池，带来更多流动性。

PoolTogether 有潜力成为 DeFi 彩票的重要组成部分，甚至在全球彩票业中占得份额。



### 抽奖机制

抽奖机制如下:

1. 开奖前管理员选取一个随机数（密数）
2. 随机数生成一个数字指纹，公布指纹但不公布密数
3. 管理员锁定参加抽奖资金
4. 管理员公开密数。智能合约保证密数与数字指纹匹配
5. 智能合约选取与随机数匹配的获奖者

抽奖机制目前选取随机数方面仍旧中心化。后续版本团队会在这方面改进。

![winner sellection](/inserted-images/pooltogether-winner.jpg)

中奖者选取过程：

假设资金池中有两位用户张比特和李太坊。张比特存入 800 Dai，李太坊存入 200 Dai。那张比特的彩票就是 1 - 800，李太坊的彩票就是 801 - 1000。如果中奖随机数是 513，那就张比特中奖。如果随机数是 842，李太坊中奖。



### 安全性

目前 PoolTogether 合约采用 ERC 777 标准，有管理员权限。合约都经过 OpenZeppelin 和 Quantstamp 审计。社区还有[漏洞赏金计划](https://github.com/pooltogether/pooltogether-contracts/issues/1)，奖励发现漏洞的黑客。因为项目在初始阶段，用户在使用前做好对合约等各项风险评估。



*（__风险提示__：本文仅供学习交流之用。加密资产为高波动高风险资产，购买或交易前请做好风险评估。）*



--------------

*参考：*

1. Pool Together FAQ：https://www.pooltogether.com/faq

2. [How PoolTogether Selects Winners](https://medium.com/pooltogether/how-pooltogether-selects-winners-9301f8d76730)

3. [PoolTogether v2.0: Audit Disclosures](https://medium.com/pooltogether/pooltogether-v2-0-audit-disclosures-d968a1875ec)



