---
layout: post
date: 2006-03-16T03:00:00+09:00
title: 自分のホームディレクトリ内にPerlモジュールをインストール(Template-ToolKit編)
slug: cpantemplatetoolkit_1
tags:
- 日々
status: draft
type: post
published: false
meta: {}
---
以前に<a href="/blog/2005/11/cpan.html" title="wolog: CPANで自分のホームディレクトリ内にモジュールをインストール">CPANで自分のホームディレクトリ内にモジュールをインストール</a>したのですが、最近になって Template-Toolkit を試してみたいと思いました。そのときのメモです。

いつものように perl -MCPAN -e shell から test をやってみたけれど、なぜかうまくインストールできず。どうやらソースからやる必要がありそう。

<a href="http://www.sea-bird.org/doc/Solaris8/Perl_2.html" title="Template Toolkit について">Template Toolkit について</a>

↑を参考に、Template-Toolkit のソースをダウンロード＆展開し、INSTALL ファイルを軽く読んでみた後に以下を実行。
<blockquote>perl Makefile.PL LIB=~/perl/lib PREFIX=~/perl/lib INSTALLMAN1DIR=~/perl/man/man1 INSTALLMAN3DIR=~/perl/man/man3
make test
make install
</blockquote>
これで無事にインストールはできた模様。

（最初の実行で、Makefile.PL からいろいろ質問される。Stash::XSがうんたらかんたらっていうのも、一応 y と答えてみた。あと「ドキュメントとかはどこに置く？」みたいなことも聞かれたので、ホームディレクトリ内のパスを指定。）

TTが無事にインストールできれば、あとは CGI::Application や Catalyst とかのフレームワークも試せるかなーと。
