{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "拡張子", "ファイル", "ファイル形式", "データベースファイルの種類", "データベースファイル形式", "データベースファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SQL ファイル形式と,SQL ファイルを作成して開くことができる API について学びます。",
  "title" :"SQL ファイル形式 - 構造化クエリ言語データ ファイル",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## SQL ファイルとは何ですか?

拡張子が .sql のファイルは、リレーショナル データベースを操作するコードを含む構造化照会言語 (SQL) ファイルです。データベースに対する CRUD (作成、読み取り、更新、および削除) 操作の SQL ステートメントを記述するために使用されます。デスクトップや Web ベースのデータベースで作業する場合、SQL ファイルは一般的です。 Java Persistence Query Language (JPQL)、LINQ、HTSQL、4D QL など、SQL の代替手段がいくつかあります。 SQL ファイルは、Microsoft SQL Server、MySQL のクエリ エディター、および Windows OS のメモ帳などのその他のプレーン テキスト エディターで開くことができます。

## 簡単な歴史

* 1970 年代初頭に IBM の Donal D. Chamberlin と Raymond F. Boyce によって開発および導入されました。
* IBM のオリジナルの準リレーショナル データベース管理システムである System R からデータを格納および取得するために使用されます。
* 1979 年、1981 年、1983 年にそれぞれ市販された System/38、SQL/DS、および DB2 を含む System R プロトタイプを使用して、商用製品ベースで使用され始めました。
* 1986 年までに、リレーショナル データベース管理システム (RDBMS) の標準「データベース言語 SQL」として ANSI および ISO 標準グループによって正式に採用されました。

## SQL ファイル形式

SQL ファイルはプレーン テキスト形式で、複数の言語要素で構成できます。複数のステートメントを相互に依存せずに実行できる場合は、1 つの SQL ファイルに複数のステートメントを追加できます。これらの SQL コマンドは、CRUD 操作を実行するためにクエリ エディターで実行できます。

### SQL 言語要素

SQL 言語の要素は次のとおりです。

|要素|説明|
---|---|
|条項|ステートメントとクエリの構成要素。|
|式|スカラー値、またはデータの列と行で構成されるテーブルを生成できます|
|述語| SQL 3 値論理 (3VL) (真/偽/不明) またはブール値の真偽値に評価できる条件を指定し、ステートメントとクエリの効果を制限したり、プログラム フローを変更したりするために使用します。|
|クエリ|特定の基準に基づいてデータを取得します。これは SQL の重要な要素です。|
|ステートメント|スキーマとデータに永続的な影響を与えたり、トランザクション、プログラム フロー、接続、セッション、または診断を制御したりする可能性があります。|

### SQL の例
次の SQL ステートメントは、**DATA** という名前のテーブルを作成し、その後に追加の `INSERT` コマンドを続けて、このテーブルにレコードを挿入します。
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## 参照 ##

* [ウィキペディアによる SQL](https://en.wikipedia.org/wiki/SQL)
* [SQL 構文](https://en.wikipedia.org/wiki/SQL_syntax)

