{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "拡張子", "ファイル", "フォーマット", "システム", "ドライバー", "Windows デバイス ドライバー", "プログラム", "コンピューター", "アプリケーション" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV - Windows デバイス ドライバー",
  "description":"DRV ファイルの形式と,DRV ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## .DRV ファイルとは何ですか? ##

拡張子が .drv のファイルは、Windows デバイス ドライバーに属します。 Windows オペレーティング システムは、これらのファイルを使用して、内蔵および外付けのハード デバイスを接続します。 DRV ファイルは、デバイスとオペレーティング システムがどのようにリンクするかを示す命令とパラメータで構成されています。これらのファイルは、Windows で適切に機能するデバイス ドライバーをインストールするのに役立ちます。また、バスまたはケーブルを介して PC のマザーボードにリンクされているデバイスには、DRV ファイルが必要です。


## DRV ファイル形式 ##

DRV ファイルは通常、ダイナミック ライブラリ ([DDL](/system/dll/) ファイル) または [EXE](/executable/exe/) ファイルとしてパッケージ化されます。これらのファイルは、スマートフォンなどのすべてのシステム プラットフォームでサポートできますが、各プラットフォームがこれらのファイルを適切にサポートするという保証はありません。ただし、.drv ファイル拡張子を使用する最も一般的なデバイスは次のとおりです。

* サウンドカード
* グラフィックカード
* プリンター
* ストレージデバイス
* ネットワーク アダプター
* コンピュータ ハードウェア アクセサリ

このファイル形式にはウイルスやその他の悪意のあるプログラムが含まれているため、電子メールで送信された DRV ファイルを開かないことをお勧めします。不明なDRVファイルを開く前に、必ず包括的なスキャンを実行してください。


## DRV の例 ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

