{
  "date" : "2021-07-12",
  "keywords" :[ "cmd ファイル","cmd ファイルとは","ファイル","cmd の例","cmd ファイルの拡張子","拡張子","形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"CMD ファイル形式と,CMD ファイルを作成して開くことができる API について学びます。",
  "title" :"CMD - Windows コマンド ファイル形式",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## .CMD オプション番号
CMD ファイルは、さまざまなタスクを実行するために実行されるプレーン テキスト形式の 1 つまたは複数のコマンドを含むスクリプトで構成されます。これは [BAT](/executable/bat/) ファイルに似ており、一般的に実行可能なコマンドのバッチを保存するためにも使用されます。 CMD ファイルは、Microsoft Windows オペレーティング システムで広く使用されています。これらのファイルはほぼ 90 年代に導入されましたが、最新の Windows オペレーティング システムでも使用されています。これらのファイルは通常、複数のコマンドを連続して実行するために作成されます。

## CMD ファイル形式
CMD は、CP/M スタイルの実行可能プログラムで使用されるファイル形式です。 CP/M-80 の [COM](/executable/com/) や DOS の [EXE](/executable/exe/) に相当します。 CMD ファイルには、1 ～ 8 グループのコードまたはデータと 128 バイトのヘッダーが含まれています。各グループのサイズは最大 1 MB です。 CMD ファイルには、新しいバージョンの再配置情報と Resident System Extensions (RSX) を含めることもできます。 CMD は、[BAT](/executable/bat/) ファイルに比べて新しいものです。 MS-DOS では、Windows がリリースされる前に MS-DOS で使用されていました。現在でもファイルを .bat 拡張子で保存できますが、多くの人は .cmd 拡張子を使用して実行可能なスクリプトを保存しています。

### CMDフォーマット仕様

ヘッダーの先頭には、ファイルに存在するグループのリストとそのタイプが含まれています。各タイプは最大 1 回使用できます。これらのタイプは次のとおりです。

- コード
- データ
- 追加
- スタック
- ユーザー 1
- ユーザー 2
- ユーザー 3
- ユーザー 4
- 共有コード

DOS のプログラム セグメント プレフィックスと同様に、データ グループの最初の 256 バイトはゼロです。これらは、CP/M-86 によってゼロ ページで読み込まれます。データ グループがない場合は、代わりにコード グループの最初の 256 バイトが使用されます。
## CMD ファイルの例
以下は、システム情報を表示する CMD スクリプトの例です。
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## 参考文献

※【CMDスクリプトの書き方】(https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD ファイル (CP/M) - Wikipedia による](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

