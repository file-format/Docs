{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3 ファイル形式 - Canon Raw 3 画像ファイル",
  "description":"CR3 ファイル形式と,CR3 ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## CR3 ファイルとは何ですか?

CR3 ファイルは、一部の Canon デジタル カメラで作成される Canon RAW 画像ファイル形式です。 CR2 ファイル形式を置き換えるために Canon によって導入され、一部の Canon デジタル デバイスで使用されています。 CR3 ファイルには、カメラによってキャプチャされた元の未処理のロスレス画像データが保存されます。これらの RAW 画像を使用すると、高品質の画像が提供され、写真家が編集するための十分な余地が与えられます。メインの画像データに加えて、CR3 ファイルには画像に関するメタデータ情報も保存されます。

## CR3 ファイル形式

CR3 ファイルは、ISO Base Media File Format (ISO/IEC 14496-12) のバイナリ ファイルとしてディスクに保存され、カスタムの [Canon タグ](https://exiftool.org/TagNames/Canon.html#uuid) も含まれます。また、JPEG-LS (Rice-Golomb + RLEコーディング) および JPEG-2000 (LeGall 5/3 DWT + 定量化)。

## CR3 カスタム タグ

CR3 ファイルには、さまざまな目的のカスタム タグが含まれています。これらのタグの一部は次のとおりです。

|タグID|タグ名|書き込み可能 |値 / メモ|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP タグ|
|'CMT1' |IFD0| - |--> EXIF タグ|
|'CMT2' |ExifIFD| - |--> EXIF タグ|
|'CMT3' |MakerNoteCanon| - |--> Canon タグ|
|'CMT4' |GPSInfo| - |--> GPS タグ|
|'CNCV' |コンプレッサーのバージョン|いいえ| | |
|'CNOP' |カノンCNOP| - |--> Canon CNOP タグ|
|'CNTH' |CanonCNTH| - |--> キヤノン CNTH タグ|
|'THMB' |ThumbnailImage|いいえ| | |

## 参考文献

* [CR2 ファイル形式](http://lclevy.free.fr/cr2/)
* [キヤノンタグ](https://exiftool.org/TagNames/Canon.html#uuid)

