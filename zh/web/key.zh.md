{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 KEY 文件格式和可以创建和打开 KEY 文件的 API。",
  "title" :"密钥文件格式 - 增强隐私的邮件私钥文件",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
"identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## 什么是 KEY 文件？

KEY 文件是以隐私增强恶意 (PEM) 文件格式保存到光盘的安全机制的私有部分。它用于解密在 Web 浏览器和为浏览请求提供服务的 Web 服务器之间交换的信息。 KEY 文件包含对人眼无用的编码字符串，但作为 Web 服务器上 SSL 证书的一部分，它是加密/解密信息交换的本质。 KEY 文件自动生成并安装在客户端。

您可以使用任何文本编辑器打开 **KEY** 文件，例如 Microsoft Notepad (Windows)、Apple TextEdit (Mac) 或 GitHub Atom（跨平台）。 KEY 文件类似于 [CRT](/zh/web/crt/) 和 [CER](/zh/web/cer/) 文件格式。

## KEY 文件格式 - 更多信息

KEY 文件以纯文本文件的形式存储到光盘中，但它们是编码字符串，不便于阅读。实际上，用户在文本编辑器中打开字符串时对字符串的理解为零。私钥证书是机密的，不应与任何人共享。确保通过 Internet 进行信息交换的完整过程包括：

* **公钥** - 用于加密用户信息以在浏览器和网络服务器之间交换数据
* **私钥** - 用于解密 Web 服务器接收到的信息

SSL 证书（也称为 X.509 证书）对于每个网站都是唯一的。 KEY 文件使用以下语法：

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

### KEY 文件示例

以下是私钥文件的示例。
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 参考

* [公钥、私钥和证书](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

