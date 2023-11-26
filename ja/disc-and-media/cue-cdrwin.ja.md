{
"日付":"2023-10-18",
   "keywords":[
"合図",
"キューファイル",
"cue cdrwin cue シート ファイル",
"キューファイルを開く方法",
"ファイル",
"キューファイル拡張子",
"拡大",
"ファイル"
],
   "author":{
"display_name":"シャキール・ファイズ"
},
"draft": "false",
"toc": true,
"title":"CUE ファイル形式 - CDRWIN キューシート",
   "description":"CUE CDRWIN Cue Sheet ファイル形式と,CUE ファイルを作成して開くことができる API について説明します。",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
"parent":"disc-and-media"
}
},
"lastmod":"2023-10-18"
}

## CUEファイルとは何ですか?

**.CUE** ファイル (**CDRWIN Cue Sheet** とも呼ばれます) は、オーディオ CD またはディスク イメージのトラックとレイアウトに関する情報が含まれるプレーン テキスト ファイル (通常は BIN または ISO 形式) です。これらのファイルは、ディスクの構造や内容を記述するためによく使用され、CD 書き込みソフトウェアや仮想ドライブ ソフトウェアがオリジナルのディスクを正確に再現できるようになります。

## CUEファイルの例

「.cue」ファイルがどのようなものであるかの例を次に示します。

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN キューシート

CDRWIN Cue Sheet は、CDRWIN ソフトウェアで使用される「.cue」ファイル形式の特定のバリエーションです。 CDRWIN は CD/DVD 書き込みおよびオーサリング ソフトウェアであり、その「.cue」シートはこのソフトウェアで使用するように設計されています。これらの「.cue」シートには、CDRWIN が CD または DVD を正確に作成または書き込むために必要な情報が含まれています。

ここでは、CDRWIN Cue Sheet に特有の重要な詳細をいくつか示します。

1. **CDRWIN に固有**: CDRWIN の「.cue」シートは、CDRWIN ソフトウェアに固有の独自形式です。これらは標準の「.cue」ファイルと類似点を共有していますが、CDRWIN の機能と設定で動作するように調整されています。
    






2. **ユーザーフレンドリーなインターフェイス**: CDRWIN は、「.cue」シートを作成および編集するための使いやすいインターフェイスを提供します。ユーザーは、トラック、インデックス、ギャップ、その他のパラメーターに関する情報を使いやすい方法で追加または変更できます。
    






3. **互換性のあるディスク タイプ**: CDRWIN キュー シートは主に、データ ディスク、オーディオ CD、混合モード ディスクなどを含む、さまざまなタイプの CD および DVD を作成するために使用されます。この形式を使用すると、ユーザーは作成したいディスクの種類と内容を指定できます。
    






4. **ディスク レイアウトの制御**: CDRWIN キュー シートは、トラックの順序、一時停止/ギャップ設定、ユーザーが持つその他の特定の好みなど、ディスクのレイアウトと構造を詳細に制御できます。
    






5. **ISO と BIN のサポート**: CDRWIN は ISO と BIN の両方のディスク イメージ フォーマットで動作します。 「.cue」シートは、ディスクに使用されるイメージ ファイルを指定し、キューとイメージ間の適切な同期を確保します。
    






6. **書き込みとリッピング**: これらの「.cue」シートは、CDRWIN を使用してディスクに書き込み、またはディスクからトラックをリッピングするときに重要です。これらは、最終製品が意図したレイアウトとコンテンツに一致していることを確認するのに役立ちます。
    






7. **バックアップと復元**: CDRWIN ユーザーは、CD または DVD のバックアップを作成するときに「.cue」シートを作成することがよくあります。これらのシートは、後でトラック レイアウトやタイミングなどのディスクのコンテンツを復元するために使用できます。

## CUEファイルを開くにはどうすればよいですか?

CDRWIN Cue Sheet は CDRWIN ソフトウェア用に特別に設計されているため、通常は CDRWIN 内で開いて使用することを目的としています。

CUE ファイルを開いたり参照したりするプログラム

- CDRWIN
- スマート プロジェクト IsoBuster
- EZB システム UltraISO

## その他の CUE ファイル

**.cue** ファイル拡張子を使用する他のファイル タイプは次のとおりです。

**ディスクとメディア**
- [CUE - キューシートファイル](/ja/disc-and-media/cue/)
- [CUE - CDRWIN キューシート](/ja/disc-and-media/cue-cdrwin/)

## 参考文献
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

