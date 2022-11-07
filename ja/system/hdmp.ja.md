{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP ファイル - Windows ヒープ ダンプ ファイル形式",
  "description":"HDMP ファイル形式と,HDMP ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## .HDMP ファイルとは?

HDMP ファイルは、エラーが原因でアプリケーションまたはプログラムがクラッシュしたときの圧縮されていないメモリ ダンプです。これは Windows XP/Vista でのみ作成され、アプリケーションがクラッシュしたときの状態のダンプが含まれています。非圧縮の HDMP ファイルは、レポート用に圧縮されたミニダンプ [MDMP](/system/mdmp/) ファイルと比較して、ディスク上でより多くのスペースを必要とします。

HDMP ファイルを **開く** または分析するために使用できるアプリケーションには、Windows 用のデバッグ ツールを備えた Microsoft Visual Studio が含まれます。

## HDMP ファイル形式

HDMP ファイルはバイナリ ファイルとしてディスクに保存され、適切なアプリケーションなしで開いた場合は何のメリットもありません。これらには、エラーが発生したときに記録された関連システム データが含まれます。

### HDMP と MDMP ファイル形式の違い

HDMP は非圧縮のメモリ ダンプ ファイルです。対照的に、MDMP はミニ ダンプ ファイルであり、ファイル サイズを縮小するために圧縮され、問題を報告するために Microsoft に送信されます。

## 参照 ＃＃

* [DMP - マイクロソフト](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

