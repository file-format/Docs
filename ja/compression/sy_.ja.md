{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ファイル形式 - 圧縮SYSファイル",
  "description":"SY_ ファイル形式と,SY_ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## SY_ ファイルとは何ですか?

SY_ ファイルは、インストーラー内にパッケージ化されたインストール ファイルのサイズを縮小するためにソフトウェア インストーラーによって使用される圧縮された .sys ファイルです。これにより、インストーラーの全体的なサイズが縮小されます。 SY_ ファイルは、1 つ以上の圧縮ファイルを展開する Microsoft Expand コマンド ライン ユーティリティを使用して展開できます。

## SY_ ファイル形式 - 詳細情報

SY_ ファイルは、圧縮されたバイナリ ファイルとしてディスクに保存されます。ただし、内部ファイル形式は公開されていません。 Microsoft Expand コマンド ライン ユーティリティは、次のコマンド ラインのいずれかを使用して SY_ ファイルを展開できます。

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
展開すると、SY_ ファイルは [SYS](https://docs.fileformat.com/system/sys/) ファイルに変換されます。

SY_ ファイルは、EX_ および DL_ ファイルに似ています。

## 参考文献

* [StuffIt - ウィキペディアによる](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

