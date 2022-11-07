{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SIFZ ファイル形式 - Synfig Studio 圧縮プロジェクト ファイル",
  "description":"SIFZ ファイル形式と,SIFZ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## .SIFZ オプション番号

SIFZ ファイルは、オープン ソースの 2D アニメーション作成アプリケーション **Synfig Studio** によって作成された gzip 圧縮された SIF ファイルです。アニメーションを構成する複数のグラフィック要素が含まれています。全体的なアニメーション コンテンツは、図形、ブラシまたは鉛筆のストローク、およびテキストで満たされたキャンバスの組み合わせを使用して構築されます。これらはすべて、半径、接線、角度、頂点、および幅ハンドルの独自の位置に配置されます。 SIFZ ファイルは [Synfig Studio](https://www.synfig.org/) で開くことができます。

## SIFZ ファイル形式

SIFZ ファイルは、gzip 圧縮方式を使用してパッケージ化された圧縮 [ZIP](/compression/zip/) ファイルです。 Synfig は、ベクターとビットマップのアートワークを使用して映画品質のアニメーションを作成するために使用されます。従来のフレームごとのアニメーション作成方法とは異なり、より少ないリソースで高品質の 2D アニメーションを作成できます。

圧縮されている SIFZ ファイルは、圧縮されていない SIF ファイルよりも小さくなります。これにより、低帯域幅のインターネット接続での転送も簡単になります.

## 参考文献

* [Synfig オープン ソース - Github](https://github.com/synfig/synfig/)
* [Synfig ドキュメント](https://synfig.readthedocs.io/en/latest/index.html)

