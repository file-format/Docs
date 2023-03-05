{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail ファイル形式",
  "description":"EMLX ファイル形式と,EMLX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .EMLX オプション番号

EMLX ファイル形式は、Apple によって実装および開発されています。 Apple Mail アプリケーションは、電子メールのエクスポートに EMLX ファイル形式を使用します。 EMLXファイルを開いて、これらを他のファイル形式に変換できる他のアプリケーションもあります。

## EMLX ファイル形式の歴史

Mac OS X オペレーティング システムは、NeXTSTEP オペレーティング システムの一部として NeXT によって作成された既存の電子メール プログラム、NeXTMail を採用しました。 Apple は NeXT を買収した後、その機能を強化し、デフォルトのメール クライアントとして使用される Apple Mail メール アプリケーションになりました。 Apple Mail 経由でエクスポートされた電子メールは、EMLX ファイルとして直接保存されます。さらに、誰かが Mac OS でこれらをダブルクリックして開くと、EMLX ファイルのデフォルトのメール クライアントになります。

## EMLX ファイル形式

EMLx ファイルは、メモ帳などのテキスト エディターで開くことができる単純なテキスト ベースのファイルです。 EMLX ファイル構造は、次の 3 つの部分で構成されています。

* メッセージのバイト数 - ASCII で 10 進数で記述され、0x0a で終了するメッセージ自体の長さ
※メッセージそのもの
* XML plist 形式のメッセージ メタデータ

これらは、Apple Mail から EMLX として抽出された次のサンプル メールをテキスト エディターで開くことで、よりよく説明できます。

### EMLX の例

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

この例では、875 はメッセージの全長を示しています。メッセージのメタデータは、<plist>タグとフラグは次のように記述されています。

|フィールド|説明|値
---|---|---|
|0|読み取り|1 << 0
|1|削除|1 << 1
|2|回答済み|1 << 2
|3|暗号化|1 << 3
|4|フラグ付き|1 << 4
|5|最近|1 << 5
|6|下書き|1 << 6
|7|初期 (現在は使用されていません)|1 << 7
|8|転送済み|1 << 8
|9|リダイレクト|1 << 9
|10-15|添付ファイル数|3F << 10 (6 ビット)
|16-22|優先度|7F << 16 (7 ビット)
|23|署名|1 << 23
|24|がらくたです|1 << 24
|25|ジャンクではない|1 << 25
|26-28|フォント サイズ デルタ|7 << 26 (3 ビット)
|29|記録された迷惑メールレベル|1 << 29
|30|目次のテキストをハイライト|1 << 30
|31|(未使用)|

## 関連項目 ##

* [EML](/メール/eml/)
* [メッセージ](/email/msg/)

