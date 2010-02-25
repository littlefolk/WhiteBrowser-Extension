 しょぼいタグクラウドエクステンション
======================================

 Summary
---------

表示しているファイルからタグクラウドを作成します。
タグクラウドの見栄えを複数のCSSから選択・変更することが出来ます。


 Buttons
---------

### ![AutoFollow Start](./icon/play_alt_24x24.png) ![Stop](./icon/minus_alt_24x24.png) ###

画面が変更される度に自動的にタグクラウドが更新されるようになり、もう一度押されるとストップする。

### ![Clear](./icon/home_24x24.png) ###

現在の検索内容を消去して、最初の画面に戻る。

### ![Update](./icon/reload_24x28.png) ###

タグクラウドを作成しなおす。


 Option
--------

SimpleTagCloud.htm自体を編集して下さい。
タグクラウドの表示例は[Tag Cloudのスタイル](http://3ping.org/2007/10/20/1428)を参考にして下さい。

    // タグクラウドの見栄えを変更する。
    // CSSのファイル名(tagCloud_01.css)の数値を変更する(01から13まで)。
    <link type="text/css" rel="stylesheet" href="./skin/tagCloud_01.css">

    // 先頭から最大何個のファイルをタグクラウド作成のデータとして調べるか。
    var SearchFileLimit = 2500;
    // ファイルのタグ更新時にタグクラウドを更新、する(true) or しない(false)。
    var ModifiedUpdate = false;


 TODO
------

解決策募集中。

  * CSSの切り替えフォーム
  * シャッフルして表示
  * タグ情報のキャッシュ
  * タグクラウド作成アルゴリズム
  * 時間軸の導入


 System Requirements 
---------------------

  * Windows XP / 7
  * IE8
  * Whitebrowser 0.7.2.2


 Version
---------

### v2.0 (2010/02/26) ###

全面書き直し

  * タグクラウドの見栄えを複数のCSSから選べるように
    * CSSに[Tag Cloudのスタイル](http://3ping.org/2007/10/20/1428)を使用
    * 改行時の見栄えを変更([タグクラウドの日本語文字の改行を制御したい](http://p2b.jp/200912-tagcloud-with-word-break-and-white-space))
  * モードの廃止
  * ボタンをアイコンに変更
    * [Iconic](http://somerandomdude.com/projects/iconic/)を使用
  * ドキュメントの形式を変更
  * prototype.jsのversion1.6.1を同梱

### v1.2.1 (2009/12/27) ###

半角文字の折り返し処理

### v1.2 (2009/12/27) ###

コメントを参考に、タグクラウド作成のタイミングを変更

  * 呼び出し時
  * タグ更新時
  * メイン画面更新時(followモード)

### v1.1 (2009/12/20) ###

prototype.jsが最新で無い場合にエラーが出てたのを修正しました

### v1.0 (2009/12/19) ###

公開


 Thanks
--------

  * [268@Gt](http://www12.atwiki.jp/whitebrowser/)
  * [prototype.js](http://prototypejs.org/)
  * [Iconic](http://somerandomdude.com/projects/iconic/)
  * [タグクラウドのフォントサイズの計算式について - Open MagicVox.net](http://www.magicvox.net/archive/2008/04091135/)
  * [Tag Cloudのスタイル](http://3ping.org/2007/10/20/1428)
  * [タグクラウドの日本語文字の改行を制御したい](http://p2b.jp/200912-tagcloud-with-word-break-and-white-space)

<!-- vim: set sw=2 sts=2 ft=markdown : -->

