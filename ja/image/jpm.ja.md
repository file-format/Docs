{
  "date" : "2019-11-25",
  "keywords" :["jpmファイル","jpmファイル形式","jpmファイルとは","ファイル","jpm例","jpmファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - JPEG 2000 複合ファイル形式",
  "description":"JPM ファイル形式と,JPM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## .JPM オプション番号

JPM は、ドキュメントの画像処理に使用される JPEG 2000 画像符号化システム Part 6 を指します。混合ラスター コンテンツ標準 (ISO/IEC 16485) に基づいており、JPEG 2000 およびその他のエンコーディングを使用するレイヤー化された静止画像が含まれています。 JPM ファイル形式は、独自の仕様に加えて、その親である [jp2](/image/jp2/) ファイル形式から機能を継承しています。

## JPM ファイル形式

JPM ファイル形式は [ISO/IEC 15444-6:2003](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124) で定義されています -- JPEG 2000 画像コーディング システム -- パート 6: 複合イメージ ファイル形式。複合イメージには、スキャンされたイメージ、合成イメージ、またはその両方が含まれる場合があり、連続トーンとバイレベルの圧縮方法を組み合わせる必要があります。 JPM ファイル形式は、ITU-T T.44 | で定義されている多層混合ラスター コンテンツ (MRC) 画像モデルを使用して、複数の画像を組み合わせて複合画像を生成する方法を説明する構成モデルを定義します。 ISO/IEC 16485。

### JPM仕様
JPM ファイル形式標準では、複数の画像を 1 つの画像に結合できる複合画像を表すバイナリ コンテナーであると指定されています。複数の画像をレイアウト オブジェクト、ページ、およびページ コレクションの階層にグループ化して、JPEG 2000 およびその他の圧縮画像データ形式を格納するためのメカニズムを設定します。この形式には、メタデータ (デジタル ライブラリ プロジェクトでは構造メタデータと呼ばれることが多い) を組み込むメカニズムが含まれています。

## 参考文献

* [ITU-T 勧告。 T.805](http://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124)
* [ウィキペディア:JPEG 2000](http://en.wikipedia.org/wiki/JPEG_2000)
