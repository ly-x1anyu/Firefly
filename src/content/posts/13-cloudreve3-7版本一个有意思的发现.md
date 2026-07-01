---
title: Cloudreve3.7版本一个有意思的发现
published: 2023-06-02
pinned: false
tags: [bug？, 发现, 技术交流]
category: 技术交流
draft: false
slug: 13
image: https://api.boxmoe.com/random.php?13
---

昨天更新了Cloudreve到3.7.1版本，发现一个很有意思的情况

再替换源文件之后，重新启动Cloudreve进入网页却发现整体变成了英文界面

我以为是缓存问题，清除缓存后仍然存在 之前用的3.5版本并没有这个问题 神奇的是，谷歌显示英文，edge显示中文 在手机上尝试了一下，问题同上

按理来说，如果按照的事系统语言，并不会导致两个不同的浏览器显示不同的语言 而且他们还是同样的内核，神奇