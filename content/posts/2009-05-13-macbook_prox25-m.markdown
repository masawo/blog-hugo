---
layout: post
title: MacBook ProでX25-Mを使う
tags:
- 未分類
status: publish
type: post
published: true
meta: {}
---
2ヶ月ぐらい前に、爆速で評判のIntel製MLC SSD <a href="http://www.intel.com/design/flash/nand/mainstream/index.htm">X25-M</a>を買いました。(購入価格\39,800)

これまではThinkpad X61sに導入して速さを堪能していました。

が、X61sよりMacBook Proのほうを使っていることがほとんどなのでもったいないと思い、10日にMBPに換装してしまいました。

既にMBPのHDDは500GBに換装していたけど、今の自分の用途だと80GB程度でも十分なので。

手順は前回と同じように、

中を開けてHDDをSSDに交換→TimeMachineのHDDを接続・Leapardのディスクを入れ、cを押しながら電源ON→TimeMachineで復元

ですんなり。

とりあえず目に見える効果として、OS起動時間が半減しました(１分ちょい→30秒)。

また、前より動きがキビキビしている感じ。

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B001F4YIYY/masawo-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/31quClCokEL._SL160_.jpg" alt="インテル社製 X25-M Mainstream SATAII SSD 2.5インチSATAII 80GB READ 240MB/s WRITE 70MB/s SSDSA2MH080G1" style="border: none;" /></a></div><div class="amazlet-info" style="float:left;margin-left:15px;line-height:120%"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B001F4YIYY/masawo-22/ref=nosim/" name="amazletlink" target="_blank">インテル社製 X25-M Mainstream SATAII SSD 2.5インチSATAII 80GB READ 240MB/s WRITE 70MB/s SSDSA2MH080G1</a><div class="amazlet-powered-date" style="font-size:7pt;margin-top:5px;font-family:verdana;line-height:120%">posted with <a href="http://www.amazlet.com/browse/ASIN/B001F4YIYY/masawo-22/ref=nosim/" title="インテル社製 X25-M Mainstream SATAII SSD 2.5インチSATAII 80GB READ 240MB/s WRITE 70MB/s SSDSA2MH080G1" target="_blank">amazlet</a> at 09.05.13</div></div><div class="amazlet-detail">Intel <br />売り上げランキング: 5911<br /></div><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B001F4YIYY/masawo-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jp で詳細を見る</a></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<!--more-->

以下はXbenchの結果。Random Read性能が激変してるし、Sequentialも倍ぐらいになってますね。

導入したMBPは2006年後半発売のものでSATA2ではないので、X25-Mのフル性能は出せていないようです。でもスペックアップとしては十分かな。

換装前
<pre>
Results	129.73
System Info
Xbench Version		1.3
System Version		10.5.6 (9G55)
Physical RAM		2048 MB
Model		MacBookPro2,2
Drive Type		WDC WD5000BEVT-22ZAT0
(中略)
Disk Test	59.50
Sequential	90.70
Uncached Write	105.62	64.85 MB/sec [4K blocks]
Uncached Write	115.82	65.53 MB/sec [256K blocks]
Uncached Read	53.38	15.62 MB/sec [4K blocks]
Uncached Read	137.62	69.17 MB/sec [256K blocks]
Random	44.27
Uncached Write	16.61	1.76 MB/sec [4K blocks]
Uncached Write	126.84	40.61 MB/sec [256K blocks]
Uncached Read	70.10	0.50 MB/sec [4K blocks]
Uncached Read	125.04	23.20 MB/sec [256K blocks]
</pre>

換装後
<pre>
Results	174.97
System Info
Xbench Version		1.3
System Version		10.5.6 (9G55)
Physical RAM		2048 MB
Model		MacBookPro2,2
Drive Type		INTEL SSDSA2MH080G1GC
(中略)
Disk Test	182.39
Sequential	115.35
Uncached Write	122.54	75.24 MB/sec [4K blocks]
Uncached Write	112.85	63.85 MB/sec [256K blocks]
Uncached Read	74.18	21.71 MB/sec [4K blocks]
Uncached Read	239.68	120.46 MB/sec [256K blocks]
Random	435.49
Uncached Write	546.00	57.80 MB/sec [4K blocks]
Uncached Write	197.38	63.19 MB/sec [256K blocks]
Uncached Read	1596.25	11.31 MB/sec [4K blocks]
Uncached Read	602.07	111.72 MB/sec [256K blocks]
</pre>
