{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - クロスプラットフォーム インストーラー パッケージ ファイル",
  "description":"XPI ファイル形式と,XPI ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## .XPI ファイルとは?

XPI ファイルは、ファイルのサイズを小さくするために圧縮されたインストール アーカイブです。これは、プラグインとアドオン ファイルのインストールのために Mozilla アプリケーションによって使用されます。インストール スクリプトまたはマニフェストがファイルのルートにあり、多数のデータ ファイルが含まれています。 XPI ファイルには、Firefox ブラウザー、Thunderbird、または SeaMonkey の一部としてユーザーがインストールできるテーマ、ツールキット、または Firefox プラグインが含まれている場合があります。

## XPI ファイル形式 - 詳細情報

XPI ファイルは、複数のファイルを 1 つの圧縮ファイルに結合する [ZIP](/compression/zip/) アーカイブとしてディスクに保存されます。 XPI ファイル内のファイルには、JS などのインストール スクリプト ファイルと、[CSS](/web/css/)、[HTML](/web/html/)、[JSON](/web/json/) などの Web ファイルが含まれる場合があります。 ）。アドオンでアイコンとして使用する [PNG](/image/png/) 画像ファイルが含まれている場合もあります。

### XPI ファイルの内容を表示するには?

XPI ファイルは実質的に ZIP アーカイブであり、その内容は次の手順で表示できます。

* ファイルの拡張子を XPI から ZIP に変更します
* WinZip (Windows、Mac)、7-Zip (Windows)、または Apple Archive Utility (Mac) などの標準的な解凍ユーティリティを使用して、ファイルの内容を抽出します。

### Firefox Android に XPI ファイルをインストールする

ほとんどの人は、XPI ファイルを Android デバイスの Firefox にインストールできるかどうか知りたがっています。 Android では、ファイルを見つけて Firefox で開くことにより、XPI ファイルからアドオンをインストールできます。

## 参考文献

* [XPInstall - ウィキペディア](https://en.wikipedia.org/wiki/XPInstall)
* [XPI ファイル拡張子を開くにはどうすればよいですか?](https://support.mozilla.org/en-US/questions/1009049)

