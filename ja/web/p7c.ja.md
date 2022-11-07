{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 証明書ファイル",
  "description":"P7C ファイル形式と,P7C ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .P7C オプション番号

P7C ファイルは、他のセキュリティ証明書ファイルと同様に、ネットワーク上で ID を認証するために使用されるデジタル証明書です。証明書を使用するアプリケーションは、これらの証明書ファイルに含まれる公開鍵を使用して ID を認証します。公開鍵暗号方式 (非対称暗号方式) は、一方が公開鍵で、もう一方が秘密鍵と呼ばれる鍵のペアを使用します。秘密鍵は効果的なセキュリティのために安全に保管されますが、公開鍵は他のユーザーと共有できます。その他の一般的な証明書ファイル形式には、[CRT](/web/crt/)、DER、PEM などがあります。

## P7C ファイル形式 - 詳細情報

P7C ファイルはバイナリ ファイルとしてディスクに保存され、数学的問題に基づく暗号化アルゴリズムを使用して生成された公開鍵情報が含まれます。これらは任意のテキスト エディターで開くことができますが、その内容は人間が判読できる形式ではありません。 P7C ファイルを開くことができるアプリケーションには、Apple Keychain Access、Adobe Acrobat Reader DC、Microsoft Certificate Manager、Microsoft Windows Contacts などがあります。

### P7C ファイル形式の例

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参照 ##

* [公開鍵暗号](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C ファイルの作成方法](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

