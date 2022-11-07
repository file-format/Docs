{
  "date" : "2021-08-30",
  "keywords" :[ "ipa ファイル", "ipa ファイル形式", "ipa ファイルとは", "ファイル", "ipa の例", "ipa ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"IPA ファイル形式と,IPA ファイルを作成して開くことができる API について学びます。",
  "title" :"IPA - iOS アプリケーション パッケージ ファイル",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## .IPA オプション番号
拡張子が .ipa のファイルは iOS に属し、アプリケーション パッケージ ファイルと呼ばれます。これは、iOS アプリケーションを格納するアーカイブ ([ZIP](/compression/zip/) 圧縮を使用して圧縮された) ファイルですが、そのアプリケーションは iOS または ARM ベースの MacOS デバイス (iPad、iPhone、またはアイポッドタッチ。主に、iTunes、Apple Configurator 2、またはサードパーティのソフトウェアを使用して IPA ファイルをインストールできます。

## IPA ファイル形式
Apple Xcode を使用してアプリを開発している IOS 開発者は、IPA ファイルに精通しています。なぜなら、開発したアプリを、アプリ ストア展開のテストのために IPA ファイルとしてパッケージ化する必要があるからです。 IPA ファイルは iOS アプリとしてインストールされることが知られていますが、解凍して含まれているアプリ データを表示することもできます。 IPA ファイルには、携帯電話の ARM アーキテクチャ用のバイナリが 1 つだけ含まれており、x86 アーキテクチャ用のバイナリは含まれていないため、多くの .ipa ファイルは iPhone シミュレーターにインストールできません。
### .ipa ファイルの構造
次の例は、IPA の構造を示しています。

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
上記は、iTunes と App Store が認識する組み込みの構造です。この構造に従って：
- ペイロード ディレクトリには、すべてのアプリ データが含まれます。
- iTunes アートワーク ファイルは 512×512 ピクセルの PNG 画像で、iTunes および iPad の App Store アプリで表示するためのアプリのアイコンが含まれています。
- iTunesMetadata.plist には、開発者の名前と ID、著作権情報、バンドル ID、アプリの名前、ジャンル、リリース日、購入日など、さまざまな情報が含まれています。
- META-INF フォルダーには、IPA の作成に使用されたプログラムに関するメタデータのみが含まれます。


## 参考文献

* [.ipa - ウィキペディアによる](https://en.wikipedia.org/wiki/.ipa)


