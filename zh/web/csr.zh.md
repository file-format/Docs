{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR 文件 - 证书签名请求文件格式",
  "description" :"了解什么是 CSR 文件以及可以创建和打开 CSR 文件的 API。",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
"标识符":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## 什么是一 .csr 文件？

CSR 文件是一个 **Certificate Signing Request** 文件，用于请求 SSL/TLS 证书。当您需要 SSL/TLS 证书时，您可以在最终安装它的同一台服务器上生成 CSR。此 CSR 文件与证书颁发机构 (CA) 共享以创建证书。它包含通用名称、组织、国家/地区等信息，更重要的是，集成在您的证书文件中并使用相应的私钥签名的**公钥**。

可以**打开 CSR 文件**的应用程序包括 OpenSSL 和 Microsoft IIS。

## 证书签名请求文件格式

CSR 文件以 Base-64 PEM 格式创建，可以在 Microsoft 记事本等简单的文本编辑器中打开和查看。它包括文件开头的标题 **-----BEGIN NEW CERTIFICATE REQUEST-----** 和页脚 **-----END NEW CERTIFICATE REQUEST-----** 在文件的结尾。

### CSR 文件的外观如何？

CSR 文件的一个简单示例如下。

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

## CSR 中包含哪些信息？

CSR 文件包含以下信息。

1. `关于企业和网站的信息` - 包括通用名称、组织、组织单位、城市/地区、州/县/地区 (S)、国家和电子邮件地址等信息
1. `Public Key` - 它包含在证书中，用于加密传输的数据，使用相应的私钥解密
1. `关于密钥类型和长度的信息` - 这通常是 RSA 2048，但也可能有更大的尺寸，例如 RSA 4096+

## 参考

* [概念应用服务器](https://github.com/Devronium/ConceptApplicationServer)

