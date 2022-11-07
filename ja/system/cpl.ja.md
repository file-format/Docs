{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "拡張子", "ファイル", "フォーマット", "システム", "コントロール パネル ファイル", "Windows", "プログラム", "コンピューター", "アプリケーション" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - コントロールパネルファイル",
  "description":"CPL ファイル形式と,CPL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .CPL オプション番号##

CPL ファイルは、「システム」ファイルの一種です。これは、Windows オペレーティング システムで使用されます。 CPL ファイルは Control Panel File の略です。これらのファイルは、Microsoft Windows オペレーティング システムのコントロール パネルで開くバイナリ ファイルであり、マウス、ディスプレイ、ネットワークなど、コントロール パネルで使用可能なツールを表し、開くために使用されます。 CPL ファイルは通常、デバイスのシステム フォルダーに保存されます。これらのファイルは手動で開かないでください。


## CPL ファイル形式 ##

Windows オペレーティング システムのさまざまな CPL ファイルは、さまざまなコントロール パネル項目を表すために接続されています。すべてのコントロール パネル項目は CPL ファイルにリンクされており、項目にはサフィックス「.cpl」が付けられています。

CPL ファイルの一般的な種類とその形式は次のとおりです。

* Inetcpl.cpl – デバイスのインターネット プロパティ用
* Appwiz.cpl – デバイスのプログラム プロパティを追加または削除するには
* Desk.cpl – ディスプレイ プロパティ用
* Main.cpl – マウス、フォント、キーボード、およびプリンターに関連するプロパティ用。
* Netcpl.cpl – ネットワーク関連のプロパティ用
* System.cpl – システム関連のプロパティおよび新しいハードウェアの追加ウィザード用
* TimeDate.cpl – Date または Time プロパティ用
* Mlcfg32.cpl – Microsoft Exchange または Windows Messaging プロパティ用
* Intl.cpl – これは地域設定のプロパティに関係します
* Modem.cpl – モデム関連のプロパティ用
* Themes.cpl – デスクトップ テーマとプロパティを格納します。
* Password.cpl – パスワード プロパティ用
* Mmsys.cpl – マルチメディア プロパティ用
* Wgpocpl.cpl – Microsoft Mail Post Office に関連

## 簡単な歴史 ##

CPL ファイル タイプは Microsoft Windows によって開発され、Windows 1.0 以降の Windows オペレーティング システムの不可欠な部分です。これはすべての Windows バージョンで引き続き使用され、すべてのコントロール パネル項目のプロパティはこのファイル タイプを使用して保存されます。

## CPL の例 ##

サンプルの CPL ファイルを以下に示します。

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
