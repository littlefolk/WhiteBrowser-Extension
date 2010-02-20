 しょぼい自動タグ付けエクステンション
======================================

 Summary
---------

設定ファイルに基づき、ファイルの登録時などに自動的にタグ付けをするエクステンションです。
WhitebrowserでエクステンションをAutoTaggingに設定しておけば、表示されていなくても動きます。

### 主な機能 ###

  * 登録時にファイル名を基にした自動タグ付け
  * 表示中のファイルへの適用
  * 簡易的な設定ファイルの編集環境
  * タグ付け用検索候補


 Button
--------

### Json Data ###

設定ファイルの表示・編集用のテキストエリア。


### File Actions ###

設定ファイルの再読み込み・保存。

#### Formatter ####

テキストエリアの入力を整形して表示。

#### Reload ####

ファイルを再読み込みしてテキストエリアに表示。

#### Save ####

テキストエリアで編集したものをファイルに書き込む。


### Tag Actions ###

登録済みのファイルに自動タグ付けを適用する。

#### Select Apply ####

選択中のファイルに適用する。

#### All Apply ####

表示されている全てのファイルに適用する。


### Find Actions ###

押すたびに検索状態を切り変える。

#### RegistDate ####

  * 今日登録されたファイル
  * 一週間以内に登録されたファイル
  * 一週間以上前から一ヶ月以内に登録されたファイル
  * 一ヶ月以上前に登録されたファイル

#### Tags ####

  * タグ無し


 Data File
-----------

### 保存場所 ###

Whitebrowser本体のあるフォルダ\temp\AutoTagging.WBファイル名.json

### 書式 ###

設定ファイルはJSONフォーマットで記述され、全体としては一つのオブジェクトとして書かれる。

    {}

    // "cat and dog.mpg" => []

オブジェクトのキーにはファイル名とマッチングさせる文字列を書き、値には書きこまれるタグの文字列を配列で書く。

    {
      "cat" : ["猫"]
    }

    // "cat and dog.mpg" => ["猫"]

オブジェクトのペアが複数ある場合は上から順にマッチングしていく。

    {
      "dog" : ["犬"],
      "cat" : ["猫"]
    }

    // "cat and dog.mpg" => ["犬", "猫"]

キーの文字列は正規表現として解釈される。
また大文字小文字の違いは無視される。

    {
      "dog" : ["犬"],
      "cat" : ["猫"],
      ".*" : ["ファイル"]
    }

    // "cat and dog.mpg" => ["犬", "猫", "ファイル"]
    // "DOGDOGDOG.flv"   => ["犬", "ファイル"]
    // "Pig.avi"         => ["ファイル"]


 Option
--------

AutoTagging.htm自体を編集して下さい。

    // フルパスを対象にする(true) or ファイル名を対象にする(false)。 
    var FindFullPath = true;
    // エラーメッセージをポップアップで表示、する(true) or しない(false)。
    var ErrorMessagePopup = false;


 TODO
------

解決策募集中。

  * デザイン
  * テキストエリアのリサイズ
      * http://espion.just-size.jp/archives/06/237175908.html
      * http://p2b.jp/200903-autofit-textarea
      * http://www.switchonthecode.com/tutorials/javascript-controls-resizeable-textbox-part-tres
  * 中途で放置されたFind Actionsの再開位置
  * 他のFind Actionsの検索条件案


 Version
---------

### v1.0 (2010/02/20) ###

完成。


 Thanks
--------

  * [268@Gt](http://www12.atwiki.jp/whitebrowser/)
  * [prototype.js](http://prototypejs.org/)
  * [blueprint](http://www.blueprintcss.org/)
  * [Iconic](http://somerandomdude.com/projects/iconic/)
  * [JsonFormatter.js](http://dara-j.asablo.jp/blog/2007/05/15/1509590)

