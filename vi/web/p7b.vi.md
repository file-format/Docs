{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp chứng chỉ P7B - PKCS 7",
  "description":"Tìm hiểu về định dạng tệp P7C và các API có thể tạo và mở tệp P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp P7B là gì?

Tệp P7B là tệp chứng chỉ bảo mật chứa chứng chỉ kỹ thuật số an toàn để xác thực một người hoặc một thiết bị. Tương tự như tệp chứng chỉ [.cer](/vi/web/cer/), tệp P7B có thể được cài đặt bằng tùy chọn "Cài đặt chứng chỉ" bằng cách sử dụng tùy chọn nhấp chuột phải vào tệp. P7B sử dụng tùy chọn định dạng khác với định dạng tệp CER. Nó chứa một hoặc nhiều tệp chứng chỉ kỹ thuật số X.509 sử dụng mã hóa base64 (ASCII). Các tệp P7B được nhận dưới dạng tệp [ZIP](/vi/compression/zip/) hoặc được nhận từ Tổ chức phát hành chứng chỉ.

## Định dạng tệp P7B

Các tệp P7B được lưu trữ dưới dạng tệp ASCII đơn giản có thể được mở trong bất kỳ trình soạn thảo văn bản nào. Nó chứa khóa chung là một chuỗi được mã hóa, vô nghĩa theo quan điểm dễ đọc.

### Ví dụ về định dạng tệp P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Người giới thiệu ##

* [Mật mã khóa công khai](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Cách tạo tệp P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

