{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp CMS - Tệp hồ sơ dịch vụ quản lý kết nối",
  "description":"Tìm hiểu về tệp CMS và các API có thể tạo và mở tệp CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Tệp CMS là gì?

Tệp CMS là tệp dữ liệu chứa thông tin cấu hình được Microsoft Windows Connection Manager sử dụng. Nó cho phép người dùng từ xa kết nối với mạng bằng thông tin hồ sơ này. Thông tin được lưu trữ bên trong tệp CMS bao gồm dữ liệu về hệ điều hành của người dùng và các quyền được sử dụng để thiết lập kết nối giữa người dùng từ xa và mạng. Quản trị viên CMS sử dụng Bộ công cụ quản trị trình quản lý kết nối (CMAK) để tạo tệp CMS.

## Định dạng tệp CMS - Thông tin khác

Các tệp CMS không được tìm thấy phổ biến trên máy người dùng. Vì chúng được sử dụng đặc biệt để cho phép người dùng từ xa kết nối mạng, nên bạn sẽ tìm thấy chúng trên các máy tính được sử dụng để kết nối với mạng công ty hoặc một số văn phòng xây dựng có mục đích cụ thể. Trong hầu hết các trường hợp, nó được sử dụng để kết nối với mạng tổ chức, chẳng hạn như Mạng riêng ảo (VPN) chỉ dành riêng cho một công ty. Là quản trị viên mạng, bạn sẽ thiết lập quyền truy cập vào mạng như vậy với Trình quản lý kết nối để cho phép anh ta truy cập mạng công ty từ một vị trí từ xa.

### Insdie CMS là gì?

Tệp cấu hình CMS được tạo bằng Trình quản lý kết nối và được đóng gói cùng với các tệp cấu hình khác trước khi được cung cấp cho người dùng từ xa. Các tệp bổ sung này có thể bao gồm tệp CMP và tệp INF được đóng gói cùng với tệp [EXE](/vi/executable/exe/). Gói hoàn chỉnh này được cung cấp cho người dùng từ xa để kết nối với mạng.

## Người giới thiệu

* [Hiểu và định cấu hình Trình quản lý kết nối Windows](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/under Hiểu-and-configure-windows-connection-manager)

