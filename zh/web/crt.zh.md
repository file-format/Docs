{
  "date" : "2019-10-11",
  "keywords" :["crt","crt 文件","crt 文件格式","crt 文件类型","文件","类型","什么是 crt 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - 安全证书文件格式",
  "description":"了解 CRT 文件格式和可以创建和打开 CRT 文件的 API。",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .crt 文件？

带有 .crt 扩展名的文件是一个安全证书文件，安全网站使用它来建立从 Web 服务器到浏览器的安全连接。安全网站可以确保数据传输、登录、支付卡交易的安全，并为网站提供受保护的浏览。如果您打开一个安全网站，您会在地址栏中看到一个“锁定"图标。如果单击它，您可以查看已安装证书的详细信息。 Verisign 和 Thawte 等国际公司分发这些 SSL 证书。

## CRT 文件格式

CRT 文件为 ASCII 格式，可以在任何文本编辑器中打开以查看证书文件的内容。它遵循定义证书结构的 X.509 认证标准。它定义了应包含在 SSL 证书中的数据字段。 CRT 属于 PEM 格式的证书，它是 Base64 ASCII 编码文件。

### PEM 文件结构

一个 PEM 文件可以有多个证书。在这种情况下，PEM 文件中的每个证书都遵循以下结构。

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

### CRT 文件格式示例

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参考 ＃＃

* [公钥、私钥和证书](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

