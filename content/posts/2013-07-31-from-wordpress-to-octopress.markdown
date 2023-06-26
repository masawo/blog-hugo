---
layout: post
date: 2013-07-31T03:00:00+09:00
title: "WordpressからOctopressに移行"
slug: from-wordpress-to-octopress
date: 2013-07-31T22:03:00+09:00
comments: true
---
7月の始めごろに、このブログを Wordpress から Octopress に移行していました。

移行した理由は主に

- Wordpress がレンタルサーバ上で動いているため表示に時間がかかりがちで、開くだけでもストレス
- 管理画面でも同様なので、書く気が萎えがち(それで更新も億劫になっていた)

という感じです。

<!--more-->

他のブログサービスへの移転も考えましたが、

- これまでのURLをなるべく生かしたい
- OctopressはRubyで作られているので,PHPなWordpressよりはいじり甲斐がありそう
- 静的なHTMLにすれば表示速度は最強だろう

と思い、Octopressへの移行をしました。

## データの移行

- http://octopress.org/docs/  
- http://jekyllrb.com/docs/migrations/  

を見ながら、WPの管理画面でexportしたXMLでデータのmigrationを実施。

※ https://github.com/benbalter/wordpress-to-jekyll-exporter
でWP管理画面からzipに落とせるみたいだけど、うまく動かず。

## 記事の調整

あとは生成された記事のファイル名を .html -> .markdown に変えて（スクリプト作ってrenameしました）、あとは記事1つ1つを確認しつつ調整。  
Octopress では記事を markdown の記法で書くので、"改行するのは行末に空白2つ" などの書き方を覚えるのに若干手間取りつつ進行。  
こんな過疎ブログでも300件程度の記事があったので、空いた時間に少しずつ進めていくようにして、数日かかって完了しました。

画像パスを
wp/wp-content/uploads -> images/uploads
に変えるところはエディタ(Sublime Text)で一斉置換しました。  
（後から考えると .htaccess にパス移動仕込めば済む話だったかも）

### 記事全体の生成

    $ rake generate

### 新しい記事の作成

    $ rake new_post["title"]

## 旧URLからのredirect

各記事のURLが /wp/some_entry.html から /blog/some_entry.html へ変更になるので、 新URLへ移動するよう .htaccess に設定。

    Redirect permanent /wp/atom.xml http://wo.skr.jp/atom.xml
    RedirectMatch permanent /wp/(.*) http://wo.skr.jp/blog/$1

301 Redirect Parmanent にするので、SEO的にも安心（たしか）。

## deploy

Octopressは静的なファイルたちを生成するので、それをアップするだけです。  標準では設定を少し書けばrsyncでファイルを送れるようになっているので、 [Deploying with rsync - Octopress](http://octopress.org/docs/deploying/rsync/) の通りにするだけ。

    $ rake deploy

で、自分の場合は30秒もかからず反映が終わります。  
さくらのレンタルサーバだと rsync が使えるので良かったですが、使えないサーバだとやっかいかも。

## デザインの調整

テーマというものを導入すると、デザインが簡単に変えられます。  
以下でいろいろ探してみました。  
[3rd Party Octopress Themes · imathis/octopress Wiki](https://github.com/imathis/octopress/wiki/3rd-Party-Octopress-Themes)

で、以下のテーマにしました。  
https://github.com/wallace/justin-kelly-theme

あとは source/_includes 以下のファイルを主にいじって、以下のような変更をしました。基本的にHTML。

- [Octopress - Facebook OGP 設定！ - mk-mode BLOG](http://www.mk-mode.com/octopress/2012/12/31/octopress-facebook-ogp/)
- [OctopressのサイドバーにTwitterのタイムラインを埋め込む - MSaiSai's Blog](http://msaisai.github.io/blog/2013/06/19/octopress-twitter/)
- Facebook Like, Disqus の設定
- はてなブックマークのボタン
- Google Adsenseとか

## 移行後1ヶ月経ってみて

月末近くになって、ようやく一通り調整が済んだかなあというところです。  
ブログ用にどこかVPS的なサーバを別に借りるべきかと思っていましたが、そこまでするのもなあと思ってました。引き続きレンタルサーバのスペースを生かせるし、レスポンス問題も解決できたのでひとまず満足です。 

アクセス数は特に変化ないんですが、少なくとも表示まで時間がかかるストレスは解消されたはずなので、あとは本人がまめに記事を書くだけ。。汗

