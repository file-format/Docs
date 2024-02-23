{
   "date" : "2023-12-14",
   "keywords" : [
"うーん",
"wsファイル",
"ws Windows スクリプト ファイル",
"wsファイルを開く方法",
"ファイル",
"ws ファイル拡張子",
"拡大",
"ファイル"
],
   "author" : {
      "display_name" : "Shakeel Faiz"
},
   "draft" : "false",
   "toc" : true,
   "title" : "WS ファイル - Windows スクリプト - .ws ファイルとは何ですか?またその開き方は?",
   "description" : "WS Windows Script ファイル形式と、WS ファイルを作成して開くことができる API について説明します。",
   "linktitle" : "WS",
   "menu" : {
      "docs" : {
         "identifier" : "executable-ws-ja",
         "parent" : "executable"
}
},
   "lastmod" : "2023-12-14"
}

## .WS ファイルとは何ですか?

通常、Windows 上の **.WS ファイル**には、**Windows スクリプト ホスト** を通じて実行されるように設計された実行可能スクリプトが含まれています。このスクリプトには、XML 要素だけでなく、JScript や VBScript ルーチンなどのさまざまな要素やルーチンを含めることができます。 「.ws」ファイルをダブルクリックすると、Windows スクリプト ホストはファイル内に埋め込まれたスクリプトの実行を開始します。

## Windowsホストスクリプトについて

Windows Script Host (WSH) は、Microsoft が開発したスクリプト ホストで、ユーザーが VBScript (Visual Basic Scripting Edition) や JScript (Microsoft バージョンの JavaScript) などのスクリプト言語で書かれたスクリプトを実行できるようにします。 Windows オペレーティング システムでスクリプトを作成するためのフレームワークを提供し、さまざまなタスクとシステム管理の自動化を可能にします。

Windows スクリプト ホストに関する重要なポイントをいくつか示します。

1.  **スクリプト言語:** WSH は複数のスクリプト言語をサポートしており、VBScript と JScript が最も一般的に使用されています。これらの言語のいずれかでスクリプトを作成して、タスクを自動化したり、オペレーティング システムと対話したり、データを操作したりできます。
    
2.  **スクリプトの実行:** WSH スクリプトは通常、VBScript の場合は「.vbs」、JScript の場合は「.js」などの拡張子を持つファイルに保存されます。スクリプトを実行すると、WSH がコードを解釈して実行します。
    
3.  **自動化:** WSH は、反復的なタスクの自動化、システム設定の管理、管理機能の実行などの自動化の目的でよく使用されます。これは、システム管理者やパワー ユーザーにとって特に役立ちます。
    
4.  **コンソールおよび GUI スクリプト:** WSH スクリプトは、コンソールベースまたは GUI ベースのいずれかにすることができます。コンソール スクリプトはコマンド ライン ウィンドウで実行されますが、GUI スクリプトはより対話型のアプリケーション用のグラフィカル ユーザー インターフェイスを作成できます。
    
5.  **Security:** WSH has security features to help prevent malicious scripts from causing harm; users are typically prompted before executing scripts and scripts are subject to certain restrictions to prevent unauthorized access and actions.
    
6.  **Windows スクリプト ホスト オブジェクト モデル:** WSH は、スクリプトが Windows オペレーティング システムと対話できるようにするオブジェクト モデルを提供します。これには、ファイル システム、レジストリ設定、ネットワーク リソース、その他のシステム コンポーネントへのアクセスが含まれます。
    
7.  **コマンド ラインからのスクリプト実行:** スクリプトをコンソール環境で実行するか GUI 環境で実行するかに応じて、`cscript.exe` または `wscript.exe` 実行可能ファイルを使用して、コマンド ラインから WSH スクリプトを実行できます。 。

## WSファイルを開くにはどうすればよいですか?

WS ファイルはプレーン テキスト ファイルであるため、開いたり編集したりする場合は、任意のテキスト エディタを使用できます。

- **メモ帳**
- **メモ帳++**
- **Apple TextEdit**
- **Visual Studio コード**

WS ファイル内のスクリプトを実行したい場合は、それをダブルクリックするか、コマンドラインで「wscript」コマンドを使用することができます。

## 参考文献
* [Windows スクリプト ホスト](https://en.wikipedia.org/wiki/Windows_Script_Host)


