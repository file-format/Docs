{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - TrueType コレクション ファイル形式",
  "description":"TrueType コレクション (TTC) ファイルは,複数のフォントを 1 つのファイルに結合します。Apple と Microsoft の両方が,Mac および Windows オペレーティング システムで TTF を使用しました。",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## .TTC オプション番号
TrueType Collection は True Type 形式の拡張であるため、TTC は省略されます。 TTC ファイルは、複数のフォント ファイルを結合できます。これらのファイルは、多くのグリフを共有する複数のフォントを組み合わせるのに役立ちます。 Windows 2000 より前は、TTC ファイルは中国語、日本語、および韓国語版の Windows で使用されていましたが、その後、すべての地域でサポートが利用できるようになりました。


## フォントコレクションファイルの構造
TTC ファイルは、TTC ヘッダー テーブル、テーブル ディレクトリ、および複数の OpenType テーブルで構成されます。 TTC ヘッダーは、ファイルの先頭にある必要があります。各フォントの完全なテーブル ディレクトリが存在する必要があります。 TableDirectory 形式は、非コレクション ファイルに存在するものと同様である必要があります。 TTC ファイル内のすべてのディレクトリのテーブル カウントは、TTC ファイルの先頭から計算されます。
TTC ファイル内のテーブルは、それぞれのフォントのテーブル ディレクトリから参照されます。 OpenType テーブルのいくつかは、TTC に追加されたフォントごとに 1 回、複数回表示する必要があります。他のテーブルは、TTC ファイル内の複数のフォントによって共有される場合があります。

### TTC ヘッダー
これまでのところ、TTC ヘッダー テーブルの 2 つのバージョンが利用可能です。
- バージョン 1.0 は、デジタル署名のない TTC ファイルに使用されます。
- バージョン 2.0 は、デジタル署名の有無にかかわらず TTC ファイルに使用できます。
両方のバージョンの TTC ヘッダー テーブルを次に示します。

**TTC ヘッダー バージョン 1.0:**

|タイプ|名前|説明|
---|---|---|
|TAG|ttcTag|フォント コレクション ID 文字列: 'ttcf' (CFF または CFF2 アウトラインと TrueType アウトラインを含むフォントに使用)|
|uint16|majorVersion|TTC ヘッダーのメジャー バージョン = 1.|
|uint16|minorVersion|TTC ヘッダーのマイナー バージョン = 0.|
|uint32|numFonts|TTC のフォント数|
||Offset32|tableDirectoryOffsets[numFonts]|ファイルの先頭から各フォントの TableDirectory までのオフセットの配列|

**TTC ヘッダー バージョン 2.0:**

|タイプ|名前|説明|
---|---|---|
|TAG|ttcTag |フォント コレクション ID 文字列: 'ttcf'|
|uint16| majorVersion |TTC ヘッダーのメジャー バージョン = 2.|
|uint16| minorVersion |TTC ヘッダーのマイナー バージョン = 0.|
|uint32| numFonts |TTC のフォント数|
|オフセット32| tableDirectoryOffsets[numFonts] |ファイルの先頭から各フォントの TableDirectory までのオフセットの配列|
|uint32| dsigTag |DSIG テーブルが存在することを示すタグ、0x44534947 ('DSIG') (署名がない場合は null)|
|uint32| dsigLength |DSIG テーブルの長さ (バイト単位) (署名がない場合は null)|
|uint32| dsigOffset |TTC ファイルの先頭からの DSIG テーブルのオフセット (バイト単位) (署名がない場合は null)|

## 参考文献
* [OpenType フォント ファイル](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (ウィキペディア)](https://en.wikipedia.org/wiki/TrueType)

