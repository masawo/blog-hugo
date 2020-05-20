---
layout: post
date: 2008-06-25T03:00:00+09:00
title: Ubuntu 8.04 server-amd64 のインストール
slug: ubuntu_804_server-amd64
tags:
- 未分類
status: publish
type: post
published: true
meta: {}
---
今使っている自宅サーバはかなり非力(Celeron400MHz)で、ちょっと何かをインストールしようとするだけで結構な時間がかかったりします。

我慢して使ってきたけれど、さすがにもう5,6年経つしそろそろ換えどきかなと思ったので、以前組み立てたTurion64なPCに移行していきたいと思います。

ということでまずはＯＳの準備。

<!--more-->
部屋の片隅で眠っていたTurion64マシンを開けて、買ってきた1TBのHDD2つを組み付け、ubuntu linux server をインストール。

＃1TB HDDは秋葉原で1つ15k強で購入。今やこんな容量でも安いんだな...

RAIDの設定とかは以下を参考にしながら。

<a href="http://www.thinkit.co.jp/free/article/0707/11/2/">[ThinkIT] 第2回：Ubuntu Serverをインストール (1/4)</a>

apt-get upgrade を済ませたあと、「確か以前にCentOSを入れたときには powernow！が効いていたから、今回も効くはず」ということを思い出して cat /proc/cpuinfo をしてみると、CPUは1600Mhz（大きい方）になっていました。（小さいほうは800MHz。低負荷時はこれになってるはず）

はて。何か設定とかあるのかな？と思って情報を探したら、以下を発見。その通りにやってみたら、無事に800MHzになりました。

<a href="http://exposed.egoism.jp/wordpress/?p=325">hp prolliant ml115 debianでのCool'n'Quiet</a>

以上を一通り終えてからも、HDD LEDがずっと点灯したままでしたがRAIDによるもののようです。(就寝して起きたら消えてた)

続きはまた日を改めて。
