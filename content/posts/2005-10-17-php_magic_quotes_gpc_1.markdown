---
layout: post
title: さくらのレンタルサーバでのPHPと magic_quotes_gpc
tags:
- 日々
status: draft
type: post
published: false
meta: {}
---
<a href="http://www.sakura.ne.jp/">さくらのレンタルサーバ</a>ではPHP4が動き、そこで（っていうか、ここか）個人的なサイトを作ったりしているわけだけど、GETやPOSTでわたってきた値にシングルクォートが入っていると /' みたいにエスケープしてくれちゃう。

お約束の magic_quotes_gpc というやつである。

このPHP設定がONになっているためにやってくれちゃうので、OFFにしたいのだけれど、さくらのレンタルサーバでは php.ini による変更も .htaccess による変更もどちらも不可。

さて困ったので、マニュアルを読んだ。するとおあつらえ向きの代替関数を発見。

<a title="PHP: マジッククオートを無効にする - Manual" href="http://jp.php.net/manual/ja/security.magicquotes.disabling.php">PHP: マジッククオートを無効にする - Manual</a>

これで一件落着。ふう。
