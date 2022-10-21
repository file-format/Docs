{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7 证书文件",
  "description":"了解 P7C 文件格式和可以创建和打开 P7C 文件的 API。",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .p7b 文件？

P7B 文件是一个安全证书文件，其中包含用于验证个人或设备的安全数字证书。与 [.cer](/zh/web/cer/) 证书文件类似，可以使用“安装证书"选项通过文件上的右键单击选项来安装 P7B 文件。 P7B 使用与 CER 文件格式不同的格式选项。它包含一个或多个使用 base64 (ASCII) 编码的 X.509 数字证书文件。 P7B 文件作为 [ZIP](/zh/compression/zip/) 文件接收或从证书颁发机构接收。

## P7B 文件格式

P7B 文件存储为可以在任何文本编辑器中打开的纯 ASCII 文件。它包含的公钥是一个编码字符串，从可读性的角度来看是没有意义的。

### P7B 文件格式示例

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参考 ＃＃

* [公钥密码学](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [如何创建 P7C 文件？](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

