{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM 文件 - 增强隐私的邮件证书文件格式",
  "description":"了解 PEM 文件格式和可以创建和打开 PEM 文件的 API。",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## 什么是一 .pem 文件？

PEM 文件是一个安全证书文件，用于在 Web 服务器和浏览器之间建立安全通信通道。它是 Base64 编码的，可能包含私钥、服务器证书和/或其他证书的组合。 PEM 文件在使用方面类似于 .der 证书文件，但存储为 Base64 编码文本而不是二进制数据。其他类似的证书文件格式包括 [.cer](/zh/web/cer/) 和 [.crt](/zh/web/crt/) 文件。

可以**打开 PEM 文件**的应用程序包括 Microsoft Notepad 和 Apple TextEdit 等文本编辑器。

## PEM 文件格式

PEM 是一种容器文件格式，它定义了用于存储数据的文件的结构和编码类型。 PEM 文件作为人类不可读的 Base64 编码文件格式存储到光盘中。该标准定义 PEM 文件以：

```
-----BEGIN <type>-----
```
并以：
```
-----END <type>-----
```

其中的所有其他内容都是 base64 编码的（大写和小写字母、数字、+ 和 /）。一个 PEM 文件可以包含多个可供其他程序使用的块。如果 PEM 文件包含多个证书，则每个证书由单独的块分隔，如下所示：

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

### PEM 文件示例

带有 CERTIFICATE 块的 PEM 文件通常如下所示：

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

带有 RSA 的 PEM 文件开始如下。

```
-----BEGIN RSA PRIVATE KEY-----
```

## 参考 ＃＃

* [公钥密码学](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [如何创建 P7C 文件？](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

