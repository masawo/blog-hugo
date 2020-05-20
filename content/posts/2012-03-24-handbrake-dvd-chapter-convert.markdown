---
layout: post
date: 2012-03-24T03:00:00+09:00
title: HandBrakeを使ってDVDをチャプターごとに動画変換する
slug: handbrake-dvd-chapter-convert
tags:
- チラシの裏
status: publish
type: post
published: true
meta:
  _edit_last: '1'
  has_been_twittered: 'yes'
  fb-status-updater-sn-reference: a:1:{i:0;a:2:{i:0;s:8:"facebook";i:1;s:24:"1301932082_3529978730458";}}
---
Mr.ChildrenのライブDVDを動画変換するために、表題の作業をMac版で行ったのでそのメモです。

(Windows版でもたぶん同様なのではとおもいます)

<a href="http://handbrake.fr/" title="HandBrake" target="_blank">HandBrake</a>

<a href="http://wo.skr.jp/images/uploads/2012/03/d0befdced14949441a76f8528ddbb9c2.jpg"><img src="http://wo.skr.jp/images/uploads/2012/03/d0befdced14949441a76f8528ddbb9c2.jpg" alt="" title="スクリーンショット 2012-03-24 16.34.58" width="987" height="666" class="alignnone size-full wp-image-429" /></a>

        1. ソースのファイルを指定（isoファイルや、マウントしたDVDとか）
        2. 画面の上のほうにチャプターが選べるプルダウンがあるので、そこを見る。
        連番になっていると思うので、まず1を2つ選択。（これで、チャプター1を範囲指定したことになる）
        3. ファイル保存先のところを、チャプター番号がわかるようにファイル名を修正する
        4. キューに追加する。英語版であれば "Add to Queue" ボタンを押す
        5. 2〜4をチャプターの数だけ繰り返す。
        6. キューに追加した処理を開始する。英語版であれば "Start"ボタン

開始するとこんな表示に。

<a href="http://wo.skr.jp/images/uploads/2012/03/f9c2249cbdc88303332f164438bcc624.jpg"><img src="http://wo.skr.jp/images/uploads/2012/03/f9c2249cbdc88303332f164438bcc624.jpg" alt="" title="スクリーンショット 2012-03-24 16.35.25" width="701" height="624" class="alignnone size-full wp-image-430" /></a>

これでmp4ファイルを生成しました。H.264で生成したので、Macはもちろん,iPhoneやiPadでもiTunesにアップロードして見られます。

とやっているうちに、ああ <a href="http://code.google.com/p/ps3mediaserver/">ps3mediaserver</a> とか使ってDLNA経由で再生するという手もあるなあ、と思いました。

<!--more-->
余談1

コンサートの類には滅多に行かない私ですが、Mr.Children はこの頃マイブーム（死語）で、 tour SENSE のBlu-rayを見て行きたくなりました。でもこないだの先行予約は2回とも敗北したので、縁がないですね。誰か連れて行ってくれるありがたい人いないかな〜。


余談2

ついでに忘備録として。。
<strong>Mac でのスクリーンショットの撮り方</strong>
- Command+Shift+3 で画面全体を撮影
- Command+Shift+4 で範囲選択カーソルが出る。さらにスペースを押すとウインドウ選択ができる
- <a href="http://inforati.jp/apple/mac-tips-techniques/system-hints/how-to-use-mac-screenshot-with-keyboard-shortcut.html">Macのスクリーンショット機能のキーボードショートカットまとめ（17種類） / Inforati</a>

撮った画像の編集は<a href="http://skitch.com/jp/">Skitch</a>でやりました。使いやすくて楽勝。
