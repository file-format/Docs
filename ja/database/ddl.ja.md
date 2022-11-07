{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "拡張子", "ファイル", "ファイル形式", "データベースファイルの種類", "データベースファイル形式", "データベースファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DDL ファイル形式と,DDL ファイルを作成して開くことができる API について学びます。",
  "title" :"DDL ファイル形式 - データ定義言語ファイル",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## .DDL ファイルとは?

拡張子が .ddl のファイルは、データベースのスキーマを定義するために使用されるデータ定義言語ファイルです。テーブル、列、レコード、その他のフィールドなどのデータベース構造を操作するためのステートメント/コマンドが含まれています。 DDL ファイル内のコマンドは [SQL](/database/sql/) で記述され、データベース内のテーブルの作成、削除、更新などの操作を実行できます。データベース スキーマは作成者によって所有され、すべての CRUD 操作を実行できます。 DDL ファイルを作成して開くことができる一般的なアプリケーションは、Windows Text Editor、Jetbrains Intellij Idea、および EclipseLink です。

## DDL コマンド

1 つの DDL ファイルに複数のコマンドを含めることができます。これらのコマンドは、構文が正しいため、順番に実行され、文字セットとテーブルの作成、テーブルの削除、テーブルの名前変更と変更などのスキーマに変更を加えます。次の DDL コマンドは、データベース スキーマの操作中によく使用されます。

`CREATE` - データベースまたはそのオブジェクト (テーブル、インデックス、関数、ビュー、ストア プロシージャ、トリガーなど) を作成するために使用されます。

`DROP` – データベースからオブジェクトを削除するために使用されます。

`ALTER` - データベースの構造を変更するために使用されます。

`TRUNCATE` – テーブルからすべてのレコードを削除するために使用され、レコードに割り当てられたすべてのスペースが削除されます。

COMMENT – データ ディクショナリにコメントを追加します。

`RENAME` – データベース内の既存のオブジェクトの名前を変更します。

## DDL の例

次の例は、テーブルを作成し、そのフィールドを定義する CREATE コマンドの DDL ステートメントを示しています。

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## 参照 ##

* [ウィキペディアによる DDL](https://en.wikipedia.org/wiki/Data_definition_language)

