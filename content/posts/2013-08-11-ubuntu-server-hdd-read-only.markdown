---
layout: post
title: "自宅サーバがread-onlyになってた&修復"
date: 2013-08-11 21:19
comments: true
categories: 
---
自宅サーバのUbuntuにちょっと久しぶりにログインしたら、read-only file system などという文言が。  
数日前からHDDの片方が怪しくなって、RAIDが解除されてこの状態になってたみたい。  
この週末はこれをどう直そうか調べたり、他の手段を考えたりしているうちに終わってしまいました。この機会にNASにでも移行したほうがいいのかなあ、でも高いしな、とか。。
<!-- more -->

<iframe src="//instagram.com/p/c3tQByCSun/embed/" width="612" height="710" frameborder="0" scrolling="no" allowtransparency="true"></iframe>

問題のHDDはRAID1構成にしてた1台目のほうで、再起動するとread-onlyになったりならなかったりして不安定な状態。  
今回の自宅サーバだとシステム領域はデータとは別に切ってあって、RAIDはデータ部分だけ取っているという環境です(導入時になぜかHDD全体ごとのRAIDができなかったので)。  

とりあえずシステムのデータを2台目にddでコピーして、1台目をRAIDから切り離したあとにshutdown。  
物理的にHDD1台目を外して起動しなおし、RAIDを解除したりfstabの設定を書き換えたりして、通常の動作に戻りました。

てことで今はHDD単独の体制で、いつ災いが起こるか分からない状態。  
まめに他HDDにバックアップを取っているつもりなので、それでもなんとかなるけれど、不安なのでやっぱりNASを買うべきかなあ。

NASはいろいろ調べた中では QNAP TurboNAS TS-220 というのが気になりました。  
[QNAP Systems, Inc. - ネットワーク接続ストレージ - 製品紹介 - 製品紹介 - ストレージ - ホーム＆SOHO - 2 ベイ - TS-220](http://www.qnap.com/jp/index.php?lang=jp&sn=699&c=328&sc=601&t=610&n=18427)

<iframe src="http://rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=masawo-22&o=9&p=8&l=as4&m=amazon&f=ifr&ref=ss_til&asins=B00CF9VFSU" style="width:120px;height:240px;" scrolling="no" marginwidth="0" marginheight="0" frameborder="0"></iframe>

<iframe src="http://rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=masawo-22&o=9&p=8&l=as4&m=amazon&f=ifr&ref=ss_til&asins=B008P56QTG" style="width:120px;height:240px;" scrolling="no" marginwidth="0" marginheight="0" frameborder="0"></iframe>



### 参考
◇mdadmによるRAIDの解除◇初心者のためのLinuxサーバー構築講座(CentOS 自宅サーバー対応)☆お便利サーバー.com☆ http://www.obenri.com/_raid_create/delete_mdadm.html
