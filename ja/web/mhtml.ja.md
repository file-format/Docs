{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","mhtml ファイル", "mhtml ファイル形式", "mhtml ファイルの種類", "ファイル", "種類", "mhtml ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML ファイル",
  "description":"MHTML ファイル形式と,MHTML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .MHTML オプション番号

MHTML 拡張子を持つファイルは、さまざまなアプリケーションで作成できる Web ページ アーカイブ形式を表します。この形式は、ウェブ **[HTML](/web/html/)** コードと関連するリソースを 1 つのファイルに保存するため、アーカイブ形式として知られています。これらのリソースには、画像、アプレット、アニメーション、オーディオ ファイルなど、Web ページにリンクされているすべてのものが含まれます。 MHTML ファイルは、Internet Explorer や Microsoft Word などのさまざまなアプリケーションで開くことができます。 Microsoft Windows は、問題を引き起こす Windows 上のアプリケーションの使用中に観察された問題のシナリオを記録するために、MHTML ファイル形式を使用します。 MHTML ファイル形式は、プレーン テキストの電子メール関連の仕様である message/rfc822 で定義されている仕様と同様のページ コンテンツをエンコードします。形式の実際の仕様は、[RFC 2557](https://tools.ietf.org/html/rfc2557) で詳しく説明されています。

## MHTML ファイル形式

MHTML は、HTML Web ページとそのリソースを単一の Web アーカイブにエンコードする機能から、集約 HTML ドキュメントの MIME カプセル化としても知られています。 RFC 2557 仕様によると、集約ドキュメントは MIME でエンコードされたメッセージであり、ルート リソース (オブジェクト) と、URI を介してそれにリンクされた他のリソースを含みます。そのような他のリソースは、インライン画像、スタイルシート、アプレットなどの表現である可能性があります。さらに、これらは他のマルチメディアドキュメントのルートになる可能性があります。 MHTML ファイル形式の完全なドキュメント仕様は、[RFC 2557](https://tools.ietf.org/html/rfc2557) に詳述されており、このファイル形式の読み取り/書き込みのためのあらゆる種類のアプリケーション開発で参照する必要があります。この規格では、参照するボディ パーツを Content-ID または Content-Location のいずれかで識別できると規定しています。

### MIME コンテンツ ヘッダー

MIME コンテンツ ヘッダー Content-Location は、他のボディ パーツのリソースへの URI 参照を解決するために定義されています。このヘッダーは、任意のメッセージまたはコンテンツの見出しで発生する可能性があります。

### Content-Location ヘッダー

Content-Location は、配置されているボディ部分のコンテンツにラベルを付ける URI の表現です。その値は、絶対または相対 URI にすることができます。メッセージの一部またはすべての受信者が取得できないリソースにラベルを付けるために使用できます。 1 つのメッセージは、1 つの Content-Location ヘッダーのみを持つことができます。 Content-Location ラベルと Content-ID ラベルの両方を持つボディ パーツを含むマルチパート/関連構造の例:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML 集合体の URI

MHTML 集約の URI は、そのルート URI の URI とは異なります。マルチパート/関連見出しの見出しで使用される場合、Content-Location ヘッダー フィールドは集約全体に適用する必要があります。同様に、取得されるリソースのセットは、MHTML 集約を参照する URI を使用してこの集約を取得する場合、その部分の Content-Locations を使用して取得されるリソースのセットとは異なる場合があります。たとえば、MHTML 集約を取得すると古いバージョンが返される場合がありますが、ルート URI とそのインライン リンク オブジェクトを取得すると新しいバージョンが返される場合があります。

## 参考文献

* [集約ドキュメントの MIME カプセル化 - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML ファイル形式 - ウィキペディアによる](https://en.wikipedia.org/wiki/MHTML)

