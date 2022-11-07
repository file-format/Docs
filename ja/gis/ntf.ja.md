{
  "date" : "2021-07-28",
  "keywords" :[ "ntf ファイル", "ntf ファイル形式", "ntf ファイルとは", "ファイル", "ntf の例", "ntf ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - National Transfer Format ファイル",
  "description":"NTF ファイル形式と,NTF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## .NTF ファイルとは何ですか?
拡張子が .ntf のファイルは **National Transfer Format (NTF)** ファイルと呼ばれます。主に UK Ordnance Survey (OS) で使用されます。特に地理空間データの転送用。英国規格協会によって管理されています。これは、Ordnance Survey デジタル データの標準的な転送形式になっています。横メルカトル図法の一種である英国のナショナル グリッド図法は、NTF ファイルの地理参照情報をすべて保持しています。

## NTF ファイル形式
NTF ファイル形式は、英国の Ordnance Survey が所有しています。インポート用の GDB ライブラリでサポートされています。 NTF ファイル形式の現在のバージョンは 2.0 です。このファイル形式は、構造ごとに属性フィールドが 1 つしかない **PCIDSK** ベクター セグメントの制限に対処するために導入されましたが、ベクター データで抽出できるさまざまな属性があります。 NTFファイルフォーマットは回避するために、2つのセグメントを持つように構成されています。各セグメントは同じベクトルで構成されていますが、属性が異なります。 NTF ベクター ファイルの最初のセグメントには、特徴コード番号を属性として持つベクターが含まれています。 2 番目のセグメントには、属性として値を持つベクトルが含まれます。

### 座標参照システム
GDB ライブラリは、適切な TM 射影特性を持つラスター データとベクター データを表します。

- 基準経度: 49.0
- 基準緯度: 2.0
- 偽東: 400000
- 偽北距離: -100000
- スケール: 0.9996012717
- 楕円体: Airy 1830 (E009)
NTF ファイルの更新または書き込みはサポートされておらず、DTM ファイルにリンクすることもできません。

### Ogrinfo の例
次の例では、NTF ファイルで **ogrinfo** を使用してレイヤー番号を取得します。
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## 参考文献

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web マッピング - Tyler Mitchell によるイラスト](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

