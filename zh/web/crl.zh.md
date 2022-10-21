{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRL 文件 - 证书吊销列表",
  "description":"了解 CRL 文件格式和可以创建和打开 CRL 文件的 API。",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## 什么是一 .crl 文件？

CRL（证书吊销列表）文件是 X.509 数字证书的黑名单，证书颁发机构 (CA) 在指定的吊销日期之前吊销这些证书。它包含有关问题和吊销日期的信息，让安全管理员可以阻止受影响的数字证书。 CRL 不包括过期证书，因为它的主要目的是通知不受信任和无效的证书。

可以**打开 CRL 文件**的应用程序包括 OpenSSL、Microsoft IIS Server 和 Citrix NetScaler。

## CRL 文件格式 - 更多信息

CRL 文件包含 X.509 标准中的信息，该标准还定义了共享公钥信息的语义。 CRL 文件中包含的其他信息可能包括证书被吊销的时间限制、吊销原因、吊销证书的序列号和时间戳。


### 将证书添加到 CRL 的主要原因

撤销您网站的证书并将其添加到 CRL 可能有多种原因。其中一些可能是；

1.您的证书私钥已泄露
1. 您的证书无效或由 CA 错误签发
1. 与证书相关的组织细节发生变化，CA 颁发新证书
1. 其他不能避免的证书被吊销的原因

## 参考

* [美国国家标准与技术研究院 (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [互联网工程任务组 (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [证书撤销列表](https://en.wikipedia.org/wiki/Certificate_revocation_list)

