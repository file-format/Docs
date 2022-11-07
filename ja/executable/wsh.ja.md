{
  "date" : "2021-08-27",
  "keywords" :["wshファイル","wshファイル形式","wshファイルとは","ファイル","wsh例","wshファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"WSH ファイル形式と,WSH ファイルを作成して開くことができる API について学びます。",
  "title" :"WSH - Windows スクリプト ファイル",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## .WSH オプション番号
拡張子が .wsh のファイルには、VB や VBS などの特定のプログラミング言語スクリプトのプロパティとパラメーターが含まれています。WSH の実際の必要性は、特定のスクリプトの実行をカスタマイズするためにそれらを使用することです。実行するには WScript または CScript が必要で、どちらも Windows オペレーティング システムに含まれています。 WSH ファイルは、最初は Windows 95 のインストール ディスクで、コントロール パネル用のオプションの構成およびインストール可能なものとして提供され、その後 Windows 98 のデフォルト コンポーネントとして提供されました。

## WSH ファイル形式
WSH (Windows Script Host) は、管理、ログオン スクリプト、一般的な自動化など、さまざまな目的で使用できます。 WSH は、スクリプトを実行するための環境を確立します。適切なスクリプト エンジンを呼び出し、スクリプトが処理する一連のサービスとオブジェクトを割り当てます。これらのスクリプトは、COM オブジェクトまたはコマンド ライン モードから GUI モードで実行できるため、対話型スクリプトと非対話型スクリプトの両方に柔軟に対応できます。

### 例
これは、ルート WSH COM オブジェクト「WScript」を使用して「OK」ボタン付きのメッセージを表示する VBScript を示す非常に簡単な例です。このスクリプトが起動されると、CScript または WScript エンジンが呼び出され、ランタイム環境が確立されます。

```
WScript.Echo "Hello world"
WScript.Quit
```


## 参考文献

* [Windows スクリプト ホスト - ウィキペディアによる](https://en.wikipedia.org/wiki/Windows_Script_Host)



