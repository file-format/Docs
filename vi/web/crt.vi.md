{
  "date" : "2019-10-11",
  "keywords" :[ "crt","tệp crt", "định dạng tệp crt", "loại tệp crt", "tệp", "loại", "tệp crt là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Định dạng tệp chứng chỉ bảo mật",
  "description":"Tìm hiểu về định dạng tệp CRT và API có thể tạo và mở tệp CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp CRT là gì?

Tệp có phần mở rộng .crt là tệp chứng chỉ bảo mật được các trang web bảo mật sử dụng để thiết lập kết nối bảo mật từ máy chủ web đến trình duyệt. Các trang web an toàn cho phép chuyển dữ liệu an toàn, đăng nhập, giao dịch thẻ thanh toán và cung cấp trình duyệt được bảo vệ cho trang web. Nếu bạn mở một trang web an toàn, bạn sẽ thấy biểu tượng "khóa" trên thanh địa chỉ. Nếu bạn nhấp vào nó, bạn có thể xem chi tiết của chứng chỉ đã cài đặt. Các công ty quốc tế như Verisign và Thawte phân phối các chứng chỉ SSL này.

## Định dạng tệp CRT

Các tệp CRT ở định dạng ASCII và có thể được mở trong bất kỳ trình soạn thảo văn bản nào để xem nội dung của tệp chứng chỉ. Nó tuân theo tiêu chuẩn chứng nhận X.509 xác định cấu trúc của chứng chỉ. Nó xác định các trường dữ liệu nên có trong chứng chỉ SSL. CRT thuộc định dạng chứng chỉ PEM là các tệp được mã hóa Base64 ASCII.

### Cấu trúc tệp PEM

Một tệp PEM có thể có nhiều chứng chỉ. Trong trường hợp này, mỗi chứng chỉ trong tệp PEM tuân theo cấu trúc sau.

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

### Ví dụ về định dạng tệp CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Người giới thiệu ##

* [Khóa chung, Khóa riêng và chứng chỉ](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

