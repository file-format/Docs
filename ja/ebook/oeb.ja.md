{
  "date" : "2021-03-23",
  "keywords" :[ "OEB", "Open eBook Publication Structure", "extension", "format", "eBook", "OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"OEB ファイル形式と,OEB ファイルを作成して開くことができる API について学びます。",
  "title" :"OEB - 電子書籍出版構造を開く",
  "linktitle" : "OEB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## .OEB オプション番号

OEB ファイルは、International Digital Publishing Forum (**IDPF**) によって導入されました。より正式には、OEB ファイルは **OEBPS** としても知られています。これらのファイルは、電子ブックの構造、コンテンツ、および表示に関する XML ベースの仕様です。このファイル形式は [EPUB](/ebook/epub/) 形式に取って代わられました。

## OEB ファイル形式の技術的詳細

OEB ファイル形式は、他のすべてのコンポーネント ファイルをリストするマニフェストを含む必須パッケージ ファイルと、論理的な読み取り順序を示すスパインを含む一連のファイルで構成されます。さらに、[XML](/web/xml/) のテキストに対して、OEB ファイルのリーダーは、[JPEG](/image/jpeg/) および [PNG](/image/png/) 形式の画像をレンダリングできる必要があります。 .他の形式のコンテンツ コンポーネントを組み込むことができますが、フォールバック コンテンツは基本的な OEB 形式のいずれかで提供する必要があります。

OEBPS 1.2 は、以前のバージョン (OEBPS 1.0.1) に対する密結合の更新でした。これは、特にマークアップ語彙 (現在は XHTML 1.1 の正規のサブセット) の拡張や大幅に拡張された CSS サポートなど、レンダリング制御の分野で最新の機能を提供しました。持続可能性の要素は、以前のバージョンから変更されていません。
  

ファイルの OEB バンドルは、主にミッドステート フォーマットとして使用され、エンド ユーザーへの公開は、さまざまな電子ブック ビューアに適した形式で電子ブックを提供する出版社またはアグリゲータを通じて管理されていました。その後継バージョンである [EPUB](/ebook/epub/) は、最終段階の形式として、また中間段階の形式としてエンド ユーザーに届く可能性が高くなります。

## 参考文献

* [OEBPS (Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [オープン電子ブック](https://en.wikipedia.org/wiki/Open_eBook)


