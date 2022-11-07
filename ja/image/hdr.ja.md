{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR ファイル形式 - HDR 画像ファイルとは?",
  "description":"HDR ファイル形式と,HDR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## HDRファイルとは何ですか?

HDR ファイルは、デジタル カメラの写真を保存するためのハイ ダイナミック レンジ (HDR) ラスター イメージ ファイル形式です。これにより、写真編集者は、ダイナミック レンジが制限されているデジタル画像の色と明るさを向上させることができます。この修正により、コーナー周辺の明るさが改善され、自然に近い画像が得られます。通常、HDR ファイルは 32 ビットのラスター イメージとして保存されます。 Adobe Photoshop は、HDR ファイルを作成して開くことができます。

HDR ファイルは、HDRI とも呼ばれます。

## HDR ファイル形式 - 詳細情報

HDR ファイル形式は、オリジナルの Radiance Picture (.pic) ファイル形式に基づいています。通常、HDR ファイルのピクセル データは圧縮されずに保存されますが、単純なランレングス エンコーディング システムを使用して圧縮される場合もあります。

### HDR ファイル構造

HDR イメージ ファイルは、次の 3 つのセクションで構成されます。

* **ヘッダー:** HDR ファイルは、画像ファイルの最初のバイト、つまり「#?RADIANCE」で識別されます。
* **解決文字列:** ヘッダーの後には、4 つの値で構成される単一の解決行が続きます。 X および Y ラベルのそれぞれに整数値が続きます。 X と Y の順序は回転を示します。 X と Y の正と負の値の組み合わせは、可能なすべてのイメージの向きと回転をカバーします。
* **ピクセル データ:** HDR ファイルのピクセル データは、圧縮されていないか、標準のランレングス エンコーディングを使用して圧縮されています。

## オープンソースの HDR/HDRI API

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - クロス プラットフォームの超高速シングル ヘッダー [C++](/programming/cpp/) ライブラリを使用して、ロード/デコードせずに画像のサイズと形式を取得します。
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - ロード/デコードせずに画像サイズとフォーマットを取得する Rust ライブラリ。 [.avif](/image/avif/)、[.bmp](/image/bmp)、[.cur](/image/cur/)、[.dds](/image/dds/)、[. gif](/image/gif/), hdr (写真), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ico /)、[.jp2](/image/jp2/)、[jpeg (jpg)](/image/jpeg/)、[jpx](/image/jpx/)、ktx、[png](/image/png /)、[psd](/image/psd/)、qoi、tga、tiff (tif)、および webp。
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - HdrHistogram の Java 実装。

## 参考文献

* [ラディアンス HDR](http://paulbourke.net/dataformats/pic/)
* [画像情報](https://github.com/xiaozhuai/imageinfo )

