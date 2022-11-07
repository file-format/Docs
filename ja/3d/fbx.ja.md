{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "ファイル", "拡張子", "形式", "3Dファイル形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FBX ファイルとは何か,およびそれらを作成して開くことができる API を知るためのファイル形式ガイド。",
  "title" :"FBX - FilmBox 3D ファイル形式",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .FBX ファイルとは?

FBX (FilmBox) は、MotionBuilder 用に Kaydara によって最初に開発された、人気のある 3D ファイル形式です。 2006 年に Autodesk Inc に買収され、現在では多くの 3D ツールで使用されている主要な 3D 交換フォーマットの 1 つです。 FBX は、バイナリ ファイル形式と ASCII ファイル形式の両方で利用できます。この形式は、デジタル コンテンツ作成アプリケーション間の相互運用性を提供するために確立されました。 FBX ファイル フォーマットとの間の変換に使用できるツールは多数あります。

## FBX ファイル形式 - 詳細情報

FBX は独自の形式であり、そのバイナリ ファイル形式に関する仕様は公式には入手できません。 C++ FBX SDK は、FBX ファイルの読み取り、書き込み、および変換用にオートデスクから提供されています。 FBX 用の Python インポートおよびエクスポート スクリプトは、FBX SDK を使用しない Blender ソフトウェアでも利用できます。

### テキストベースのファイル構造

テキストベースのファイル構造は、明確に名前が付けられた識別子で文書化されたツリー構造です。これは、階層に配置されたネストされたノードのリストで構成され、各ノードには次のものがあります。

* NodeType 識別子 (クラス名)
* それに関連付けられたプロパティのタプル。タプル要素は通常のプリミティブ データ型です: ##float、integer、string## など。
* 同じ形式のノードを (再帰的に) 含むリスト。

これらは、次のように論理的に表すことができます。

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

標準ノードの一部は、各項目がネストされたリストで構成される暗黙的なリストとして定義されています。 FBX ジオメトリにアクセスするアプリケーションは、これらのコンテンツを解析し、有用な意味を持たせる必要があります。テキストベースの FBX ファイルの例を以下に示します。

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## FBX ファイルのバイナリ ファイル構造

前述のとおり、FBX のファイル形式の仕様は公開されていません。 Blender Foundation は、会社が提供する SDK を使用せずに FBX ファイル形式を実装しているため、バイナリ ファイル形式に関する詳細の一部は [入手可能](https://code.blender.org/2013/08/fbx-binary-file-format -仕様/) 実装の一部として。

バイナリ ファイルの構造は、次の順序に従います。

* ヘッダー
* オブジェクト レコード
* フッター

### FBX ヘッダー

ファイル ヘッダー情報は 27 バイトで構成されます。

* バイト 0 ～ 20: Kaydara FBX Binary \x00 (ファイル マジック、最後に 2 つのスペース、次に NULL ターミネータ)。
* バイト 21 ～ 22: [0x1A, 0x00]## (不明ですが、観測されたすべてのファイルがこれらのバイトを示しています)。
* バイト 23 ～ 26: unsigned int、バージョン番号。たとえば、バージョン 7.3 の場合は 7300 です。

### オブジェクト レコード ###

ヘッダーの後には、空の名前と空のプロパティ リストを持つ完全なノード レコードであるオブジェクト レコードが続きます。ファイル形式全体が再帰的に含まれます。

### フッター ###

FBX フッター セクションは、内容が不明なファイルの最後にあります。

## レコード形式 ##

FBX ファイル内のレコードは、次のように分類されます。

* ノード レコード
* 財産記録

### ノード レコードの形式 ###

各ノード レコード フォーマットには名前が付けられており、次のメモリ レイアウトがあります。


|サイズ (バイト)|日付タイプ|名前
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|NameLength|char|名前
|?|?|Property[n]、ここで n = 0:PropertyListLen
|オプション| | |
|?|?|ネストされたリスト
|13|uint8[]|ヌルレコード

どこ：

* `EndOffset` は、ファイルの先頭からノード レコードの末尾までの距離です (つまり、次に来るものの最初のバイト)。これを使用して、不明または不要なレコードを簡単にスキップできます。
* `NumProperties` は、ノードに関連付けられた値のタプル内のプロパティの数です。最後の要素としてネストされたリストは、プロパティとしてカウントされません。
* `PropertyListLen` はプロパティ リストの長さです。これは、##NumProperties## プロパティを格納するために必要なサイズであり、プロパティのデータ型によって異なります。
* `NameLen` はオブジェクト名の長さ (文字数) です。これが 0 になる唯一のケースは、トップレベルのリストのようです。
* `Name` はオブジェクトの名前です。ゼロターミネーションはありません。
* `Property[n]` は n 番目のプロパティです。フォーマットについては、セクション プロパティ レコード フォーマットを参照してください。プロパティはパディングなしで順番に書き込まれます。
* `NestedList` はネストされたリストであり、その存在は最後の NULL レコードによって示されます。

ネストされたリスト エントリの存在は、EndOffset に達するまでにバイトが残っているかどうかを確認することで判断できます。その場合、次のオブジェクト レコードは、最後のプロパティの直後に読み取られる必要があります。次に、オブジェクト レコードが 13 個のゼロ バイトに続き、これが EndOffset と組み合わされます。 NULL エントリの目的または要件は不明であり、何らかの形式機能を示している可能性があります。

### プロパティ レコードの形式 ###

プロパティ レコードには、ノードの一部であるプロパティに関する詳細が含まれています。プロパティ レコードには、次のメモリ レイアウトがあります。


|サイズ (バイト)|データ型|名前
--- | --- | ---
|1|char|TypeCode
|?|?|データ

TypeCode は、同様の処理が必要なグループで順序付けられた文字コードを表します。 TypeCode は次の種類に分類でき、TypeCode はこれらの種類のうちのいずれかの文字コードです。

#### プリミティブ型 ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

プリミティブ スカラー型レコードのデータは、リトルエンディアン バイト順の値の正確なバイナリ表現です。

#### 配列型 ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

配列型のデータはより複雑で、次の構造になっています。


|サイズ (バイト)|データ型|名前
--- | --- | ---
|4|Uint32|配列の長さ
|4|Uint32|エンコーディング
|4|Uint32|圧縮された長さ
|?|?|目次

### 特別なタイプ ###

以下は特殊なタイプの TypeCode です。

```
S: String
R: raw binary data
```

これらの TypeCode は両方とも次のように表されます。


|サイズ (バイト)|データ型|名前
--- | --- | ---
|4|Uin32|長さ
|長さ| | |

文字列は 0 で終了せず、\0 文字が含まれている可能性があります (これは実際には一部の FBX プロパティで使用されます)。

## 参照 ##

* [FBX - Autodesk SDK](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
※【FBXバイナリファイルフォーマット仕様書】(https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - ウィキペディア](https://en.wikipedia.org/wiki/FBX#File_format)

