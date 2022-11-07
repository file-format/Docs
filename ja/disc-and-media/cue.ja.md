{
  "date" : "2021-06-09",
  "keywords" :["キュー","ファイル","拡張子","フォーマット","キューファイルとは","音楽","キューファイルフォーマット","キューファイルフォーマット仕様","キューシート","CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"CUE ファイル形式と,CUE ファイルを作成,変換,開くことができる API について学びます。",
  "title" :"CUE - キューシートファイル",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## .CUE ファイルとは何ですか?

キュー シート ファイルとも呼ばれる .cue 拡張子を持つファイルは、CD または DVD 上のトラックのレイアウトに関する情報を含むメタデータ ファイルです。これらは、メディア プレーヤーや光ディスク オーサリング アプリケーションでサポートされています。 CD に格納されている主要なオーディオ データは、トラックの長さ、ディスク タイトル、および出演者の仕様と共に、キュー ファイルによって参照されます。したがって、1 つのオーディオ ファイルに複数のトラックが含まれている場合、キュー ファイルを使用して、オーディオを複数のファイルに分割したり、さまざまなトラックを参照したりできます。

## CUE ファイル形式

CUE またはキュー シート ファイルは、人間が判読できるプレーン テキスト形式で保存されます。キュー ファイル内の情報は、1 つ以上のパラメーターを持つコマンドです。これらのコマンドは、特定のコマンドとコンテキストに応じて、ファイル全体または個々のトラックに適用されます。 CDRWIN ユーザー ガイドでは、キュー シートの構文とセマンティクスの仕様について説明しています。

## CUE シートの基本コマンド

|コマンド|説明|
---|---|
|ファイル| [MP3](/audio/mp3/)、[WAV](/audio/wav/)、プレーン バイナリ ディスク イメージなどのデータとその形式を含むファイルを指します。
|トラック|番号やタイプ、モードなどのトラック コンテキスト情報を定義します。|
|インデックス| FILE 内のインデックスとして位置を表します。形式は mm:ss:ff (分-秒-フレーム) です。|
|PREGAP および POSTGAP|これは、どのデータ ファイルにも格納されていない、トラックのプレギャップまたはポスト ギャップを示します。長さは INDEX と同じ分秒枠の形式で指定します。|

### CUE シートの例

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## 参考文献

* [.cda ファイル - ウィキペディアによる](https://en.wikipedia.org/wiki/.cda_file)

