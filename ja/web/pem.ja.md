{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM ファイル - プライバシー強化メール証明書ファイル形式",
  "description":"PEM ファイル形式と,PEM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## .PEM オプション番号

PEM ファイルは、Web サーバーとブラウザーの間で安全な通信チャネルを確立するために使用されるセキュリティ証明書ファイルです。これは Base64 でエンコードされており、秘密鍵、サーバー証明書、および/または他の証明書の組み合わせが含まれている場合があります。 PEM ファイルは、使用方法に関しては .der 証明書ファイルに似ていますが、バイナリ データではなく、Base64 でエンコードされたテキストとして保存されます。他の同様の証明書ファイル形式には、[.cer](/web/cer/) および [.crt](/web/crt/) ファイルがあります。

**PEM ファイルを開く**ことができるアプリケーションには、Microsoft メモ帳や Apple TextEdit などのテキスト エディターが含まれます。

## PEM ファイル形式

PEM は、データの格納に使用されるファイルの構造とエンコード タイプを定義するコンテナ ファイル形式です。 PEM ファイルは、人間が判読できない Base64 でエンコードされたファイル形式としてディスクに保存されます。標準では、PEM ファイルが次で始まると定義されています。

```
-----BEGIN <type>-----
```
そして次で終わります：
```
-----END <type>-----
```

これらの内部の他のすべてのコンテンツは base64 でエンコードされています (大文字と小文字、数字、+、および /)。 1 つの PEM ファイルは、他のプログラムで使用できる複数のブロックで構成できます。 PEM ファイルに複数の証明書が含まれている場合、各証明書は次のように個別のブロックで区切られます。

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### PEM ファイルの例

CERTIFICATE ブロックを含む PEM ファイルは通常、次のようになります。

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

RSA を含む PEM ファイルは次のように始まります。

```
-----BEGIN RSA PRIVATE KEY-----
```

## 参照 ##

* [公開鍵暗号](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C ファイルの作成方法](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

