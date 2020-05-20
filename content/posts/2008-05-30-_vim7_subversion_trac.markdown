---
layout: post
date: 2008-05-30T03:00:00+09:00
title: さくらインターネットで vim7, Subversion, Trac
slug: _vim7_subversion_trac
tags:
- 開発系
status: publish
type: post
published: true
meta: {}
---
このブログの置いてある、さくらインターネットのレンタルサーバの環境を整えようと、vim7 や Subversion やら Trac を導入してみました。

やはり、既にやってる方のログを真似することに。

まずは↓の内容の通りに、それぞれインストール。

<a href="http://www.ruche-home.net/sakura.html">さくらサーバをオレ色に染めてみる</a>

※最初、neonなどの各アプリは最新のものをわざわざ見つけてきて試したのですが、依存関係などがあってハマってしまいました...(最終的にはneonを25.xでビルドしなおしたら解決)

書いてあるままのバージョンのものを導入すれば問題ないのではと思います。

で、Tracがとりあえずブラウザで見えるようになったら、↓を見ながら設定。

<a href="http://www.machu.jp/diary/20070718.html#p01">さくらインターネットで Subversion + Trac - まちゅダイアリー (2007-07-18)</a>

とりあえず構築だけしたってことで、まだ使い道はノープラン。。

<!--more-->
この作業にはまっていたせいか、インストールした目的を忘れかけてた...

↓を試そうとして svn export しようとしたら、svn コマンドがサーバになかったからでした。

<a href="http://start.typepad.jp/typecast/">TypePadの絵文字アイコン画像と、携帯表示モジュールをフリー（自由）ライセンスで公開</a>

