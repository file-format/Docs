{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "ファイル", "拡張子", "ファイル形式", "ページレイアウト", "カプセル化 PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"EPS ファイル形式と,EPS ファイルを作成して開くことができる API について学びます。",
  "title" :"EPS ファイル形式 - カプセル化された PostScript ファイル",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## .EPS ファイルとは何ですか?

.eps ファイルは、Encapsulated Postscript ファイル形式でディスクに保存されるイメージ ファイルです。テキスト、グラフィック、画像の任意の組み合わせを含めることができます。 EPSファイルには、そのようなファイルを開くことができるアプリケーションで表示するために、内部にカプセル化されたビットマッププレビュー画像も含まれる場合があります。

## EPS ファイル形式の歴史

履歴の観点から EPS ファイル形式をざっと見てみると、次の情報が明らかになります。

* EPS の最初のバージョンは、1985 年から 1988 年の間に Adobe によってリリースされました。
* EPS 仕様のバージョン 2.0 は 1989 年 1 月に公開されました
* EPS のバージョン 3.0 の仕様は、1992 年に別のドキュメントとして公開されました。これは最新の公開バージョンです。

EPS は、Adobe の PostScript Language Document Structuring Conventions Specification の条項 9 で説明されている Open Structuring Conventions 拡張メカニズムと組み合わせて、Adobe Illustrator アートワーク ファイル形式の初期バージョンの基礎を形成しました。

## EPS ファイル形式

EPS は独自の形式ですが、公式に文書化されており、EPS ファイル形式の仕様は開発者が参照できるように公開されています。 EPS は [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) 準拠のファイル形式であり、DSC によって確立されたすべての規則に準拠しています。 DSC は、Adobe による PostScript ドキュメント用の特別なファイル形式です。 EPS ファイルを読み取ることができると主張するすべてのアプリケーションは、DSC に準拠する必要があります。

EPS ファイルは、以下で説明する 2 つの主要なセクションで構成されます。

### プレビュー画像 ###

典型的な EPS ファイルには、複数のシステムまたはアプリケーションを含むワークフローでの便利な使用を目的とした形式のプレビュー イメージが含まれています。プレビューの目的は、ほとんどのグラフィックス アプリケーションがレンダリングできる形式で画像を表示することです。プレビューは通常、ピクセル寸法および/またはビット深度の解像度が低くなります。プレビュー ファイルは、さまざまな形式のいずれかにすることができます。 EPS_3 の仕様には、次の 3 つの「デバイス固有」のプレビュー形式がリストされています。

* Apple Macintosh の場合、QuickDraw アプリケーションで使用される PICT 画像
* DOS コンピュータの場合、TIFF ビットマップ
* Windows メタファイル。

PICT と Windows メタファイルには、ビットマップ データとベクトル グラフィックスの両方を組み込むことができます。さらに、この仕様では、埋め込まれたビットマップ プレビュー イメージのデバイスに依存しない非常に単純な表現が定義されています。この表現は、Encapsulated PostScript Interchange Format (EPSI) として知られています。

EPSI プレビューは、ASCII 16 進数で表されるビットマップであり、識別のためにいくつかの PostScript コメントで囲まれ、シンプルで簡単に転送できるようになっています。 EPS ファイルを異なるプレビュー形式で区別するために、EPS 仕様では異なる DOS ファイル拡張子と Macintosh ファイル タイプが推奨されました。

### PostScript コード

EPS ファイル形式には、少なくとも次のものが含まれている必要があります。

* ヘッダー コメント %!PS-Adobe-3.0 EPSF-3.0
* および境界ボックスのコメント %%BoundingBox: llx lly urx ury は、イラストの境界を説明します。これら 4 つの引数は、境界ボックスの左下 (llx、lly) と右上 (urx、ury) の角に対応します。

EPS ファイルでは、次の演算子は使用できません。

*バンドデバイス、
* cleardictstack
*コピーページ
*消去ページ
* 出口サーバー
* フレームデバイス
*グレストアオール
* initclip
* initgraphics
* 初期行列
* 終了する
*レンダーバンド
* セットグローバル
* setpagedevice
*セット共有
* ジョブを開始します。

## EPSから他のファイル形式への変換

EPS ファイルは、[JPG](/image/jpeg/)、[PNG](/image/png/)、[TIFF](/image/tiff/)、[PDF](/pdf) などの標準的な画像形式に変換できます。 /) Adobe Illustrator、Photoshop、PaintShop Pro などのさまざまなアプリケーションの使用。

[セキュリティの脆弱性](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) の EPS ファイル、Office 2016、Office 2013、Office 2010、および Office 365 では、EPS ファイルを Office ドキュメントに挿入する機能がオフになっています。

## 参考文献

* [カプセル化された PostScript - ウィキペディアによる](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

