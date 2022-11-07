{
  "date" : "2021-06-29",
  "keywords" :[ "DLL","拡張子","ファイル","フォーマット","システム","ダイナミック リンク ライブラリ","設定","プログラム","コンピューター","アプリケーション" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - ダイナミック リンク ライブラリ",
  "description":"DLL ファイルの形式と,DLL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## DLL ファイルとは? ##

DLL ファイルまたはダイナミック リンク ライブラリは、実行可能ファイルの一種です。これは、デバイスで最もよく見られる拡張ファイルの 1 つで、通常は Windows の System32 フォルダーに保存されています。 DLL 拡張ファイルは Microsoft によって開発され、広く使用されています。ユーザー評価も高い人気です。 DLL は、Windows サーバーによってプログラム/アプリケーション用に設計および適用される *drivers/procedures/functions/properties* を含むシェルフとして機能します。 1 つの DLL ファイルをさまざまな Windows プログラム間で共有することもできます。これらの拡張ファイルは、ファイルの書き込みや読み取り、セットアップの外部にある他のデバイスとの接続など、プログラムでさまざまな機能を有効にして実行する責任があるため、デバイスで Windows プログラムをスムーズに実行するために不可欠です。
ただし、これらのファイルは、任意のバージョンの Windows (windows 7/windows 10/など) をサポートするデバイスでのみ開くことができるため、Mac OS をサポートするデバイスで直接開くことはできません。 (Mac OS で DLL ファイルを開きたい場合は、さまざまな外部アプリケーションでファイルを開くことができます。)


## DLL ファイル形式 ##

DLL ファイルは Microsoft によって開発され、タイプを表す拡張子 ".dll" を持ちます。これは、Windows 1.0 サーバーの不可欠な部分であり、その後も続いています。これはバイナリ ファイル タイプであり、Microsoft Windows のすべてのバージョンでサポートされています。このファイル タイプは、Windows プログラム内に共有ライブラリ システムを作成する手段として作成されました。これにより、プログラムを再リンクする必要なく、プログラム ライブラリを個別かつ独立して編集または変更できるようになります。


## DLL の例 ##

DLL エントリ ポイントのサンプル コードを以下に示します。

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## 参照 ＃＃

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
