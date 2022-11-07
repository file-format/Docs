{
  "date" : "2021-03-23",
  "keywords" :[ "OEBZIP", "Open eBook Publication Structure", "extension", "format", "eBook", "OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"OEBZIP ファイル形式と,OEBZIP ファイルを作成して開くことができる API について学びます。",
  "title" :"OEBZIP - 圧縮された Open eBook 出版物の構造",
  "linktitle" : "OEBZIP",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## .OEBZIP ファイルとは? ##

OEBZIP ファイルは、International Digital Publishing Forum (**IDPF**) によって導入されました。 [OEB](/ebook/oeb/) と同様に、これらのファイルは、電子ブックの構造、コンテンツ、および表示に関する XML ベースの仕様ですが、圧縮または zip 形式になっています。

## OEBZIP ファイル形式の技術的な詳細 ##

OEBZIP は、特にマークアップ ボキャブラリ (現在は XHTML 1.1 の基本サブセット) の改善や広く拡張された CSS サポートなど、レンダリング コントロールの分野でより多くの新しい機能を提供しました。持続可能性の要素は、以前のバージョンから変更されていません。

OEBZIP ファイル形式は、他のすべてのコンポーネント ファイルをリストするマニフェストを含む強制パッケージ ファイルと、論理的な読み取り順序を示すスパインを含む一連のファイルで構成されます。さらに、[XML](/web/xml/) のテキストに対して、OEBZIP ファイルのリーダーは、[JPEG](/image/jpeg/) および [PNG](/image/png/) 形式の画像をレンダリングできる必要があります。 .他の形式のコンテンツ コンポーネントを組み込むことができますが、フォールバック コンテンツは基本的な OEB 形式のいずれかで提供する必要があります。
  

ファイルの OEBZIP バンドルは、主にミッドステート フォーマットとして使用され、エンド ユーザーへの公開は、さまざまな eBook ビューアーに適した形式で eBook を提供する出版社またはアグリゲーターを通じて管理されていました。その後継バージョンである [EPUB](/ebook/epub/) は、最終状態の形式でエンド ユーザーに届く可能性が高く、中間状態の形式としても機能します。

## 参考文献

* [OEBPS (Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [オープン電子ブック](https://en.wikipedia.org/wiki/Open_eBook)


