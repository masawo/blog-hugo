---
layout: post
date: 2009-04-26T03:00:00+09:00
title: Delicious Bookmarks 2.1.034の罠
slug: delicious_bookmarks_21034
tags:
- 未分類
status: publish
type: post
published: true
meta: {}
---
家のMBPで使ってるFirefoxでいつのまにかブックマークができないという罠になっていたので、何が原因なのか追求しました。

各設定のバックアップ＆復元ができる<a href="https://addons.mozilla.org/ja/firefox/addon/2109">FEBE</a>を入れて（今回初めて知った。。便利）、アドオンのバックアップを取ったりProfileをバックアップしてFirefox起動。

        アドオンがまっさらな状態だと問題なくブックマークできる
        ↓
        バックアップしたアドオンを入れなおしてみたら、ブックマークできない。。
        ↓
        これはもうアドオンのせいね、ということでまず Delicious Bookmarks を疑う。無効化
        ↓
        ビンゴ。ブックマークできた！

どうもそれまで入れていた Delicious Bookmarks のバージョンが 2.1.034 なのですが、これが地雷だったんですね。。

<a href="https://addons.mozilla.org/ja/firefox/reviews/display/3615">Delicious Bookmarks のレビュー :: Firefox Add-ons</a>を見ると3/28あたりからそんな投稿が。

これを書いた時点での最新は2.1.018で、これなら問題ない感じ。

最新のアドオンを頭ごなしに入れてると、まれにこんな罠になる可能性もあるんだなってことを実感しました。
