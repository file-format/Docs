{
  "date" : "2019-10-11",
  "keywords" :[ "dcm ファイル", "dcm ファイル形式", "dcm ファイルとは", "ファイル", "dcm の例", "dcm ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCM ファイル形式 - デジタル医療情報ファイル",
  "description":"DCM ファイル形式と,DCM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## .DCM オプション番号

拡張子が .dcm のファイルは、MRI、CT スキャン、超音波画像などの患者の医療情報を保存するデジタル画像を表します。 DCM ファイルは、[DICOM](/image/dicom) (医学におけるデジタル画像と通信) 画像ファイル形式を使用し、参照用に患者の情報を含めることができます。 [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) によって開発され、医療画像の配布と表示のための画像ファイル形式を標準化することを目的としていました。

## DCM ファイル形式

DCM ファイルは、情報を DICOM 画像形式で保存します。これらのファイルには、DICOM IOD に関連する SOP インスタンスを表す現実世界の情報であるデータ セットが格納されます。 DICOM ファイル メタ情報はファイルに格納され、その後に実際のデータ セットのバイト ストリームが続きます。

### DICOM ファイルのメタ情報 ##

すべての DICOM ファイルには、カプセル化されたデータ セットの識別情報ヘッダーが含まれています。
* 128 バイトのファイル プリアンブル
* 4 バイトの DICOM プレフィックス
* ファイルのメタ要素

このヘッダーは、すべての DICOM ファイルに必須です。

### ファイルのメタ要素 ###
|属性名|タグ|タイプ|属性の説明
---|---|---|---|
|ファイル プリアンブル|タグまたは長さフィールドなし|1|アプリケーション プロファイルまたは実装指定の使用に使用できる固定の 128 バイト フィールド。アプリケーション プロファイルまたは特定の実装で使用されない場合、すべてのバイトは 00H に設定されます。ファイル セット リーダーまたはアップデーターは、このプリアンブルの内容に依存して、このファイルが DICOM ファイルであるかどうかを判断してはなりません。
|DICOM プレフィックス|タグまたは長さフィールドなし|1|文字列「DICM」を含む 4 バイト。このプレフィックスは、このファイルが DICOM ファイルであるかどうかを認識するために使用することを目的としています。
|ファイル メタ情報グループの長さ|(0002,0000)|1|このファイル メタ要素 (値フィールドの終わり) からグループ 2 ファイル メタ情報の最後のファイル メタ要素までのバイト数
|ファイル メタ情報バージョン|(0002,0001)|1|これは、各ビットがこのファイル メタ情報ヘッダーのバージョンを識別する 2 バイト フィールドです。バージョン 1 では、最初のバイト値は 00H で、2 番目の値のバイト値は 01H です。この属性が 1 に設定された 2 番目のバイトのビット 0 (lsb) を持つメタ情報を含むファイルを読み取る実装は、ファイル メタ情報をこのPS3.10のバージョン。他のすべてのビットはチェックされません。
|メディア保管 SOP クラス UID|(0002,0002)|1|データ セットに関連付けられた SOP クラスを一意に識別します。メディアストレージに許可される SOP クラス UID は、PS3.4 - メディアストレージアプリケーションプロファイルで指定されています。
|メディアストレージSOPインスタンスUID|(0002,0003)|1|ファイルに配置され、ファイルメタ情報に続くデータセットに関連付けられたSOPインスタンスを一意に識別します。
|転送構文 UID|(0002,0010)|1|次のデータ セットをエンコードするために使用される転送構文を一意に識別します。この転送構文は、ファイル メタ情報には適用されません。
|実装クラス UID|(0002,0012)|1|このファイルとその内容を書き込んだ実装を一意に識別します。インターチェンジの問題が発生した場合に、ファイルを最後に書き込んだ実装のタイプを明確に識別します。
|実装バージョン名|(0002,0013)|3|最大 16 文字のレパートリーを使用して、実装クラス UID (0002,0012) のバージョンを識別します。
|ソース アプリケーション エンティティ タイトル|(0002,0016)|3|このファイルのコンテンツを作成した (または最後に更新した) AE の DICOM アプリケーション エンティティ (AE) タイトル。使用すると、メディア交換の問題が発生した場合にエラーの原因を追跡できます。
|個人情報作成者UID|(0002,0100)|3|個人情報(0002,0102)の作成者のUID。
|個人情報|(0002,0102)|1C|ファイル メタ情報に配置された個人情報を含みます。作成者は (0002,0100) で識別されます。 Private Information Creator UID (0002,0100) が存在する場合は必須。

### データセットのカプセル化 ###

DICOMファイルには、単一のSOPクラスに関連する単一のSOPインスタンスを表す単一のデータセットが含まれています。 DICOM ファイル メタ情報の転送構文 UID は、データ セットのエンコードに使用される転送構文を定義するものとします。

### ファイル管理情報のサポート ###

メディア フォーマット層は、所定の DICOM アプリケーション プロファイルに必要な場合、次のファイル管理情報を提供します。

* ファイル コンテンツ所有者の識別

* ファイルアクセス統計 (例: 作成日時)

* アプリケーション ファイルのアクセス制御

* 物理メディアのアクセス制御 (書き込み保護など)

## 参照 ##
※【DICOM規格】(https://www.dicomstandard.org/current/)
* [DICOM ファイル形式](http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)
