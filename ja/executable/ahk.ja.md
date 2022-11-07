{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AHK ファイル形式と,AHK ファイルを作成して開くことができる API について学びます。",
  "title" :"AHK ファイル形式 - AutoHotkey スクリプト ファイル",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## .AHK オプション番号

AHK ファイルは、Microsoft Windows でのタスクの自動化に使用される AutoHotkey ソフトウェア アプリケーションで生成されたスクリプト ファイルです。これには、インスタント アクションの実行に使用できるショートカット キーを使用してタスクを自動化するための手順が含まれています。ファイルは AutoHotkey によって実行され、すべてのアクションが順番に実行されます。 AHK ファイルは、ホットキーを使用して定義されたホットキーを使用して複雑なタスクを実行するのに十分強力です。 AHK ファイルは、Microsoft Notepad や Notepad++ などのテキスト エディターで開くことができます。

## AHK ファイル形式

AHK ファイルはプレーン テキスト ファイルとしてディスクに保存され、AutoHotkey で実行できるコード行が含まれています。 AutoHotkey は、無料のオープン ソース スクリプト言語であり、ユーザーは単純なものから複雑なスクリプトを作成して、フォーム入力、自動クリック、マクロの実行などのアクションを実行できます。AHK ファイルは、少なくとも 1 つのアクションを実行してから終了できます。 .

AHK を [Exe](/executable/exe/) ファイルに変換するために使用できるツールがあります。

### AHK の例

次の例では、Win + Z キーを使用して Microsoft メモ帳を実行するか、既に実行されている場合は前面に移動します。

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## AHK ファイルを作成するにはどうすればよいですか?

次の手順を使用して、AHK ファイルを作成できます。これらは、AutoHotkey が既にマシンにインストールされていることを前提としています。

※デスクトップ上で右クリックしてください。
*メニューで「新規」を見つけます。
* 「新規」メニュー内の「AutoHotkey Script」をクリックします。
* スクリプトに新しい名前を付けます。
* デスクトップに新しく作成されたファイルを見つけて、右クリックします。
※「スクリプト編集」をクリックします。
* ウィンドウがポップアップするはずです。おそらくメモ帳です。
* ファイルを保存します。

## 参考文献

* [オートホットキー](https://www.autohotkey.com/)
* [バッチ ファイル - ウィキペディアによる](https://en.wikipedia.org/wiki/Batch_file)

