---
layout: post
title: "自分のブックマークライフについて"
date: 2014-02-28 22:31
comments: true
categories: 
---
何年か前からソーシャルブックマークサービス(deliciousやはてなブックマークのような)を使って、気になったサイトのブックマークを日頃つけています。

確か、はてなブックマーク が始まる前に delicious ができて、そこで始めたんだったと思います。  
で、はてブができたあとも基本は delicious を使ってブックマークを追加してます。  
そしてそこからtwitterに1時間おきとかで「じわじわ」投稿したり、はてブに同じ内容を追加する仕組みを ifttt を使って行っています。

[自分のtwitter](http://twitter.com/masawo)にリンクつきのものが多いのは以上のような理由です。

- [自分のdelicious](https://delicious.com/masawo)
- [自分のはてブ](http://b.hatena.ne.jp/masa-wo/bookmark)

<!-- more -->

## フロー

* delicious にブックマークを追加する
* ifttt その1: deliciousに追加されたブックマークをbufferのtw postに追加
* ifttt その2: deliciousに追加されたブックマークをはてブにも追加
* ifttt その1でbufferに追加されたツイートが、bufferで設定した時間に少しずつpostされる

## なぜdeliciousを使っている?
普段ブックマークに使っているのがiOSアプリの[reeder](http://reederapp.com/ios/)で、これは国外で作られているアプリなのでブックマークサービスがdeliciousぐらいしか選べないためです。  
feedly も使っていますが、そこでも同じ。  
delicious はサービス運営元が時々変わったりしていて不安な気もするのですが、わりと仕方なくそうしている向きも。

## ifttt 便利
はてブへの転送をするために作ったrecipeが↓なんですが、同じことを考えている方はそこそこいるようで、18 uses になっています。

[IFTTT / delicious to hatena bookmark by masawo](https://ifttt.com/recipes/25763-delicious-to-hatena-bookmark)

※ハマりどころとして、iftttの設定(preferences)にある URL Shortening はOFFにしておく必要があります。これをやらないと、はてブに追加されるURLが ift.tt なものになってしまっておかしくなります。

## bufferからのツイートにちと問題が
タイトルやURLが長いブックマークだと、bufferに追加される際にURLが略されてしまったり、短縮URLだけになってしまうことが多少あります。  
ここはiftttだとどうにもならなさそうな気配なので、はてブ側のwebhookを使うとか、別の方法を模索したほうがいいかもなと思っている今日この頃。

## なぜ、じわじわツイートしている?
「短時間に連投すると、気分を害するfollowerさんがいるかもしれない」という（無用かもしれない）配慮です。ツイート間隔が開いているほうが自分的には好ましいかな、と。  
もちろん、普通に即時のツイートもしています。ただ最近は以上のブクマしたときの内容ツイートが半分以上な感じですね。

## bufferで蓄積できるのは10件まで
普通にブックマークしていると簡単に10件上限になってしまうので、ブクマしすぎないように留意したりしています。  
月額契約をすればリミッターを解除できるんですが、月に900円ぐらいかかるので、二の足を踏んだまま運用でカバーしている感じです。