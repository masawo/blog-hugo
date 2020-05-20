---
layout: post
title: Imager のインストール@ubuntu
tags:
- 開発系
status: draft
type: post
published: false
meta:
  _edit_last: '1'
---
Perl用の画像処理モジュール Imager を Ubuntu Linux(9.10) に入れたので、メモ的にエントリーしてみるテストです。

以下を aptitude install

<blockquote>libjpeg62-dev libpng12-dev libgif-dev</blockquote>
したあと、Imager をインストール
<blockquote>cpanm Imager</blockquote>

#cpan -i でもいいんですが、cpanm が便利なので最近はすっかりこれです。

使える画像形式を確認するには以下。

<blockquote># perl -MImager -e 'print join ", ", sort keys %Imager::formats'
bmp, gif, ifs, jpeg, png, pnm, raw, tga</blockquote>

前述の各形式のライブラリを入れてないと gif jpeg png が出てきません。

足りないフォーマットのライブラリを後から追加して、それをImagerに対応させるには

<blockquote>cpanm -f Imager</blockquote>

でforce install すればOK。

これで縮小画像などを作ったりできます。

参考

- <a href="http://e8y.net/mag/012-imager/">use Imager; - 今日のCPANモジュール</a>
- <a href="http://it.kndb.jp/entry/show/id/2572">Perlの画像処理モジュールImagerのインストール方法 - Knowledge Database IT</a>
