 しょぼい自動タグ付けエクステンション
======================================

 Summary
---------

設定ファイルに基づいて、ファイルの登録時などに自動的にタグ付けをするエクステンションです。
エクステンションがAutoTaggingに設定されていれば、画面に表示されていなくても自動的にタグ付けされます。

### 主な機能 ###

  * ファイル名を基にした自動タグ付け
    * 登録時・表示中のファイルへの適用
  * データベース別の設定ファイル
  * 簡易的な設定ファイルの編集画面


 Data File
-----------

### Syntax ###

ファイル名にマッチさせる正規表現を文字列にしたものをキー、追加するタグが要素の配列を値、としたオブジェクトをJSON形式で記述したもの。

    {
      "ファイル名にマッチさせる正規表現" : [
        "追加するタグ1"
      ],
      "ファイル名にマッチさせる正規表現" : [
        "追加するタグ1",
        "追加するタグ2",
        "追加するタグ3"
      ]
    }

  * 上から順にマッチングしていく
  * マッチングでは大文字小文字の違いは無視される


#### Sample ####

同梱の[AutoTagging.sample.json](./AutoTagging.sample.json)を参考にして下さい。


 Button
--------

### File Actions ###

#### Formatter ####

  テキストエリアの内容を整形して表示しなおす。

#### Reload ####

  設定ファイルを再読み込みしてテキストエリアに表示する。

#### Save ####

  テキストエリアの内容を設定ファイルに書き込む。


### Json Data ###

  設定ファイルの表示・編集用のテキストエリア。
  編集した内容は、Saveを押して保存しないと反映されません。


### Tag Actions ###

#### Select Apply ####

  選択中のファイルに自動タグ付けを適用する。

#### All Apply ####

  表示されている全てのファイルに自動タグ付けを適用する。


### Find Actions ###

  押すたびに検索状態を切り変える。

#### RegistDate ####

  * 今日登録されたファイル
  * 一週間以内に登録されたファイル
  * 一週間以上前から一ヶ月以内に登録されたファイル
  * 一ヶ月以上前に登録されたファイル

#### Tags ####

  * タグの付いていないファイル


 Option
--------

AutoTagging.htm自体を編集して下さい。

    // フルパスを対象にする(true) or ファイル名を対象にする(false)。 
    var FindFullPath = true;


 TODO
------

解決策募集中。

  * ドキュメント
  * デザイン
  * 中途で放置されたFind Actionsの再開位置
  * 他のFind Actionsの検索条件案


 System Requirements 
---------------------

  * Windows XP / 7
  * IE8
  * Whitebrowser 0.7.2.2


 Version
---------

### v2.0 (2010/05/26) ###

公開。

### v1.0 (2010/02/20) ###

完成。


 Thanks
--------

  * [268@Gt](http://www12.atwiki.jp/whitebrowser/)
  * [prototype.js](http://prototypejs.org/)
  * [blueprint](http://www.blueprintcss.org/)
  * [Iconic](http://somerandomdude.com/projects/iconic/)
  * [JsonFormatter.js](http://dara-j.asablo.jp/blog/2007/05/15/1509590)

<!-- vim: set sw=2 sts=2 ft=markdown : -->

