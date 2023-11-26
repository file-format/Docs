{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR ファイル - ESRI BIL ヘッダー ファイル形式",
  "description":"HDR ファイルとは何ですか?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## HDRファイルとは何ですか?

HDR ファイルは、バンド インターリーブ バイ ライン (.BIL) ファイルのヘッダー情報を含む GIS ヘッダー ファイルです。画像データを記述したもので、画像ファイルと同じ名前になります。 HDR ファイルは一連のエントリで構成され、各エントリは画像の特定の属性を記述します。 HDR ファイルには、別の地理参照ファイルと組み合わせて現実世界の座標に変換するための BIL ファイルのレイアウトとフォーマットが記述されています。

## HDR ファイル形式

HDR ファイルは ASCII テキスト ファイル形式で保存されます。これには、各エントリが画像の特定の属性を説明する一連のエントリが含まれています。各 HDR ファイルの形式は次のとおりです。

```
<keyword> <value>
```

`<keyword> ` - 設定されている特定の属性を示します
`<value> ` - 属性に設定されている値です

ヘッダー内のエントリの順序に制限はありません。ただし、HDR リーダーで使用される解析方法に準拠するために、各エントリは行の別個の行に存在する必要があります。

## HDR ファイルで使用されるキーワードのまとめ

|キーワード |許容値 |デフォルト|
---|---|---|
|nrows |任意の整数 > 0|なし
|ncols |任意の整数 > 0|なし
|nbands |任意の整数 > 0| 1
|nbits |1、4、8、16、32| 8
|バイトオーダー| I = Intel、M = Motorola |ホスト マシンと同じ|
|レイアウト|ビル、ビップ、bsq|ビル|
|スキップバイト|任意の整数 ≥ 0| 0
|ulxmap |任意の実数| 0|
|ulymap |任意の実数 |nrows - 1|
|xdim |任意の実数| 1
|ydim |任意の実数| 1
|bandrowbytes |任意の整数 > 0|最小の整数 ≥ (ncols x nbits) / 8|
|totalrowbytes |任意の整数 > 0| bil の場合: nbands x Bandrowbytes;bip の場合: 最小の整数 ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |任意の整数 ≥ 0| 0|

## 参考文献

* [HRD ファイル形式 - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

