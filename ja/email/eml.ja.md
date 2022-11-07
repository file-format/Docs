{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - メールメッセージ",
  "description":"EML ファイル形式と,EML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## .EML オプション番号

EML ファイル形式は、Outlook およびその他の関連アプリケーションを使用して保存された電子メール メッセージを表します。ほとんどすべての電子メール クライアントは、RFC-822 Internet Message Format Standard に準拠するために、このファイル形式をサポートしています。 Microsoft Outlook は、EML メッセージ タイプを開くためのデフォルトのソフトウェアです。 EML ファイルは、ディスクへの保存や、通信プロトコルを使用した受信者への送信に使用できます。

## EMLの歴史

EML ファイル形式の仕様は、[RFC 822](http://www.ietf.org/rfc/rfc0822.txt) 標準形式に従って入手できます。 RFC-822 より前は、RFC-733 がネットワーク メッセージ交換のルールを管理していましたが、1982 年に前者は ARPA 標準を確立することによりラテラルの改良として作成されました。同時に、Microsoft は独自の電子メール クライアント、つまり Outlook Express を開発するための独自の COM モジュールを作成しました。 RFC-822 は、Microsoft がオープン スタンダードから逸脱し、電子メールが高度に構造化されたデータベース形式で保存される [PST](/email/pst/) ファイル形式を作成したときに、独自の形式として確立される道をたどりました。これにより、電子メールが Microsoft Outlook から転送されたときに、Microsoft 以外の電子メール クライアントのユーザーに問題が発生しました。

822 標準が 2822 (MIME RFC-822 形式で EML メッセージを作成、読み取り、送信するために現在使用されている Internet Message Format) に拡張されたのは 2001 年でした。

## EML ファイル形式の仕様

EML ファイルは、次の 2 つのセクションで構成されています。

* ヘッダー - メッセージ ヘッダーに関する情報が含まれます
* メッセージ本文 - メッセージの内容、埋め込み画像、添付ファイルを含む一連の情報が含まれます

### ヘッダー情報 ###

EML ファイルは、ヘッダー情報とオプションのメッセージ本文で構成されます。 EML の各ヘッダー行には、コロン「:」で区切られた 2 つの部分があります。最初のものはヘッダー名と呼ばれ、コロンに続くものはヘッダー本体です。たとえば、そのようなヘッダーには次のものが含まれます。

* 送信者のメールアドレス
* 受信者のメールアドレス
* メールの件名
* メッセージの日時スタンプ

**ヘッダーの例**

から：<John@bmw.eml.light.com>

に：<Andy@fileformat.com>

日付: 2018 年 3 月 8 日 (木) 10:43:37 +0100

件名: bmw eml ライト

＃＃＃ メッセージ本文 ＃＃＃

EML メッセージ本文には、電子メールの主要な情報がテキスト、ハイパーリンク、および添付ファイルの形式で含まれています。メール本文には読みやすいテキストを含めることができますが、必須ではありません。この場合、メッセージ本文は空にするか、エンコードされた添付データを含めることができます。

メッセージ本文の内容は、読み取りアプリケーションがそれぞれの形式で情報を読み取れるようにする Content-Type によって記述されます。実際には、ドキュメントの性質と形式を表します。 MIME タイプまたはコンテンツ タイプの構造は非常に単純です。 '/' で区切られた 2 つの文字列であるタイプとサブタイプで構成されます。スペースは使用できません。 「タイプ」はカテゴリを表し、離散型またはマルチパート型にすることができます。 「サブタイプ」は各タイプに固有です。コンテンツ タイプのカテゴリに分類されるタイプのリストは長いですが、いくつかの重要なコンテンツ タイプは次のとおりです。


|**タイプ**|**説明**|**サブタイプの例**
---|---|---|
|text|人が読める形式を表します|text/plain、text/html、text/css、text/javascript
|image|動画を除く任意のタイプの画像を表します|image/bmp、image/png、image/jpg、image/gif
|audio|任意のオーディオ ファイル形式を表します|audio/mdi、audio/wav
|application|あらゆる種類のバイナリ データを表します|application/octet-stream、application/vnd.mspowerpoint、application/xhtml+xml、application/xml、application/pdf

### EML 本文での添付ファイルの表現 ###

EML 本文には、含まれる各コンテンツ タイプの境界が含まれます。メッセージ本文の添付ファイルは、次の例に示すように、Content-Type と Content-Disposition によって識別されます。

コンテンツ タイプ: テキスト/プレーン。 charset#"windows-1252"; name#"apple app store.txt"
Content-Disposition: 添付;ファイル名#"apple app store.txt"
コンテンツ転送エンコーディング: base64
X-Attachment-Id: f_jkhztmd02

ご覧のように、Content-Disposition を attachment に設定すると、読み取りアプリケーションは、添付ファイル名や転送エンコーディングなどの添付情報を取得できます。添付ヘッダー情報の後に、読み取られるエンコードされた添付コンテンツが続きます。

#### 添付ファイルとしてのスプレッドシートの例 ####

コンテンツ タイプ: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
Content-Disposition: 添付;ファイル名#"english_spodr.xlsx"
コンテンツ転送エンコーディング: base64
X-Attachment-Id: f_jkhztmd43

## 参考文献

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

