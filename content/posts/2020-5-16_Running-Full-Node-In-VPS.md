---
title: "VPS 运行 Grin 全节点"
date: 2020-05-15
draft: false
author: "楊小猴"
tags:
  - crypto
  - 中文
---

本文将介绍如何利用 VPS 设置 Grin 全节点。

### 为什么要设置全节点？

* 安全。利用自己设置的全节点可以保证交易安全性。
* 保护隐私。自己的全节点验证交易，保证交易输出和 IP 地址不被泄露。
* 保证网络稳定。拒绝恶意行为。提高区块同步速度和交易速度。

---------------------------------

### 准备

* VPS
* Linux Debian 10.0

### 设置：

进入 root：

```
sudo -i
```

或建立新超级用户，请参阅[这里](https://linuxize.com/post/how-to-create-a-sudo-user-on-debian/)。

更新系统：

```
sudo apt-get update
```

安装必备工具：

```
sudo apt-get install git nano screen pkg-config
```

出现提示 `Do you want to continue? [Y/n]` 输入  `Y`。

安装相关组件：

```
sudo apt-get install clang cmake libncurses5-dev libncursesw5-dev zlib1g-dev libssl-dev tor
```

出现提示 `Do you want to continue? [Y/n]` 输入  `Y`。

安装 rust：

```
curl https://sh.rustup.rs -sSf | sh; source $HOME/.cargo/env
```

出现提示
`1) Proceed with installation (default)`
`2) Customize installation`
`3) Cancel installation`
一般选择默认选项 `1`。

在安装节点和钱包前，先用 Screen 打开三个界面。一个界面用以安装程序和普通浏览 (console)；一个用以运行节点 (node)；一个用以操作钱包 (wallet)。关于 Screen 使用，详情参阅[这里](https://linuxize.com/post/how-to-use-linux-screen/)。建议用一个打开一个。

```
screen -S console
```

按 `Ctrl + A + D` 退出到主介面。

```
screen -S node
```

按 `Ctrl + A + D` 退出。

```
screen -S wallet
```

构建最新版本节点：

```
git clone https://github.com/mimblewimble/grin.git
cd grin
cargo build --release
```

也可以从[这里](https://github.com/mimblewimble/grin/releases)直接下载新版本节点。这步大概需要 30 分钟。等待期间可以浏览 [Grin Wiki 百科页面](https://github.com/mimblewimble/docs/wiki/Wallet-User-Guide)，多了解 Grin。

设置节点：

退出到主介面，使用以下命令显示现有页面

```
screen -ls
```

使用下面的命令打开 `node` 页面

```
screen -r xxxxx
```

运行 node

```
cd grin
export PATH=`pwd`/target/release:$PATH
grin
```

设置节点配置文件（可选）

```
cd  #进入根目录
nano .grin/main/grin-server.toml  #打开配置文件
```

设置 `api_http_addr = "0.0.0.0:3413"` 和 `host = "::"`。
最后重启节点。

全节点如图顺利运行

![1](/inserted-images/Node-running.jpg)

![2](/inserted-images/Node-direction.jpg)

----------------------

*参考：*

1. *[How to: Run a Grin node on Google Cloud for free](https://github.com/mimblewimble/docs/wiki/How-to%3A-Run-a-Grin-node-on-Google-Cloud-for-free)*
2. *[Running a Grin Node](https://github.com/mimblewimble/docs/wiki/How-to-run-a-Grin-node)*
3. *https://github.com/MCM-Mike/grinnode.live/blob/master/grin-server.toml*
4. *[How to use the Grin wallet](https://github.com/mimblewimble/docs/wiki/How-to-use-the-Grin-wallet)*
5. *[How to install Grin node on VPS (下载安装)](https://medium.com/@28e6d94f/how-to-install-and-run-a-grin-node-with-a-debianvps-dab8dcbe88d8)*

