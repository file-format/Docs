{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX ファイル形式 - ペイントブラシ ビットマップ イメージ ファイル",
  "description":"PCX ファイル形式と,PCX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## .PCX オプション番号

PCX ファイル、Picture Exchange ファイルは、PC Paintbrush アプリケーションのネイティブ ファイル形式として使用されたラスター イメージ ファイル形式です。米国の ZSoft Corporation によって DOS および Windows プラットフォーム用に開発され、[BMP](/image/bmp/)、[JPEG](/image/jpeg/)、および [ PNG](/image/png/) ファイル形式。 PCX ファイルは、RLE エンコーディングを使用して圧縮されているため、サイズが小さくなります。これは、主にデジタル ファックス ファイルの作成に使用される複数ページの [DCX](/image/dcx/) ファイルで使用されます。

## PCX ファイル形式

PCX ファイルは、バイナリ ファイル形式でディスクに保存されます。内部ファイル形式の構造は、リトル エンディアンのバイト順に従っており、次の 3 つのセクションがあります。

**`PCX ヘッダー`** - PCX ヘッダーの長さは 128 バイトです。これには、識別子、バージョン番号、画像のサイズ、16 のパレット色、各プレーンのカラー プレーンとビット深度の数、および圧縮方法の値が含まれます。

PCXヘッダーは画像ファイルフォーマット百科事典（第2版）を参考に以下の通りです。
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`画像データ`** - ヘッダーの直後に PCX 画像データが続きます。ヘッダーのフィールド設定によっては、画像データが圧縮される場合があります。 PCX ファイル内のデータの格納は、指定されたカラー プレーンの数によって異なります。画像データは行単位で編成されます。複数のプレーンの場合、これらは、赤、緑、青のデータが順番に配置された行内のプレーンごとに格納されます。このパターンは、平面内の各行に対して繰り返されます。

## 参考文献

* [PCX - ウィキペディアによる](https://en.wikipedia.org/wiki/PCX)

