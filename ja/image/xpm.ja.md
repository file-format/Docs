{
  "date" : "2019-10-11",
  "keywords" :[ "xpm ファイル", "xpm ファイル形式", "xpm ファイルとは", "ファイル", "xpm の例", "xpm ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap ファイル形式",
  "description":"XPM ファイル形式と,XPM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .XPM オプション番号

拡張子が .xpm のファイルは、X Windows システムで使用されていた画像ファイル形式です。透明なピクセルをサポートし、通常はアイコン ピックスマップの作成を対象としています。モノクロ、グラスケール、カラーのピックスマップ データをサポートしています。これらは手動で編集できるように設計されており、[C](/programming/c/) コードに含めることができます。この目的のために、XPM ファイルはプレーン テキスト ファイル形式であり、C プログラミング言語の構文に従います。 XPM ファイルは、次のようなさまざまな画像表示アプリケーションで開くことができます。
CorelDRAW Graphics Suite 2020、Corel PaintShop Pro、IrfanView、および Canvas X。

## XPM ファイル形式

XPM ファイル形式は、これらを C および C++ プログラムに統合するために C 構文を使用します。次の 6 つの異なるセクションで構成されます。

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

セクションは、実際には次のような文字列の配列です。

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
以下、各部の詳細です。

`<Values> ` - このセクションは、底が 10 で、以下に対応する 4 つまたは 6 つの整数を含む文字列です。

* ピックスマップの幅と高さ
* 色数
* 1 ピクセルあたりの文字数
* オプションのホットスポット座標と XPMEXT タグ

`<Colors> ` - このセクションには、色と同じ数の文字列が含まれます。各文字列は次のとおりです。

```
<chars>{<key><color> }+
```
`<Pixels> ` - このセクションは<height>文字列と<width>\*<chars_per_pixel>文字。毎日<chars_per_pixel>長さの文字列は、<Colors>セクション。

`<Extension> ` - 拡張セクションが空でない場合は、拡張セクションにラベルを付ける必要があります。<Values>セクション。複数で構成されている場合があります<Extension>次の 2 つのタイプのサブセクション:

* 次のように構成された 1 つの独立した文字列: XPMEXT<extension-name><extension-data>
* または複数の文字列で構成されるブロック:XPMEXT<extension-name><related extension-data composed of several strings>

## 参考文献

* [XPM - ウィキペディア](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM マニュアル](http://www.xfree86.org/current/xpm.pdf)

