
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS ファイル - APK セット アーカイブ",
  "description":"APKSファイルとは何か?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## APKファイルとは?

拡張子が .apks のファイルは、Android パッケージ **APK** ファイルのコレクションであるアーカイブ ファイルです。 APKS ファイル内の個々の APK ファイルは、デバイスのさまざまな側面を考慮して生成されます。これらには、アーキテクチャ、言語、画面密度、およびその他のデバイス機能が含まれます。 APKS ファイルは **bundletool** によって生成されます。これは、Android アプリ バンドルをビルドし、デバイスに展開するためにアプリ バンドルを異なる APK に変換するために使用されます。

## APKS ファイル形式 - 詳細情報

APKS ファイルは、[ZIP](/compression/zip/) ファイル形式を使用して圧縮ファイルとして保存されます。

## APKSファイルを生成するには?

Android アプリ バンドル (AAB) の準備ができたら、Google Play ストアでの動作をテストしてデバイスに展開できます。この目的のために、AAB ファイルから APKS ファイルを生成し、Google の Android [bundletool](https://developer.android.com/tools/bundletool) を使用してテスト デバイスにインストールできます。次のコマンドを使用して、APK から APKS アーカイブ ファイルを作成するためのコマンド ライン ツールを提供します。

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

APK をデバイスにデプロイするために、次のようにデバイス署名情報を使用して APKS ファイルに署名できます。

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## 参考文献

* [バンドルツール - コマンドライン](https://developer.android.com/tools/bundletool)

