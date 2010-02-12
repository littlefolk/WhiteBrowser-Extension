 しょぼいタグ入力支援エクステンション
======================================

 Summary
---------

テキストボックスに書かれたタグを選択中のファイルに追加する。
その際に選択中のファイルと似たファイルに付けられたタグを候補として提示します。
ファイルの複数選択や、半角コンマで区切って複数タグが付けれたりもできます。


 Button
--------

### Save

テキストボックスにつけられたタグを、選択したファイルに追加。

### Get

候補の探索範囲を広げて再検索。
押せば押すほど探索範囲を広げるので押しすぎ注意。

### Include

選択中のファイルにつけられたタグをテキストボックスに自動入力。


 Option
--------

TagInputRelation.htm自体を編集して下さい。

    // Saveした後にテキストボックスを空っぽに、する(true) or しない(false)。
    var SaveAfterReset = true; 
    // 既にテキストボックスに入力されたタグは候補に、出す(true) or 出さない(false)。
    var InputDuplication = false;
    // 類似検索範囲の初期値。
    var GetRelationLimit = 20;  


 TODO
------

解決策募集中。

*   テキストボックスに入りきらない
*   テキストボックスから削除
*   高速化
*   prototype.js version1.5


 Version
---------

### v3.0 (2010/02/12)

全面書き直し。

*   デザイン変更
    *   [blueprint](http://www.blueprintcss.org/)
    *   [Iconic](http://somerandomdude.com/projects/iconic/)
*   input復活
*   prototype.jsのversion1.6.1を同梱

### v2.1.1 (2009/12/30)

prototype.jsのversion1.6以上を必要としてたのを修正。

### v2.1 (2009/12/26)

手動入力を追加。

### v2.0 (2009/12/22)

書き直し。

*   デザイン変更
*   input廃止

### v1.0 (2009/12/12)

公開。


 Thanks
--------

*   [268@Gt](http://www12.atwiki.jp/whitebrowser/)
*   [prototype.js](http://prototypejs.org/)
*   [blueprint](http://www.blueprintcss.org/)
*   [Iconic](http://somerandomdude.com/projects/iconic/)

