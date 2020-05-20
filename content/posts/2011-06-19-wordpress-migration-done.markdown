---
layout: post
date: 2011-06-19T03:00:00+09:00
title: wordpressへの移行done
slug: wordpress-migration-done
tags:
- 日々
status: publish
type: post
published: true
meta:
  _edit_last: '1'
  has_been_twittered: failed
  twitter_failure_code: '401'
  twitter_failure_reason: Invalid / expired Token
---
開いた時間にちまちま進めていたwordpressへの移行が、ようやくひと通り終わりました。

参考にしたもの

- <a href="http://www.ideaxidea.com/archives/2008/12/movabletypewordpress.html ">固定リンクを変えずにスムーズにMovableTypeからWordPressに移行するまでの作業ログ | IDEA*IDEA</a>
- <a href="http://www.msng.info/archives/2010/11/what-i-did-to-switch-from-mt-to-wp.php">Movable TypeからWordPressへの移行に際してやったことまとめ - 頭ん中</a>

MT時代にいくつか下書きしたままの投稿があったので、WP側のDBのpermalinkパラメータをいじる件はちょっと手間でした（欠番をよしなに直さないといけなかった）。

後者の Search Regex プラグインが、移行時のコンテンツ置換がさくっとできて神でした。

これまでの /mt/ にきたアクセスは /wp/ に移動されます。

<code>
RedirectMatch permanent /mt/(.*) http://wo.skr.jp/wp/$1
</code>

一部permalinkがまだ不整合なところもあるけれど、気づいたところから直していきます。。


<!--more-->

Google Analytics をプラグイン設定したついでに現況を見てみたら、このブログの一番人気は
<a href="http://wo.skr.jp/wp/2009/05/psp-2000.html">PSP-2000のアナログスティック交換</a>でした。ううむ。
