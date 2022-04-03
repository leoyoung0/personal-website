---
title: "为何 “Commitment” 称为“秘诺”"
date: 2020-01-01T02:27:12+08:00
draft: false
tags: 
  - translation
  - cryptography
  - 中文
---

前几天在翻译 [Grin](https://github.com/mimblewimble/grin) 的文档 [Introduction to Switch Commitments](https://github.com/mimblewimble/grin/blob/master/doc/switch_commitment.md) 中出现 “Commitment Scheme”。“Commitment Scheme” 一般直接翻译为“承诺方案”。首先来看[维基百科](https://en.wikipedia.org/wiki/Commitment_scheme)对这个词的解释。

> A way to visualize a commitment scheme is to think of a sender as  putting a message in a locked box, and giving the box to a receiver. The message in the box is hidden from the receiver, who cannot open the  lock themselves. Since the receiver has the box, the message inside  cannot be changed—merely revealed if the sender chooses to give them the key at some later time.
>
> Interactions in a commitment scheme take place in two phases:
>
> 1. the *commit phase* during which a value is chosen and specified
> 2. the *reveal phase* during which the value is revealed and checked
>
> In simple protocols, the commit phase consists of a single message from the sender to the receiver. This message is called *the commitment*.
>
> 形象讲解 “commitment scheme” 就是，设想信息发送者将信息放在一个加锁的盒子里，把盒子给接收者。接收者打不开盒子也不知道盒子中的信息。因为接收者拿着盒子，发送者无法更改里面的信息。只有发送者之后将钥匙给接收者才能打开盒子公开信息。
>
> 进行 “commitment scheme” 分两个步骤：
>
> 1. *承诺阶段*，选定并指定一个值
> 2. *解密阶段*，公开并检查这个值
>
> 简单的协议中，承诺阶段包含发送者给接收者发送的信息。这个信息就称为 “*commitment*”。

事实上，“*commitment*” 是一个通过哈希函数运算的一个值，发送者交给接收者。之后发送者再公开运算 “*commitment*” 的密数和致盲因子，由接收者验证哈希值是否匹配。

那么，*“commitment”* 这里就有两个含义，一个是密数，一个是不能更改的承诺。“密”是名词，“秘” 是形容词，所以取“秘”。“诺”即表示“承诺”。因此将 “*commitment*” 翻译为“**秘诺**”，简洁明了，传达其在密码学中的含义。

《秘诺切换简介》一文，阅读请点击[这里](https://github.com/Funkyswing/grin/blob/master/doc/switch_commitment_ZH-CN.md)。

---

**参考：**

1. [秘諾 Commitment](https://taicrypt.wordpress.com/2011/03/29/%E5%AF%86%E8%AB%BE-commitment/)

2. [新华字典](https://zidian.aies.cn/MTI2NjI=.htm)