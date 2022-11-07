{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL ファイル形式 - Python Wheel パッケージ ファイル",
  "description":"WHL ファイル形式と,WHL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## .WHL オプション番号

WHL (Wheel) ファイルは、Python の wheel 形式で保存された配布パッケージ ファイルです。これは、Python ディストリビューションの標準形式のインストールであり、インストールに必要なすべてのファイルとメタデータが含まれています。 WHL ファイルには、この wheel ファイルでサポートされている Python のバージョンとプラットフォームに関する情報も含まれています。 [MSI](/executable/msi/) セットアップ ファイルと同様に、WHL ファイル形式は、ソース配布をビルドせずにインストール パッケージを実行できる、すぐにインストールできる形式です。

## WHL ファイル形式

WHL ファイル形式は、[ZIP](/compression/zip/) (.zip) アーカイブであり、インストーラーがパッケージのインストールに必要とするすべてのインストール ファイルとメタデータが含まれています。これらの WHL ファイルは、解凍オプションまたは WinZIP や WinRAR などの標準解凍ソフトウェア アプリケーションを使用して抽出できます。

### WHL ファイルの命名規則

WHL ファイルは、次の規則に従って名前が付けられます。

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

WHL ファイル名の例は次のとおりです。

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

※「cryptography」はパッケージ名です。
※「2.9.2」は暗号のパッケージ版です。バージョンは、2.9.2、3.4、3.9.0.a3 などの PEP 440 準拠の文字列です。
* `cp35` は Python タグで、ホイールが要求する Python の実装とバージョンを示します。
※「abi3」はABIタグです。 ABI は、アプリケーション バイナリ インターフェイスの略です。
* `macosx_10_9_x86_64` はプラットフォーム タグです。

## 参考文献

* [Python Wheels とは何ですか? なぜ気にする必要があるのですか?](https://realpython.com/python-wheels/)
* [Python ホイール](https://pypi.org/project/wheel/)

