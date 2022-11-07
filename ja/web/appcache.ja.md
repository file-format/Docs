{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE ファイル - HTML5 キャッシュ マニフェスト ファイル形式",
  "description" :"APPCACHE ファイルとは何か,APPCACHE ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## APPCACHEファイルとは何ですか?

APPCACHE ファイルは、Web アプリケーションへのオフライン アクセスのためにブラウザによってキャッシュされるリソースのリストを含むテキスト ファイルです。これは、インターネット接続がない場合に便利です。このような状況では、ブラウザはオフライン キャッシュ リソースを使用して Web コンテンツへのアクセスを提供します。 APPCACHE ファイルには、画像 (**[PNG](/image/png/)**、**[WEBP](/image/webp/)** など)、スタイルシート **([ CSS])(/web/css/)**、およびスクリプト ファイル (Javascript **[JS](/web/js/)** ファイルなど)。

**APPCACHE ファイルを開く**ことができるアプリケーションには、Google Chrome、Safari、Firefox などの Web ブラウザーが含まれます。

## APPCACHE ファイル形式 - 詳細情報

APPCACHE ファイルは単純なテキスト ファイルであり、インターネットに接続せずに実行する Web ページへのオフライン アクセスを提供します。 APPCACHE の存在は、ページをオフラインで使用できることを示します。

### APPCACHE ファイルを参照するには?

HTML ページでは、APPCACHE ファイルは次のように参照されます。

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE マニフェスト ファイルの構造

シンプルな APPCACHE マニフェスト ファイルは次のようになります。

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

これは最も単純な例であり、より複雑な構造も存在する可能性があります。

## APPCACHE マニフェストの利点

キャッシュ インターフェイスを使用すると、Web アプリケーションに次のような利点があります。

1. オフライン ブラウジング - キャッシュ インターフェースにより、エンド ユーザーはオフラインのときにサイト全体をブラウズできます。
1. 速度 - キャッシュにより、ディスクから直接オフライン コンテンツに高速アクセスできます
1. いつでもアクセス可能 - サイトがダウンした場合でも、ユーザーは引き続き Web コンテンツにアクセスでき、オフライン エクスペリエンスを得ることができます。

## 参考文献

* [AppCache マニフェストの初心者ガイド](https://web.dev/appcache-beginner/)

