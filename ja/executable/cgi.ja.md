{
  "date" : "2021-06-28",
  "keywords" :[ "cgi ファイル", "cgi ファイルとは", "ファイル", "cgi の例", "cgi ファイルの拡張子","拡張子", "フォーマット" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"CGI ファイル形式と,CGI ファイルを作成して開くことができる API について学びます。",
  "title" :"CGI - 共通ゲートウェイ インターフェイス スクリプト ファイル",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## .CGI ファイルとは何ですか?
CGI ファイルは、Web サーバーが外部プログラムを実行してユーザー要求を処理するために使用する Common Gateway Interface スクリプトとして知られています。拡張子が .cgi のファイルに保存されたスクリプトは、通常、C または Perl プログラミング言語で記述されています。は、Web 開発者がデータベースを Web サーバーに接続したいと考えていた Web の黎明期から導入されていました。 Web サーバーとデータベース間の共通ゲートウェイをサポートするサーバーは、CGI コードの実行に適していました。

## CGI ファイル形式
CGI スクリプトは Web サーバーで使用され、所有者が URL の処理方法を簡単に構成できるようにします。この手順は通常、新しいディレクトリ (ドキュメントが主に置かれている場所) を CGI スクリプトを含むものとしてマークすることによって行われます。その一般的な名前は cgi-bin です。たとえば、/usr/local/apache/htdocs/cgi-bin を Web サーバーの CGI ディレクトリとして選択できます。 Web ブラウザーが CGI ディレクトリ内のファイルを指す URL を要求すると、そのファイル (/usr/local/apache/htdocs/cgi-bin/printenv.pl) を Web ブラウザーに単純に送信する代わりに、HTTPサーバーは指定されたスクリプトを実行し、スクリプトの出力を Web ブラウザーに返します。つまり、CGI スクリプトが標準出力に送信するものはすべて、ウィンドウのターミナルに表示される代わりに、Web クライアントに転送されます。

### CGI の例

次の Perl で書かれた CGI スクリプトは、Web サーバーから渡されたすべての環境変数を表示します。
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

出力は次のようになります。
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## CGI スクリプトの使用
CGI スクリプトを含む CGI ファイルは、通常、ユーザーからの入力データを処理し、関連する出力データを生成するために使用されます。 wiki の実装は、CGI プログラムの例の 1 つです。ユーザー エージェントがエントリの名前の要求を送信すると、Web サーバーは CGI プログラムを実行します。 CGI プログラムは、そのエントリのページのソースを取得し、それを HTML に変換して、結果を出力します。 Web サーバーは、CGI プログラムからの出力を受け取り、それをユーザー エージェントに返します。次に、ユーザー エージェントが [ページの編集] ボタンをクリックして編集機能を呼び出すと、CGI プログラムはページのコンテンツを含む HTML テキスト領域またはその他の編集コントロールを表示します。最後に、ユーザー エージェントが [ページを公開] ボタンをクリックすると、CGI プログラムは更新された HTML をそのエントリのページのソースに変換して保存します。



## 参考文献

* [共通ゲートウェイ インターフェイス - ウィキペディアによる](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

