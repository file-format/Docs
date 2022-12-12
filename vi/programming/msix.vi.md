{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Tệp MSIX là gì?",
  "description":"Tìm hiểu về tệp MSIX và API có thể tạo và mở tệp MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Tệp MSIX là gì?

Tệp MSIX là định dạng đóng gói ứng dụng Windows được sử dụng để tạo và phân phối ứng dụng trong Windows 10. Đây là định dạng tệp gói hiện đại so với [APPX](/vi/programming/appx/) và MSI cuối cùng sẽ bị loại bỏ sang định dạng tệp mới này. Nó có thể được sử dụng để triển khai các ứng dụng Win32, WPF và Windows Forms. Các tệp MSIX đáng tin cậy và nhắm mục tiêu tối ưu hóa không gian đĩa và mạng. Các nhà phát triển sử dụng chúng để phân phối chương trình cho người dùng cuối thông qua Microsoft Store (trước đây gọi là Windows Store).

## Định dạng tệp MSIX - Thông tin khác

Các tệp MSIX được nén [ZIP](/vi/compression/zip/), với tất cả các tệp được bao gồm bên trong tệp được đóng gói. Ngoài các tệp liên quan đến ứng dụng, tệp MSIX chứa các tệp cấu hình [.xml](/vi/web/xml/) chứa thông tin liên quan đến cài đặt ứng dụng.

## Có gì bên trong một gói MSIX?

Gói MSIX bao gồm các tệp sau.

* `AppxBlockMap.xml` - Được gọi là tệp bản đồ khối gói, đây là tài liệu XML chứa danh sách các tệp của ứng dụng có chỉ mục và giá trị băm mật mã cho từng khối dữ liệu được lưu trữ trong gói.
* `AppxManifest.xml` - Một tài liệu XML chứa thông tin cần thiết để triển khai, hiển thị và cập nhật ứng dụng MSIX. Thông tin này bao gồm nhận dạng gói, phần phụ thuộc gói, khả năng cần thiết, yếu tố hình ảnh và điểm mở rộng.
* `AppxSignature.p7x` - Tệp được tạo khi gói được ký. Tất cả các gói MSIX đều phải được ký trước khi cài đặt. Với AppxBlockmap.xml, nền tảng có thể cài đặt gói và được xác thực.

## Người giới thiệu

* [Tổng quan về MSIX](https://docs.microsoft.com/en-us/windows/msix/overview)
* [Tạo tệp APPX bằng Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

