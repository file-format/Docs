{
  "date" : "2019-10-11",
  "keywords" :[ "tgs ファイル", "tgs ファイル形式", "tgs ファイルとは", "ファイル", "tgs の例", "tgs ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram Animated Stickers File Format",
  "description":"TGS ファイル形式と,TGS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## .TGS オプション番号

拡張子が .tgs のファイルは、クロスプラットフォーム メッセージング サービス [Telegram](https://core.telegram.org/stickers#animated-stickers) によって導入されたアニメーション ステッカー ファイルです。アニメーション ステッカーは、メッセージング アプリのユーザーが、静止画像である静的なグラフィックスとは異なり、より強化された生き生きとしたコンテンツをメッセージで送信するために使用します。 Telegram は当初、静止画像ステッカーに [WEBP](/image/webp/) ファイル形式を使用していました。 TGS ファイル形式は、静的な WEBP ステッカーと比較して、より高い解像度とより小さいファイル サイズでアニメーション データを格納できます。 TGS ファイルは、Telegram、7-zip、Apple Archive Utility、Corel WinZip などのアプリケーションを使用して開くことができます。

## TGS ファイル形式

Telegram は、2019 年 7 月に Lottie ライブラリに基づいて TGS ファイル形式を導入しました。 TGS ファイルは、Adobe After Effects のアニメーションからエクスポートされた [JSON](/web/json/) テキストで構成されます。エクスポートされた JSON テキストは、ファイル サイズを縮小する gzip 圧縮を使用して圧縮されます。テキスト ファイルに関する JSON 情報は、高い圧縮率の元になるテキスト ファイルに格納されます。

### TGS ステッカーの仕様

TGS ファイル形式は、TGS アニメーション ステッカーの作成に特定の制限を課します。 TGS アニメーション ファイル:

* ステッカー/キャンバスのサイズは 512×512 ピクセルである必要があります。
※ステッカーオブジェクトはキャンバスから離れてはいけません。
* アニメーションの長さは 3 秒を超えてはなりません。
* すべてのアニメーションはループする必要があります。
* Bodymovin でのレンダリング後、ステッカーのサイズは 64 KB を超えてはなりません。
* すべてのアニメーションは 60 フレーム/秒で実行する必要があります。

### サンプル TGS JSON テキスト

サンプルのアニメーション ステッカーを解凍すると、次の JSON テキスト コンテンツが含まれます。
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## 参照 ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - ウィキペディア](https://en.wikipedia.org/wiki/Gzip)

