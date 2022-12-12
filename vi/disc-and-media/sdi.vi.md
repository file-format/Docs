{
  "date" : "2021-08-13",
  "keywords" :[ "tệp sdi", "định dạng tệp sdi", "tệp sdi là gì", "tệp", "ví dụ sdi", "phần mở rộng tệp sdi","tiện ích mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp SDI và API có thể tạo và mở tệp SDI.",
  "title" :"SDI - Tệp hình ảnh triển khai hệ thống Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Tệp SDI là gì?
Tệp có phần mở rộng .sdi chứa một đốm màu tải, đốm màu khởi động và đốm màu một phần; thường được Windows Embedded Studio sử dụng để tạo đĩa RAM hoặc đĩa khởi động để tải và cài đặt Windows. SDI được viết tắt cho System Deployment Image. Windows Embedded Studio là một chương trình được sử dụng để tạo ảnh đĩa cho Windows. Trên thực tế, chương trình này chứa chương trình Trình quản lý tệp SDI và một công cụ dòng lệnh có tên **sdimgr.exe**, cả hai đều có thể được sử dụng để triển khai, tạo và chỉnh sửa hình ảnh SDI.

## Định dạng tệp SDI
Định dạng tệp SDI được sử dụng rộng rãi để cho phép sử dụng đĩa ảo để khởi động hệ thống. Một số phiên bản của Microsoft Windows cho phép **Khởi động RAM**, điều quan trọng là tải tệp SDI vào bộ nhớ rồi khởi động từ tệp đó. Định dạng tệp SDI cũng tự cho phép khởi động mạng bằng cách sử dụng PXE (Môi trường thực thi khởi động trước). Nó cũng đang được sử dụng để chụp ảnh đĩa cứng.
### Phần tệp SDI
Bản thân tệp SDI có thể được chia thành các phần sau:
- **Boot BLOB**: Phần này chứa chương trình khởi động thực tế, STARTROM.COM. Điều này tương tự như khu vực khởi động của đĩa cứng.
- **Tải BLOB**: Phần này thường chứa NTLDR và được khởi chạy bởi BLOB khởi động.
- **Phần BLOB**: Phần này chứa thời gian chạy khởi động thực tế; cũng bao gồm các tệp boot.ini và ntdetect.com nên được đặt trong thư mục gốc của thời gian chạy.
- **Disk BLOB**: Đây là hình ảnh ổ cứng phẳng bắt đầu bằng MBR. Nó được sử dụng để chụp ảnh ổ cứng thay vì khởi động. Ngoài ra, chỉ Disk BLOB mới có thể được gắn với các tiện ích của Microsoft.


## Người giới thiệu

* [Hình ảnh triển khai hệ thống - theo Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


