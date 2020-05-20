---
layout: post
title: 自宅サーバのダイナミックDNSを変更 everydns->mydns.jp
tags:
- サーバー
status: publish
type: post
published: true
meta:
  _edit_last: '1'
  has_been_twittered: 'yes'
---
<a href="http://wo.skr.jp/images/uploads/2011/09/screenshot.png"><img src="http://wo.skr.jp/images/uploads/2011/09/screenshot-300x176.png" title="everydns終了のお知らせ画面" width="300" height="176" class="alignnone size-medium wp-image-398" /></a>

自宅サーバを公開するためにダイナミックDNSサービスとして <a href="http://everydns.net">everydns.net</a> を利用していたんですが、結構前にdyndnsに接収されており、8/31で完全終了されるとのこと。

dyndnsに移行してねみたいなメールが何度も来ていたんですが、いつかやろうやろうとスルーしていたら当日になってしまいました。なので慌ただしく移転先を探すことに。

探した結果、<a href="https://www.zoneedit.com">zoneedit</a> をはじめに見つけたのですが、国産で <a href="http://www.mydns.jp/">mydns.jp</a> というところがあることがわかり、そちらを利用してみることに。

自分が唯一持っている独自ドメインをとりあえず、設定してみました。ベータ版の新サイトがあるとのことなので、そちらで設定。
レジストラ側のネームサーバ設定も、さくらインターネットの管理画面に入って変更。

dig @ns0.dix.asia <em>ドメイン名 </em>などとしてとりあえず名前が引けることは確認したので、あとはDNSの浸透待ちです。

今のところ独自ドメインを使ったコンテンツはほとんどない（開発のテストに使ったりしていて、公開してるものがない）ので、少々時間がかかっても無問題。
