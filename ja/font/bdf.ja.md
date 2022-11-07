{
  "date" : "2021-02-25",
  "keywords" :[ "bdf ファイル", "bdf ファイル形式", "bdf ファイルとは", "ファイル", "bdf の例", "bdf ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - グリフ ビットマップ配布形式",
  "description":"BDF ファイル形式と,BDF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## .BDF オプション番号
BDF ファイルは人間が読める形式で、通常は ASCII エンコーディングで配布されます。このファイルは、完全なフォントに関連するグローバル情報で始まり、その後に個々のグリフの情報とビットマップが続きます。その中のデータは、単一サイズの向きのフォントを示しています。複数の方向で使用するメトリックは、1 つのファイルに含めることができます。 BDF ファイルでは、各項目がファイル内の個別のテキスト行に含まれています。スペースは、行の項目を区切るために使用されます。

## BDF ファイル形式
Glyph Bitmap Distribution Format の BDF ショート。 Adobe社が所有するビットマップタイプのフォントを保存するためのファイル形式です。コンテンツは、コンピューターと人間が読めるように意図されたテキスト ファイルの形式をとります。 BDF は、特に Unix X Window 環境で使用されます。これは、より効率的であるとされる PCF フォント形式、および OpenType および TrueType フォントに広く置き換えられています。
### BDF ファイル構造
BDF フォント ファイルは、次の 3 つのセクションで構成されます。

- フォント内のすべてのグリフに適用されるグローバル セクション。
- グリフごとに個別のエントリを持つセクション。
- ENDFONT ステートメント。

## 例
以下は、ASCII 大文字の 'A' の 1 つのグリフを含むフォントの例です。そのグローバル宣言は「STARTFONT」行で始まり、「CHARS」行で終わります
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## 参考文献
* [グリフ ビットマップ配布形式](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Glyph Bitmap Distribution Format (BDF) 仕様](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

