{
  "date" : "2021-01-21",
  "keywords" :["aiファイル","aiファイル形式","aiファイルとは","ファイル","ai例","aiファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Adobe Illustrator アートワーク ファイル",
  "description":"AI ファイル形式と,AI ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## .AI ファイルとは何ですか?

拡張子が .ai のファイルは、単一ページにベクター グラフィックスを含む Adobe Illustrator アートワーク ファイルです。ポイントを使用して画像データを表示するためのパスを作成するため、拡大しても画質が低下することはありません。 AI ファイル形式は、AI ファイルに似た PGF ファイル形式をベースとしています。 AI 形式は、ロゴや印刷媒体に主に使用され、初期バージョンは [EPS](/image/eps/) ファイルと同様と見なされていました。 AI ファイルは、Adobe Illustrator、Adobe Acrobat DC、PaintShop Pro、CorelDraw Graphics ツールで開くことができます。

## AI ファイル形式

AI は Adobe Illustrator 独自のファイル形式で、PGF と同様のデュアル パス アプローチを使用して EPS 互換ファイルを保存します。 [Adobe Illustrator ファイル形式の仕様](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) では、詳細なこのファイル形式の内部詳細については、開発者向けリファレンスを参照してください。すべて Adobe Illustrator で作成されたドキュメント (ファイル) は PostScript 言語ドキュメントであり、ドキュメント構造規則に準拠する 2 つの主要な部分、「プロローグ」と「スクリプト」があります。

### プロローグ

プロローグ セクションは、ファイルの解釈に必要な情報をカプセル化します。例として、ページ上のすべてのマークを含む境界ボックスがあります。また、フォントやプロシージャ定義などのリソース情報も含まれています。これらのリソースは、procsets と呼ばれるセットに論理的にグループ化され、プロシージャを初期化および終了するための明示的なメソッドが含まれています。

＃＃＃ 脚本

ページ上のグラフィック要素は、スクリプトによって記述されます。スクリプトには、オペランドとデータとともに、プロローグの演算子とプロシージャへの参照が含まれています。スクリプトの 3 つの論理セクションには、次のものが含まれます。

* Setup Sequence - プロローグで定義されたリソースを初期化およびアクティブ化します
* 記述演算子のシーケンス
* リソースを非アクティブ化するトレーラー

スクリプト内の演算子は、プロローグ内の procsets によって定義された言語で記述された一連のグラフィック要素です。これらのシーケンスは、データ要素のコレクション、グラフィック属性の定義、および procset で定義されたプロシージャの呼び出しで構成されます。

### オブジェクトタグ

オブジェクト タグは、カスタム情報を Adobe Illustrator アート オブジェクトに添付するために使用されます。タグは次のもので構成されます。

* タグ識別子
※タグタイプ
* データ

## 参考文献
※【Adobe Illustrator ファイル形式仕様書】(https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/ja/illustrator/sdk/AI7FileFormat.pdf)
* [PaintShopPro による AI ファイル形式](https://www.paintshoppro.com/ja/pages/ai-file/)

