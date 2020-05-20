---
layout: post
date: 2005-10-04T03:00:00+09:00
title: moblog on Mobavle Type 3.2
slug: moblog_on_mobavle_type_32
tags:
- 日々
status: publish
type: post
published: true
meta: {}
---
携帯からのblog投稿の際には、おなじみのひらたさん作のmoblog gateway を利用させていただいている。

<a title="moblog.uva.ne.jp - moblog mail gateway [dh's memoranda]" href="http://uva.jp/dh/mt/archives/000639.html">moblog.uva.ne.jp - moblog mail gateway [dh's memoranda]</a>

今回はMobavle Type 3.2 を新しく設置したので、moblogの再設定を行った。
…のだが、なぜか設定しようとすると以下のエラーが出る。
<blockquote>We detected xmlrpc API successfully.
Cannot login to your Movable Type. Please confirm username and password again.</blockquote>

MTのメニューにログインして設定を調べていたら、ああ…
XML-RPC APIのパスワードを設定する項目があった。
（「メイン・メニュー > システム・メニュー > 投稿者 > [ユーザ名]」のところの、下のほうにある）

3.2からはAPIパスワードの設定が別になったようだ。
投稿したいパスワードでログインして、そのユーザのAPIパスワードを設定し、それを moblog gateway でも設定すると
無事に設定できた。携帯にメールが送られ、書かれたメアドにテスト投稿をし、成功を確認。
というわけで引き続き利用させていただきます。

<!--more-->
(2006/02/04追記)
ここを検索経由で訪れる方が多いようですね。
トラックバックのあった以下のサイトに画面キャプチャを交えて説明がされていますので、こちらを参考にすれば一目瞭然かと思います。

<a href="http://epi.fm.senshu-u.ac.jp/~haruka/archives/2006/02/movabletype_32.html" title="オンラインマニュアル: MovableType 3.2 を使用する際の注意点">オンラインマニュアル: MovableType 3.2 を使用する際の注意点</a>
