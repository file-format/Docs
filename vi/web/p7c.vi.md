{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp chứng chỉ P7C - PKCS 7",
  "description":"Tìm hiểu về định dạng tệp P7C và các API có thể tạo và mở tệp P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp P7C là gì?

Tệp P7C, giống như các tệp chứng chỉ bảo mật khác, là chứng chỉ kỹ thuật số được sử dụng để xác thực danh tính qua mạng. Các ứng dụng sử dụng chứng chỉ xác thực danh tính bằng khóa chung có trong các tệp chứng chỉ này. Mật mã khóa công khai, hoặc mật mã bất đối xứng, sử dụng cặp khóa trong đó một khóa là khóa chung và khóa còn lại được gọi là khóa riêng. Khóa riêng được giữ an toàn để bảo mật hiệu quả, trong khi khóa chung có thể được chia sẻ với người khác. Các định dạng tệp chứng chỉ phổ biến khác bao gồm [CRT](/vi/web/crt/), DER và PEM.

## Định dạng tệp P7C - Thông tin khác

Các tệp P7C được lưu vào đĩa dưới dạng tệp nhị phân và bao gồm thông tin khóa chung được tạo bằng thuật toán mã hóa dựa trên các bài toán. Chúng có thể được mở trong bất kỳ trình soạn thảo văn bản nào nhưng nội dung của chúng không ở dạng con người có thể đọc được. Một số ứng dụng có thể mở tệp P7C bao gồm Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager và Microsoft Windows Contacts.

### Ví dụ về định dạng tệp P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Người giới thiệu ##

* [Mật mã khóa công khai](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Cách tạo tệp P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

