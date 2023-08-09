{
  "date" : "2019-12-09",
  "keywords" :[ "3mf ファイル","3mf ファイル形式","3mf ファイルとは","ファイル","3mf の例","3mf ファイルの拡張子","拡張子","形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"3MF ファイル形式と,3MF ファイルを開いて作成できる API について学びます。",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## 3MFファイルとは何ですか?

3MF (3D Manufacturing Format) は、アプリケーションが 3D オブジェクト モデルをさまざまな他のアプリケーション、プラットフォーム、サービス、およびプリンターにレンダリングするために使用されます。 [STL](/cad/stl/) などの他の 3D ファイル形式の制限や問題を回避して、最新バージョンの 3D プリンターで作業するために作成されました。 3MF は、3MF コンソーシアムによって開発および公開された比較的新しいファイル形式です。モデルを完全に記述するのに十分なほど豊富で、内部情報、色、およびその他の特性を保持しているため、3D 印刷の新しいイノベーションをサポートするために拡張できます。この形式は拡張可能であり、広く採用でき、他の広く使用されているファイル形式を悩ませる問題はありません。

## 3MF ファイル形式の歴史

STL などの利用可能なモデル記述ファイル形式の既存の制限により、主要なブランドが集まり、3D 印刷用のより拡張可能なファイル形式を策定するようになりました。重要な考慮事項は、アプリケーションがモデル データを 3D プリンターに渡す方法です。したがって、3MF コンソーシアムは、3D 印刷のニーズに十分に対応できるように拡張可能にすることを目的として、3MF と呼ばれる新しい 3D ファイル形式を支援するために発足しました。 Microsoft、Autodesk、Dassault Systems、Netfabb、SLM、HP など、いくつかの企業がこのコンソーシアムに参加しました。 Microsoft は、3MF コンソーシアムが共同で仕様をさらに発展させるための出発点として、進行中の 3D ファイル形式を寄贈しました。

## 3MF ファイル形式 - 詳細情報

3MF は XML ベースのデータ形式 (人間が判読できる圧縮 XML) であり、サードパーティによるカスタム データの拡張性など、3D 製造に関連するデータの定義が含まれています。 3MF ファイル形式は、他の 3D ファイル形式が直面する制限と問題を念頭に置いて設計されました。これにより、次のような 3MF ファイル形式が作成されました。

* **完全:** 必要なすべてのモデル、材料、およびプロパティ情報を 1 つのアーカイブに格納
* **人が読める:** OPC、[ZIP](/compression/zip/)、XML などの一般的な構造を使用して開発を容易にする
* **シンプル:** 短く明確な仕様であり、開発が容易になり、検証が迅速になります
* **拡張可能:** XML 名前空間を活用することで、互換性を維持しながらパブリック拡張とプライベート拡張の両方が可能になります
* **明確:** 明確な言語と適合性テストにより、デジタルから物理的なファイルまで常にファイルの一貫性が保たれます
* **無料:** 3MF 仕様へのアクセスと実装には、使用料、特許、およびライセンスは常に無料です。

3MF ファイル形式の仕様は、パブリック アクセスと継続的な更新のために [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) でホストされています。現在公開されているバージョンは 1.2.3 で、1 つまたは複数の 3D モデルのコンテンツと外観を記述するために XML およびその他の広く利用可能なテクノロジを使用するための一連の規則が記述されています。 3MF ファイル形式を処理するシステムを構築したい開発者は、実装目的でこれらの仕様を参照できます。

## 3MF ファイル形式の仕様

3MF ファイル形式は、その物理モデルの ZIP アーカイブの形式で Open Packaging 仕様を使用します。これには、ドキュメントの特定の目的を満たす明確に定義された一連のパーツと関係が含まれます。これにより、デジタル署名やサムネイルなどのパッケージ機能にフォーマットが追従します。

### 3MF ドキュメント - 概要

典型的な 3MF ドキュメントは次のようになります。

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

ペイロードには、3D モデル パーツの処理に必要なパーツの完全なセットが含まれています。 3D ペイロードに記述されたオブジェクトの製造に使用されるすべてのコンテンツは、3MF ドキュメントに含まれている必要があります。各ドキュメント パーツの説明と、必須またはオプションのステータスを次の表に示します。


|**名前**|**説明**|**関係ソース**|**必須/オプション**
--- | --- | --- | ---
|3D モデル|製造用の 1 つまたは複数の 3D オブジェクトの説明が含まれています。|パッケージ|必須
|コア プロパティ|さまざまなドキュメント プロパティを含む OPC パーツ。|パッケージ|オプション
|デジタル署名の起点|パッケージ内のデジタル署名のルートである OPC 部分。|パッケージ|オプション
|デジタル署名|それぞれがデジタル署名を含む OPC パーツ|デジタル署名の起点|オプション
|デジタル署名証明書|デジタル署名証明書を含む OPC パーツ|デジタル署名|オプション
|PrintTicket|3D モデル パーツで 3D オブジェクトを出力するときに使用する設定を提供します。|3D モデル|OPTIONAL
|サムネイル|パッケージ内の 3D オブジェクトまたはパッケージ全体を表す小さな JPEG または PNG 画像が含まれます。|パッケージ|オプション
|3D テクスチャ|3D モデル パーツの 3D オブジェクトに色を適用するために使用されるテクスチャを含みます (拡張機能で利用可能)|3D モデル|オプション
|カスタム パーツ|メタデータに関連付けられている OPC パーツ|パッケージ|OPTIONAL

[パーツと関係](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships)、[3D モデル](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models)、[オブジェクト リソース](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources)、[素材リソース](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) および [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) 仕様のセクションdocument は、3MF ドキュメントに関する詳細情報を提供します。

## 参照 ##

※【3MFファイルフォーマット仕様書】(https://github.com/3MFConsortium/spec_core)
* [3MF - ウィキペディアによる](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

