{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp KEY và API có thể tạo và mở tệp KEY.",
  "title" :"Định dạng tệp KEY - Tệp khóa riêng của thư được tăng cường bảo mật",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Tệp KEY là gì?

Tệp KEY là phần riêng tư của cơ chế bảo mật được lưu vào đĩa ở định dạng tệp Mal được tăng cường bảo mật (PEM). Nó được sử dụng để giải mã thông tin trao đổi giữa trình duyệt web và máy chủ web phục vụ các yêu cầu duyệt web. Tệp KEY chứa các chuỗi được mã hóa vô dụng đối với mắt người nhưng là bản chất của việc mã hóa/giải mã trao đổi thông tin như một phần của chứng chỉ SSL trên máy chủ web. Các tệp KEY được tạo tự động và được cài đặt ở cuối máy khách.

Bạn có thể mở các tệp **KEY** bằng bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Microsoft Notepad (Windows), Apple TextEdit (Mac) hoặc GitHub Atom (đa nền tảng). Các tệp KEY tương tự như các định dạng tệp [CRT](/vi/web/crt/) và [CER](/vi/web/cer/).

## Định dạng tệp KEY - Thông tin khác

Các tệp KEY được lưu vào đĩa dưới dạng tệp văn bản thuần túy nhưng là các chuỗi được mã hóa không thân thiện với con người để đọc. Trên thực tế, người dùng không hiểu gì về các chuỗi khi được mở trong trình soạn thảo văn bản. Chứng chỉ khóa riêng là bí mật và không được chia sẻ với bất kỳ ai. Toàn bộ quá trình bảo mật trao đổi thông tin qua internet bao gồm:

* **Public Key** - dùng để mã hóa thông tin người dùng để trao đổi dữ liệu giữa trình duyệt và máy chủ web
* **Private Key** - được sử dụng để giải mã thông tin khi máy chủ web nhận được

Chứng chỉ SSL, còn được gọi là chứng chỉ X.509, là duy nhất cho mỗi trang web. KEY bằng cú pháp sau:

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

### Ví dụ về tệp KEY

Sau đây là một ví dụ về tệp Khóa riêng.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Người giới thiệu

* [Khóa chung, Khóa riêng và chứng chỉ](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

