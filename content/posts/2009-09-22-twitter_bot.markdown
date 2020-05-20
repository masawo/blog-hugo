---
layout: post
title: ねんがんのtwitter botができた
tags:
- 未分類
status: publish
type: post
published: true
meta: {}
---
GAEで作るtwitter botが、とりあえず形になりました。

<a href="http://twitter.com/garahad_bot">@garahad_bot</a> です。

<span class="mt-enclosure mt-enclosure-image" style="display: inline;"><a href="http://wo.skr.jp/images/uploads/garahad_bot.png"><img alt="garahad_bot.png" src="http://wo.skr.jp/images/uploads/assets_c/2009/09/garahad_bot-thumb-500x314-123.png" width="500" height="314" class="mt-image-none" style="" /></a></span>

botの概要は、タイトルと名前で察しがつくと思いますが、

「ねんがんの」か「念願の」を含んだつぶやきを検索し、発見したら

↓

例の3つの選択肢のどれかをRTでつぶやく(@はつけず)

のようになっています。

ちなみに@をつけない形にしたのは、文面的に考えて、普通に@つきでRTするとSPAMと思われる可能性が高いと思ったからです。元ネタ知らない人に、いきなり「そう　かんけいないね」や「ころしてでも　うばいとる」がやってきても困惑するだけだろうなーと。。

まあ習作ということで、こんなもんですかね。

<!--more-->
Changelog

v0.1 (9/22)

- まだ@つきRTをしないようにしています。
- @されても何も返しません。

v0.2 (9/22)

BOTつくろう会のMLでご指摘をいただき、修正しました。（ねもとさん、ありがとうございます）

- 「〜うばいとる」の前の文言は不適切なため censored に変更。またこの文言での既存POSTを削除。
- @ユーザー名の@を全削除に変更
- 「な なにをする きさまらー」を追加

細かい仕様

- RTの文字が含まれている場合は処理しない
- @garahad_bot が最初にある場合も処理しない(=返事しません)
- 多重につぶやきが発生しないよう、処理結果をDataStoreに記入している

はまった点など

- python初心者なため、構文やモジュールなどを調べながら進めた。正規表現(re)とかrandomとか使った
- <a href="http://sites.google.com/site/bot2uku/">bot作ろう会の教材</a>がとても役に立った
- DataStoreとデータのやりとりをする、gqlなどのところがあまり見ない書き方だったので少しまごついた
- たまにtwitterとの接続ができなくて、twython付近でのエラーで503なんとかというのが返ってくることがある。コードのバグと間違えないよう注意

TODO(やるかどうかはなんともですが。。)

- twitterへの更新がタイムアウトすると失敗してしまうので、その対策
- RTのバリエーションを増やす

- 返事に対応
これをブラッシュアップするか、別に新しいの作るかのどちらかですが、まずは後者のネタを探そうかと。
