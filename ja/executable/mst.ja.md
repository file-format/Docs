{
  "date" : "2021-06-30",
  "keywords" :[ "mst ファイル", "mst ファイル形式", "mst ファイルとは", "ファイル", "mst 例", "mst ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"MST ファイルの形式と,MST ファイルを作成して開くことができる API について学びます。",
  "title" :"MST - Windows インストーラー パッケージ ファイル",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## .MST オプション番号
拡張子が .mst のファイルは、MSI パッケージのコンテンツを変換するために使用されます。これらは、システム管理者がカスタム設定を既存の MSI ファイルに適用するためによく使用されます。 MST ファイルは、グループ ポリシーなどのソフトウェア配布システムで元の MSI パッケージと一緒に使用されます。 MSTファイルは通常、ソフトウェアの開発中のバージョンを構成するためのソフトウェア開発およびテストで使用されます。

## MST ファイル形式
MST または変換ファイルは、Microsoft Windows インストーラーを使用するプログラムのインストール オプションをファイルに収集するために使用されます。これらのファイルは通常、インストーラー (MSIEXEC.EXE) コマンド ラインで使用されるか、ソフトウェア インストールのグループ ポリシーで使用されます。 Microsoft Active Directory ドメイン内。 MST ファイルは、ラップされた実行可能インストーラーでも使用できます。一般的なケースは、ラップされたインストーラーにコマンド ライン パラメーターを渡したい場合です。これを行うには、プロパティ テーブルに WRAPPED_ARGUMENTS プロパティを追加する MST ファイルが必要です。これらのファイルは、一般的なエディターを使用して作成または編集することはできません。この目的のために、特定のツールを利用できます。

### MST ファイルの使い方は?
MST ファイルは、さまざまなツールを使用して生成できます。一般に、MST ファイルの生成には Ocra が使用されます。その後、必要に応じて設定をカスタマイズし、特定の場所に保存できます。その後、MST ファイルを MSI ファイルと組み合わせて使用できます。このファイルをテストしたい場合。コマンドラインで次の構文を使用します

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS プロパティ

Windows インストーラーの **TRANSFORMS** プロパティを使用することもできます。これは実際には、パッケージのインストール時にインストーラーが適用する変換のリストです。インストーラーは、TRANSFORM プロパティにリストされているのと同じ順序で変換を実行します。変換は、拡張子 .mst のファイル名またはフル パスで指定できます。複数の変換を指定するには、次の例のように各ファイル名またはセミコロンで区切ります。

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## 参考文献

* [MST 変換ファイル](https://www.exemsi.com/documentation/mst-transformation-files/)
* [TRANSFORMS プロパティ](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)


