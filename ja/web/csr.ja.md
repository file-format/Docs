{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSRファイル - 証明書署名要求ファイル形式",
  "description" :"CSR ファイルとは何か,および CSR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## .CSR ファイルとは何ですか?

CSR ファイルは、SSL/TLS 証明書の要求に使用される **証明書署名要求** ファイルです。 SSL/TLS 証明書が必要な場合は、最終的にインストールされるサーバーで CSR を生成します。この CSR ファイルは、証明書の作成のために認証局 (CA) と共有されます。これには、共通名、組織、国などの情報が含まれ、さらに重要なこととして、証明書ファイルに統合され、対応する秘密鍵で署名された **公開鍵** が含まれます。

**CSR ファイルを開く**ことができるアプリケーションには、OpenSSL と Microsoft IIS が含まれます。

## 証明書署名要求ファイルの形式

CSR ファイルは Base-64 PEM 形式で作成され、Microsoft メモ帳などの単純なテキスト エディタで開いて表示できます。これには、ヘッダー **-----BEGIN NEW CERTIFICATE REQUEST-----** がファイルの先頭に、フッター **-----END NEW CERTIFICATE REQUEST-----** が含まれます。ファイルの終わり。

### CSRファイルはどのように見えますか?

CSR ファイルの簡単な例は次のとおりです。

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## CSRにはどのような情報が含まれていますか?

CSR ファイルには、次の情報が含まれています。

1. 「ビジネスおよびウェブサイトに関する情報」 - 一般名、組織、組織単位、市/地域、州/郡/地域 (S)、国、電子メール アドレスなどの情報が含まれます。
1. 「公開鍵」 - 証明書に含まれ、対応する秘密鍵を使用して復号化される送信データの暗号化に使用されます
1. 「鍵の種類と長さに関する情報」 - これは通常 RSA 2048 ですが、RSA 4096+ などのより大きなサイズの場合もあります。

## 参考文献

* [コンセプト アプリケーション サーバー](https://github.com/Devronium/ConceptApplicationServer)

