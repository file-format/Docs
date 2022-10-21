{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 证书文件",
  "description":"了解 P7C 文件格式和可以创建和打开 P7C 文件的 API。",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .p7c 文件？

与其他安全证书文件一样，P7C 文件是一种数字证书，用于通过网络验证身份。使用证书的应用程序使用这些证书文件中包含的公钥来验证身份。公钥密码学或非对称密码学使用一对密钥，其中一个是公钥，另一个称为私钥。私钥保持安全以实现有效安全，而公钥可以与他人共享。其他常见的证书文件格式包括 [CRT](/zh/web/crt/)、DER 和 PEM。

## P7C 文件格式 - 更多信息

P7C 文件以二进制文件的形式保存到光盘中，并包含使用基于数学问题的密码算法生成的公钥信息。这些可以在任何文本编辑器中打开，但它们的内容不是人类可读的形式。一些可以打开 P7C 文件的应用程序包括 Apple Keychain Access、Adobe Acrobat Reader DC、Microsoft Certificate Manager 和 Microsoft Windows Contacts。

### P7C 文件格式示例

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参考 ＃＃

* [公钥密码学](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [如何创建 P7C 文件？](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

