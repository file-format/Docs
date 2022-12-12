{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp CSR - Định dạng tệp yêu cầu ký chứng chỉ",
  "description" :"Tìm hiểu về tệp CSR là gì và các API có thể tạo và mở tệp CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Tệp CSR là gì?

Tệp CSR là tệp **Yêu cầu ký chứng chỉ** được sử dụng để yêu cầu chứng chỉ SSL/TLS. Khi bạn cần có chứng chỉ SSL/TLS, bạn tạo CSR trên cùng một máy chủ nơi nó sẽ được cài đặt cuối cùng. Tệp CSR này được chia sẻ với Tổ chức phát hành chứng chỉ (CA) để tạo chứng chỉ. Nó chứa thông tin như tên chung, tổ chức, quốc gia và quan trọng hơn là **khóa chung** được tích hợp trong tệp chứng chỉ của bạn và được ký bằng khóa riêng tư tương ứng.

Các ứng dụng có thể **mở tệp CSR** bao gồm OpenSSL và Microsoft IIS.

## Định dạng tệp yêu cầu ký chứng chỉ

Tệp CSR được tạo ở định dạng Base-64 PEM có thể được mở và xem trong trình soạn thảo văn bản đơn giản, chẳng hạn như Microsoft Notepad. Nó bao gồm một tiêu đề **----- BEGIN NEW CERTIFICATE YÊU CẦU-----** ở đầu tệp và một footer **------ END NEW CERTIFICATE YÊU CẦU-----** tại phần cuối của tập tin.

### Tệp CSR trông như thế nào?

Một ví dụ đơn giản về tệp CSR như sau.

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

## Thông tin nào được bao gồm trong CSR?

Tệp CSR chứa thông tin sau.

1. `Thông tin về Doanh nghiệp và Trang web` - Bao gồm các thông tin như Tên chung, Tổ chức, Đơn vị tổ chức, Thành phố/Địa phương, Tiểu bang/Hạt/Khu vực (S), Quốc gia và Địa chỉ Email
1. `Khóa chung` - Nó được bao gồm trong chứng chỉ và được sử dụng để mã hóa dữ liệu truyền đi được giải mã bằng khóa riêng tương ứng
1. `Thông tin về Loại và Độ dài Khóa` - Đây thường là RSA 2048 nhưng cũng có thể có các kích thước lớn hơn, chẳng hạn như RSA 4096+

## Người giới thiệu

* [Máy chủ ứng dụng khái niệm](https://github.com/Devronium/ConceptApplicationServer)

