{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S ファイル - デジタル署名された電子メール メッセージ",
  "description":"P7S ファイル形式と,P7S ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## .P7S ファイルとは何ですか?

P7S ファイルは、デジタル署名された電子メールで受信されるデジタル署名です。このファイルが電子メールの添付ファイルとして存在することで、電子メールが本物の送信元から送信されたことを確認できます。これにより、送信者のコンピューターに電子メール署名証明書がインストールされていることが保証されます。このような署名付き電子メールがユーザーのコンピューターから送信されると、送信者の名前を含む P7S ファイルが添付されます。署名付き電子メールをサポートする電子メール クライアントは、送信者の情報を見ることができます。

## P7S ファイル形式 - 詳細情報

S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S ファイルには、人間が判読できるプレーン テキスト形式の情報が含まれています。 Microsoft Outlook、Apple Mail、Mozilla Thunderbird などの電子メール クライアントは、S/MIME 電子メールからデジタル署名された情報を読み取ることをサポートしています。電子メールに署名すると、送信者の身元が確認され、メッセージが本物であることを受信者に伝えます。電子メールが電子メール クライアント ([EML](/email/eml/) または [MSG](/email/msg/)) からダウンロードされると、これらの P7S ファイルがこれらの電子メールに添付されていることがわかります。

P7S ファイルには、次の情報が含まれています。

* メールの発信元
* 送信日時、
*送信中に変更されたかどうか

この情報は、Public-Key Cryptography Standard #7 (PKCS7) テクノロジを使用して埋め込まれ、暗号化された署名が電子メールにデジタル的に添付されます。

## 参照 ##

* [Microsoft 署名ツール](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

