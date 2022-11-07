{
  "date" : "2019-10-11",
  "keywords" :[ "crt","crt ファイル", "crt ファイル形式", "crt ファイルの種類", "ファイル", "種類", "crt ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - セキュリティ証明書ファイル形式",
  "description":"CRT ファイル形式と,CRT ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .CRT オプション番号

拡張子が .crt のファイルは、Web サーバーからブラウザへの安全な接続を確立するために安全な Web サイトで使用されるセキュリティ証明書ファイルです。安全な Web サイトは、データ転送、ログイン、支払いカード取引を保護し、サイトへの保護されたブラウジングを提供することを可能にします。セキュリティで保護された Web サイトを開くと、アドレス バーに「ロック」アイコンが表示されます。それをクリックすると、インストールされている証明書の詳細を表示できます。 Verisign や Thawte などの国際企業がこれらの SSL 証明書を配布しています。

## CRT ファイル形式

CRT ファイルは ASCII 形式で、任意のテキスト エディターで開いて証明書ファイルの内容を表示できます。これは、証明書の構造を定義する X.509 認定基準に従います。 SSL 証明書に含める必要があるデータ フィールドを定義します。 CRT は、Base64 ASCII でエンコードされたファイルである証明書の PEM 形式に属します。

### PEM ファイルの構造

PEM ファイルには複数の証明書を含めることができます。このような場合、PEM ファイル内の各証明書は次の構造に従います。

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### CRT ファイル形式の例

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参照 ##

* [公開鍵、秘密鍵、証明書](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

