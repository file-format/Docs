{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"KEY ファイルの形式と,KEY ファイルを作成して開くことができる API について学びます。",
  "title" :"KEYファイル形式 - プライバシー強化メール秘密鍵ファイル",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## .KEY ファイルとは?

KEY ファイルは、Privacy-Enhanced Mal (PEM) ファイル形式でディスクに保存されるセキュリティ メカニズムの非公開部分です。これは、Web ブラウザーと、閲覧要求を処理する Web サーバーとの間で交換される情報を復号化するために使用されます。 KEYファイルには、人間の目には役に立たないエンコードされた文字列が含まれていますが、Webサーバー上のSSL証明書の一部として情報交換を暗号化/復号化するための本質です. KEY ファイルは自動的に生成され、クライアント側でインストールされます。

**KEY** ファイルは、Microsoft Notepad (Windows)、Apple TextEdit (Mac)、GitHub Atom (クロスプラットフォーム) などの任意のテキスト エディターで開くことができます。 KEY ファイルは、[CRT](/web/crt/) および [CER](/web/cer/) ファイル形式に似ています。

## KEY ファイル形式 - 詳細情報

KEY ファイルはプレーン テキスト ファイルとしてディスクに保存されますが、暗号化された文字列であり、人間にとって読みにくいものです。実際には、ユーザーはテキスト エディターで開いたときに文字列をまったく理解していません。秘密鍵証明書は機密情報であり、誰とも共有しないでください。インターネット上での情報交換を保護するための完全なプロセスには、次のものが含まれます。

* **公開鍵** - ブラウザと Web サーバー間のデータ交換のためにユーザーの情報を暗号化するために使用されます
* **秘密鍵** - Web サーバーが受信した情報を解読するために使用されます

X.509 証明書とも呼ばれる SSL 証明書は、Web サイトごとに一意です。次の構文を使用する KEY ファイル:

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

### キーファイルの例

以下は、秘密鍵ファイルの例です。
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参考文献

* [公開鍵、秘密鍵、証明書](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

