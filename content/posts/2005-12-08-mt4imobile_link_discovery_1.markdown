---
layout: post
date: 2005-12-08T03:00:00+09:00
title: mt4i設置&Mobile Link Discovery対応
slug: mt4imobile_link_discovery_1
tags:
- 日々
status: publish
type: post
published: true
meta: {}
---
<p><a href="http://www.sixapart.jp/docs/tech/mobile_link_discovery_ja.html" title="Six Apart - Docs: Mobile Link Discovery 仕様">Mobile Link Discovery</a>という仕様が Six Apart のmiyagawaさんによって策定されました。<br /> <a href="http://blog.bulknews.net/mt/archives/001863.html" title="Where's your Mobile URL?: blog.bulknews.net">Where's your Mobile URL?: blog.bulknews.net</a>  <br /><br />MTユーザの方におあつらえ向きなモバイル対応化アプリとして、<a href="http://www.hazama.nu/pukiwiki/index.php?MT4i">mt4i</a>があります。<br />本blogをその<a href="http://www.hazama.nu/pukiwiki/index.php?MT4i">mt4i</a>によってモバイル対応にするいい機会だなと思ったので、上記の仕様に対応する例としてさっそくやってみました。  </p><ul><li>mt4iをインストール（非常にスムーズに導入できます。感謝）</li><li>MTの管理画面を開き、[テンプレート]でメインページを編集する画面にして以下を&lt;head&gt;タグ内に追加<br />&lt;<span class="start-tag">link</span><span class="attribute-name"> rel</span>=<span class="attribute-value">&quot;alternate&quot; </span><span class="attribute-name">media</span>=<span class="attribute-value">&quot;handheld&quot; </span><span class="attribute-name">type</span>=<span class="attribute-value">&quot;application/xhtml+xml&quot; </span><span class="attribute-name">href</span>=<span class="attribute-value">&quot;/blog/mt4i.cgi&quot; </span><span class="attribute-name">/</span>&gt;<br /></li><li>サイトを再構築した後、miyagawaさん謹製の<a title="Mobile Link Discovery Validator" href="http://blog.bulknews.net/mobilelink-validator.cgi">Mobile Link Discovery Validator</a>にブログのURLを投入し、LINKタグで仕込んだモバイル用URLが出てくれば対応完了</li></ul><p>ごらんの通りけっこう簡単です。まあ一例ということで。</p>
