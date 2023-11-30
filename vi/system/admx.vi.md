{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp ADMX - Định dạng tệp mẫu quản trị chính sách nhóm",
  "description":"Tìm hiểu về định dạng tệp ADMX và cách mở tệp ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Một tập tin ADMX là gì?

Tệp ADMX là tệp cấu hình chính sách được sử dụng bởi phần mềm Chính sách nhóm Microsoft Windows để quản lý nhóm máy tính trong một nhóm. Đây là tệp mẫu quản trị dựa trên XML và được giới thiệu cùng với Windows Vista Service Pack 1. Các tệp ADMX chứa cài đặt cấu hình cho tài khoản người dùng, cấu hình hệ điều hành và ứng dụng. Các tệp ADMX được sử dụng để lưu trữ và triển khai các cấu hình để quản lý tập trung nhiều hệ thống máy tính.

Bạn có thể tạo hoặc chỉnh sửa các tệp ADMX bằng cách sử dụng bất kỳ trình soạn thảo văn bản nào tương thích với XML, bất kỳ trình soạn thảo văn bản nào hoặc Trình soạn thảo đối tượng chính sách nhóm của Microsoft.

## Định dạng tệp ADMX - Thông tin thêm

Các tệp ADMX được lưu trữ ở định dạng tệp [XML](/vi/web/xml/) phổ biến mà con người có thể đọc được. Đây là định dạng tệp đa ngôn ngữ và cho phép quản trị viên hệ thống từ các ngôn ngữ khác nhau làm việc với cùng một tệp ADMX. Các tệp ADMX đã thay thế định dạng tệp [ADM](/vi/system/adm/) cũ là định dạng tệp văn bản có định dạng unicode. Tệp ADMX chỉ định các khóa đăng ký được thay đổi khi thay đổi cài đặt Chính sách nhóm nhất định.

### Tôi có thể làm gì với tệp ADMX?

Các tệp ADMX xác định những hành động nào được phép đối với các máy tính của người dùng là một phần của nhóm. Chính sách nhóm áp đặt các quy tắc được đặt kết hợp với phần mềm Active Directory. Các tệp ADMX được quản lý từ cửa hàng trung tâm trên hệ điều hành Windows, vị trí trung tâm trong miền.

Tệp ADMX được triển khai trong môi trường làm việc có thể cho phép quản trị viên triển khai các chính sách như:

* Kiểm soát việc sử dụng internet
* Tải xuống một số loại tệp nhất định
* Sử dụng các thiết bị di động trên hệ thống

## Người giới thiệu

* [Tệp mẫu quản trị - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Quản lý tệp mẫu quản trị](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

