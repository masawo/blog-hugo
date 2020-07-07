---
title: "meishi2 に Google Meet のショートカットを設定する(macOS)"
slug: meishi2-google-meet-shortcut
date: 2020-06-28T21:06:10+09:00
draft: false
---

自作キーボードを初めて作るにあたって、練習用に meishi2 を作りました。
<img src="/images/IMG_0779.jpg">

[G Suite のキーボード ショートカットを使用する - Google Meet ヘルプ](https://support.google.com/meet/answer/9298571?hl=ja&ref_topic=7294099)  
これによると、ショートカットキーは以下になっている

- カメラのオンとオフを切り替える	⌘+e または Ctrl+e
- マイクをミュートまたはミュート解除する	⌘+d または Ctrl+d

QMKで提供されているファームウェアのデフォルトはCtrlキーでの組み合わせになっている。Windowsだとそのまま使えるっぽいけど、今回はmacOSなので ⌘ のほうで設定する必要がある。

QMK Configurator でカスタムする。  
https://config.qmk.fm/#/meishi2/LAYOUT
を開いて、画面下のパレットから適切に選んでキーマップを設定する。

Quantum のタブを開くと Mod key combinations という項目があり、⌘ に該当するのは LGui 。なのでそれを上のキーマップのところにドラッグ&ドロップして、そのあと D や E をその上にドラッグ&ドロップ。
<img src="/images/ISOJIS.png">

余っている2つには +c, +v を置いた。

<img src="/images/qmk_200628.png">

そのあと COMPILE を選んでコンパイル。  
下のFIRMFAREのところが選択可能になるので、これを選んでhexファイルをダウンロードできる。
あとはこのhexファイルを使って QMK toolkit で書き込めば完了。  

ファームウェア書き込みはCUIでも使うのかと思っていましたが、GUIですべて完了できたのでわりとお手軽でした。  
これで Google Meet するときに meishi2 をつなげば、音声やカメラのOn/Offが捗りそうです。

本番で作ったキーボードについてはまた改めて書こうと思います。HHKBでできていた Volume Up/Down, Mute が効くようにファームウェア書き込みしたりしました。

JSONファイルをエクスポートしておくと、あとからインポートすることで設定を再現できるのでやっておくと吉。(今回は4つしかキーがないのでそこまで意味ないかも)


