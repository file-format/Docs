{
  "date" : "2020-01-10",
  "keywords" :[ "dib ファイル", "dib ファイル形式", "dib ファイルとは", "ファイル", "dib の例", "dib ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"DIB ファイル形式と,DIB ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## .DIB ファイルとは何ですか?

デバイスに依存しないビットマップ (DIB) は、標準のビットマップ ファイル ([BMP]()/image/bmp/)) と構造が似ているラスター イメージ ファイルです。これには、RGB カラーのピクセル値へのマッピングを説明するカラー テーブルが含まれています。これにより、DIB は任意のデバイスでイメージを表すことができます。 WindowsおよびmacOSで標準のBMPファイルを開くことができるほとんどすべてのアプリケーションで開くことができます。 DIB はバイナリ ファイルで、BMP に似た複雑なファイル形式です。 DIB イメージは、色深度とインチあたりのピクセル数に関して、レンダリング デバイスの出力機能とは無関係です。

## DIB ファイル形式の仕様 ##
DIB には、次の色と寸法の情報が含まれています。

* 長方形の画像が作成されたデバイスのカラー フォーマット。
* 長方形の画像が作成されたデバイスの解像度。
* イメージが作成されたデバイスのパレット。
* 赤、緑、青 ( RGB ) のトリプレットを長方形の画像のピクセルにマップするビットの配列。
* ビット配列のサイズを縮小するために使用されるデータ圧縮方式 (存在する場合) を示すデータ圧縮識別子。

### DIB データブロック形式 ###

DIB は、ディスクに保存された .DIB ファイルと比較して、メモリ ブロックのコンテキストで提供されます。メモリブロックは、DIB の Windows API 仕様に準拠した構造で構成されています。実際の DIB は次のもので構成されます。
* ヘッダー
* カラーパレット
* ピクセルデータ

実際には、パレット、ヘッダー、画像データの操作は、3 つの別個のメモリ ブロックであるかのように行われます。この共通メモリ ブロックへのハンドルは、GlobalAlloc を使用して割り当てられ、HDIB として知られています。これは、ヘッダー、カラー テーブル、およびピクセル データを抽出して処理するために使用されます。

### 構造 ###
DIB に含まれる情報は、さまざまな構造で表されます。これらには以下が含まれます：

BITMAPInfo - DIB の寸法と色の情報を定義します
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
BITMAPINFOHEADER で構成されています。

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
2 つ以上の RGBQAD 構造が続きます。

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### データビット ###
|ビット|説明|
---|---|
|1 ビット形式 (モノクロ)|モノクロ ビットマップは 2 色 (黒と白) で構成されます。このように色数が限られているため、これらのビットマップはディスク上で使用するスペースが少なくなります。 bitBitCount は、両方の色を表すために true または false を返します。 bitBitCount==1 の場合、ほとんどのアプリケーションはパレットを完全にスキップします。
|4 ビット形式 (VGA または 16 色)|画像データの各バイトは 2 つのピクセルを表し、bitBitCount==4 です。これらのビットは、降順でピクセルの色を表します。
|8 ビット形式 (256 色)|この 8 ビット形式は、最大 256 色を表すことができます。イメージのビットマップ データ配列の各バイトは、1 つのピクセルを表します。そのバイトの値は、bmciColors で表される 256 のエントリから使用されるカラー パレット エントリの番号です。
|24 ビット形式 (TrueColor)|これらのビットマップは、最大 2^24 色 (biBitCount == 24) を持つことができます。ビットマップ データ配列内の各 3 バイト シーケンスは、ピクセルの 3 つの原色の色相の相対的な強度を表します。色相は 0 ～ 255 の範囲の値として記述され、青、緑、赤の順に 3 バイトに格納されます。これは重要な違いです。Windows での色の参照のほとんどは逆の順序 (赤/緑/青) を使用しているため、TrueColor 画像を扱うときは "RGB" ではなく "BGR" と考えてください。 Windows の描画プロセスを高速化するために、カラー パレットを指定できます。その場合、biClrUsed は 0 にはなりません。しかし、ご覧のとおり、ピクセル データ自体に色情報が含まれているため、これは必要ありません。
|32 ビット形式|32 ビット画像の最大色数は 2^24 (biBitCount == 24) です。

## 参照 ##
* [デバイスに依存しないビットマップ - Microsoft による](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

