{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp PEM - Định dạng tệp chứng chỉ thư nâng cao quyền riêng tư",
  "description":"Tìm hiểu về định dạng tệp PEM và các API có thể tạo và mở tệp PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Tệp PEM là gì?

Tệp PEM là tệp chứng chỉ bảo mật được sử dụng để thiết lập kênh liên lạc an toàn giữa máy chủ web và trình duyệt. Nó được mã hóa Base64 và có thể chứa khóa riêng, chứng chỉ máy chủ và/hoặc kết hợp các chứng chỉ khác. Các tệp PEM tương tự như các tệp chứng chỉ .der về cách sử dụng nhưng được lưu trữ dưới dạng văn bản được mã hóa Base64 thay vì dữ liệu nhị phân. Các định dạng tệp chứng chỉ tương tự khác bao gồm các tệp [.cer](/vi/web/cer/) và [.crt](/vi/web/crt/).

Các ứng dụng có thể **mở tệp PEM** bao gồm các trình soạn thảo văn bản như Microsoft Notepad và Apple TextEdit.

## Định dạng tệp PEM

PEM là định dạng tệp chứa xác định cấu trúc và loại mã hóa của tệp được sử dụng để lưu trữ dữ liệu. Các tệp PEM được lưu trữ vào đĩa dưới dạng định dạng tệp được mã hóa Base64 mà con người không thể đọc được. Tiêu chuẩn xác định rằng tệp PEM bắt đầu bằng:

```
-----BEGIN <type>-----
```
và kết thúc bằng:
```
-----END <type>-----
```

Tất cả nội dung khác bên trong chúng đều được mã hóa base64 (chữ hoa và chữ thường, chữ số, + và /). Một tệp PEM có thể bao gồm nhiều khối có thể được sử dụng bởi các chương trình khác. Nếu tệp PEM chứa nhiều chứng chỉ, mỗi chứng chỉ được phân tách bằng các khối riêng lẻ như sau:

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

### Ví dụ về tệp PEM

Tệp PEM có khối CERTIFICATE thường có dạng như sau:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Tệp PEM có RSA bắt đầu như sau.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Người giới thiệu ##

* [Mật mã khóa công khai](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Cách tạo tệp P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

