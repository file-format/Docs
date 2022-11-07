{
  "date" : "2021-06-09",
  "keywords" :[ "m4p","mp3","ファイル","拡張子","形式","m4pファイル形式とは","音楽","m4pファイル形式","M4bとMP3","m4pファイル形式の仕様" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"M4P ファイル形式と,M4P ファイルを作成,変換,開くことができる API について学びます。",
  "title" :"M4P - MPEG-4 オーディオブック ファイル形式",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## M4Pファイルとは何ですか?
拡張子が .m4p のファイルはオーディオ ファイルで、通常は Apple iTunes ストアでダウンロードできます。つまり、M4P は AAC ファイルですが、デジタル著作権管理 (DRM) を使用してコピー保護されていると言えます。これは、M4P ファイルが許可されたシステムまたはデバイスでのみ再生できることを意味します。通常、M4P ファイルは Apple マルチメディア デバイスに固有のものです。したがって、これらのファイルは、Apple macbooks、ポッドキャスト、iPhone 6 や iPhone 7 などのスマートフォンでのみ再生できます。

## M4Pファイル形式
M4P は MPEG 4 Protected (audio) の略で、高度なオーディオ コーデック (AAC) でオーディオをエンコードし、ファイルの不正使用からファイルを保護します。このファイル形式は、通常、iTunes Music Store のオーディオ ファイル形式と見なされます。 Apple は FairPlay Digital Rights Management (DRM) システムを使用して M4P ファイルを保護しています。 FairPlay DRM は、ベリディスクが開発した技術に基づいています。その保護メカニズムは、AES 暗号化を使用して AAC オーディオ ストリームを暗号化することによって機能します。ユーザーは、復号化のために自分のアカウントに割り当てられたマスター キーを受け取ります。このファイル形式は、MP3 ファイル形式の代替として導入されました。これは、MP3 が元々オーディオ ファイルとしてではなく、MPEG 1 または 2 ビデオ ファイルのレイヤー III として意図されていたためです。


## M4P ファイル形式の仕様

[M4A](/audio/m4a/) と同様に、M4P ファイルも連続したチャンクで構成されます。各チャンクには 8 バイトのヘッダーがあり、次のように細分されます。
- 4 バイトのチャンク サイズ (ビッグ エンディアン、上位バイトが最初)
- 4 バイトのチャンク タイプ - 定義済みの署名の 1 つ: 「mdat」、「moov」、「pnot」、「moof」、「udta」、「uuid」、「free」、「skip」、「ftyp」、 "jP2"、"wide"、"load"、"imap"、"matt"、"chap"、"kmat"、"clip"、"crgn"、"sync"、"tmcd"、"PICT"、"scpt "、"ctab"、"ssrc".

M4A と同様に、M4P の最初のチャンクはタイプ「ftype」になり、オフセット 8 にサブタイプがあります。サブタイプで定義された M4P は「M4P_」でなければなりません。

不明なタイプのチャンクが検出されるまでチャンクを繰り返し、M4P (MPEG-4 Audio) ファイルを構成します。

## 参照 ##

* [MPEG-4 パート 14 - ウィキペディアによる](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 オーディオ (M4A,M4B,M4P) フォーマットと復元例](https://www.file-recovery.com/m4a-signature-format.htm)

