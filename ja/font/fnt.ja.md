{
  "date" : "2020-08-20",
  "keywords" :[ "fnt ファイル", "fnt ファイル形式", "fnt ファイルとは", "ファイル", "fnt の例", "fnt ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows フォント ファイル",
  "description":"FNT ファイル形式と,FNT ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## .FNT オプション番号

拡張子が .fnt のファイルは、Windows オペレーティング システムの一般的なフォント情報を格納するフォント ファイルです。 FNT ファイルは、ほとんどが TrueType (.TTF) および OpenType (.OTF) ファイル形式に置き換えられており、現在では廃止されたフォント ファイル形式です。これらのファイルには、単一の評価者またはベクター フォントを格納できます。すべてのデバイス ドライバは、Windows 2.x フォントをサポートしています。ただし、すべてのデバイス ドライバーではありません。
Windows 3.0 バージョンをサポートします。

## FNTファイル形式

FNT ファイルには、単一のラスター フォントまたはベクター フォントを格納できます。ベクトル形式は、小さなビットマップを使用して各憲章のグリフが定義されるラスターと比較して、GDI でより頻繁に使用されます。 .fnt を .ttf および .otf に置き換える明白な理由は、そのラスター形式です。

### フォント ファイル ヘッダー
ラスター フォント ファイルとベクター フォント ファイルの先頭は共通で、ファイルの種類ごとに異なる情報が続きます。 Windows 3.0 のフォント ファイル ヘッダー インクルードには、Windows の将来のバージョンとの互換性を確保するためにゼロに設定されている次の 6 つの新しいフィールドが含まれています。

* dFlags
* dfAspace
* dfB スペース
* dfCスペース
* dfColorPointer
* dfReserved1

Windows 3.0 および 2.0 のヘッダーの詳細については、[Microsoft KnowledgeBase アーカイブ](https://jeffpar.github.io/kbarchive/kb/065/Q65123/) にアクセスしてください。

## 参考文献
* [フォントファイル形式](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Windows でフォントをインストールまたは削除する方法](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

