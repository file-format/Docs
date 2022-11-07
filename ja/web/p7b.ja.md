{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7 証明書ファイル",
  "description":"P7C ファイル形式と,P7C ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .P7B ファイルとは?

P7B ファイルは、個人またはデバイスを認証するための安全なデジタル証明書を含むセキュリティ証明書ファイルです。 [.cer](/web/cer/) 証明書ファイルと同様に、P7B ファイルは、ファイルの右クリック オプションを使用して [証明書のインストール] オプションを使用してインストールできます。 P7B は、CER ファイル形式とは異なる形式オプションを使用します。 base64 (ASCII) エンコーディングを使用する 1 つ以上の X.509 デジタル証明書ファイルが含まれています。 P7B ファイルは [ZIP](/compression/zip/) ファイルとして受け取るか、認証局から受け取ります。

## P7B ファイル形式

P7B ファイルは、任意のテキスト エディターで開くことができるプレーン ASCII ファイルとして保存されます。読みやすさの観点からは意味のないエンコードされた文字列である公開鍵が含まれています。

### P7B ファイル形式の例

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参照 ##

* [公開鍵暗号](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C ファイルの作成方法](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

