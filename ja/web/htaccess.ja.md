{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS ファイル - Apache HTACCESS ファイル形式",
  "description" :"HTACCESS ファイルとは何かを学ぶためのファイル形式ガイド",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## HTACCESS ファイルとは何ですか?

HTACCESS ファイルは、Web サイトのさまざまなフォルダー/ディレクトリの構成を変更できるメカニズムを提供する Apache 構成ファイルです。ディレクトリとサブディレクトリに適用可能な構成ディレクティブが含まれています。

HTACCESS ファイルは、Web サイトのインデックス ページの定義、404 (ページが見つかりません) エラー ページの一覧表示、301 または 302 ページ リダイレクトの実行、特定の IP アドレスまたは他の Web サイトからのアクセスのブロックなど、多くのチェックを実行します。したがって、.htaccess ファイルを使用すると、Apache [HTTP](/web/http/) サーバーの全体的なパフォーマンスが低下します。

## HTACCESS ファイル形式

HTACCESS ファイルは、プレーン テキスト ファイル形式でディスクに保存されます。これは、これらのファイルを任意のテキスト エディタで開いて編集できることを意味します。 「。」の前に名前はありません。 .htaccess ファイルで、フォルダー内の隠しファイルであることを示します。

## HTACCESS ファイルの一般的な用途

HTACCESS ファイルの 5 つの一般的な用途は次のとおりです。

### Mod_Rewrite

HTACCESS ファイルを使用して、Web サイト上の URL と Web ページをユーザーに表示する方法を指定および変更できます。

### 認証

.htpasswd という名前のパスワード ファイルを作成することにより、.htaccess で認証を行うことができます。これにより、サイトの訪問者は、Web ページの特定のセクションにアクセスしたい場合にパスワードを入力できます。

### カスタム エラー ページ

.htaccess ファイルを使用して、400 Bad Request、401 Authorization Required、403 Forbidden Page、404 File not Found、500 Internal Error などのカスタム エラー ページを作成できます。ただし、ページにアクセスするとすべてのチェックが実行されるため、サーバーのパフォーマンスが低下します。

### MIME タイプ

Apache HTACCESS ファイルを変更して、Multipurpose Internet Mail Extensions (MIME) タイプを含めることができます。これにより、サーバーは、サイトでサポートされていないアプリケーション ファイルの配信をサポートできます。

### SSI

サーバー サイド インクルード (SSI) は、Web サイトで時間を大幅に節約します。 SSI は、次のコードを .htaccess ファイルに挿入することで有効にできます。

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS ファイルの例

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## 参考文献

* [Apache HTTP Server チュートリアル: .htaccess ファイル](https://httpd.apache.org/docs/current/howto/htaccess.html)

