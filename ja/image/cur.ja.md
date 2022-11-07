{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "extension", "file", "format", "image", "Device-Independent Bitmap", "Cursor File Format", "Cursor", "Windows", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - カーソルファイル形式",
  "description":"CUR ファイル形式と,CUR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## .CURファイルとは何ですか? ##

CUR ファイルは、静的な Microsoft Windows カーソル ファイル形式です。基本的に、拡張子を除いてあらゆる点で ICO (アイコン) ファイルと同じ静止画像です。 CUR と [ICO](/image/ico/) はどちらも、Device-Independent Bitmap [DIB](/image/dib/) (Device-Independent Bitmap) 仕様に基づいて確立されます。 Windows オペレーティング システム用の Windows マウス ポインタなどのカスタム カーソルと同様に、デフォルト カーソルは CUR ファイルに保存されます。通常の使用では矢印、待機期間を示す回転する砂時計、テキスト編集用の I バーなどがあります。カスタム デスクトップ テーマのインストール パックには CUR ファイルが付属しており、Windows カーソルがカスタム デスクトップ テーマと一致するようになっています。

## 技術仕様 ＃＃

CUR ファイルは、Microsoft Windows オペレーティング システムで機能するデバイスにあるバイナリ システム ファイルです。 CUR ポインタ イメージには、16×16、32×32 などのさまざまな標準サイズがあります。CUR ファイルは ICO ファイルに非常に似ています。どちらも小さな静止画像で構成されています。 CUR ファイルと ICO ファイルの拡張子のみが異なります。さらに、CUR ファイルのヘッダーにあるホットスポットの説明は、ICO ファイルとは異なります。ホットスポットは、左上隅からマウスをポイントしている場所までのピクセル オフセットを解釈します。 Windows システムは引き続き CUR ファイルを使用していますが、アニメーション カーソルのファイル拡張子は通常、CUR ではなく ANI になります。

## 簡単な歴史 ##

CUR ファイルは ICO ファイルから作成されます。最初の CUR ファイル形式は、1981 年に Microsoft の Windows 1.0 オペレーティング システムに組み込まれ、商用利用がスムーズになりました。すぐに、よりインタラクティブなカーソルが導入され、ユーザーは利用可能なプレインストールされたオプションからカーソルの設定を修正できるようになりました.ただし、技術的な知識が不十分な場合でも、CUR ファイルを自分で簡単に編集できます。


## CUR の例 ##

CUR ファイルは *C:\Windows\Cursors* にあります。

{{< figure src="../cur.png" alt="CUR ファイル形式" >}}

