{
  "date" : "2021-02-20",
  "keywords" :["WMA","ファイル","拡張子","フォーマット","オーディオ交換ファイル形式","音楽"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WMA ファイル形式と,WMA ファイルを作成して開くことができる API について学びます。",
  "title" :"WMA - Windows Media オーディオ ファイル",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## .WMA ファイルとは?

拡張子が .wma のファイルは、Advanced Systems Format (ASF) 形式で保存されたオーディオ ファイルを表します。 ASF は、Windows Media Audio 9 によってエンコードされたビットストリームを含む Microsoft 独自の形式です。オーディオ コンテンツに加えて、WMA ファイルには、トラックのタイトル、アルバム、アーティスト、ジャンルなどのメタデータ オブジェクトも含まれます。 WMA ファイルは、[.mp3](/audio/mp3/) ファイルと同様に、主に Web 経由のストリーミングに使用されます。

## WMA ファイル形式

WMA ファイルはバイナリ ファイル形式で、ASF ファイル形式に含まれています。 MP3 ファイルで使用される ID3 タグと同様に、ファイルに関するメタデータのエンコーディングを指定します。 WMA コーデックは、Microsoft によって 2008 年以来、Protected Interoperable File Format (PIFF) で使用されています。ただし、DECE UltraViolet や MPEG-DASH などの関連する業界標準では、標準化されたオーディオ コーデックとして宣言されていません。

### WMA タイプ固有のデータ

Windows Media オーディオ コーデックのタイプ固有の情報は、ストリーム プロパティ オブジェクトのタイプ固有データの一部として、次の形式で格納されます。

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## 参考文献

* [ASF の概要 - マイクロソフト](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

