{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp NPK",
  "description":"Tìm hiểu về định dạng tệp NPK và API có thể tạo và mở tệp NPK.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Tệp NPK là gì?

Tệp NPK là tệp gói nâng cấp phần mềm được các bộ định tuyến **MikroTik** sử dụng để nâng cấp hệ điều hành của bộ định tuyến. Nó xuất hiện dưới dạng kho lưu trữ nhị phân nén được tải vào bộ định tuyến để cài đặt các bản cập nhật phần mềm. Thông tin chứa bên trong tệp NPK bao gồm thông tin mạng như địa chỉ IP và dịch vụ IP, thông tin trình kết nối (giao diện ethernet và cổng nối tiếp), thiết lập email, cấu hình cầu nối và quản lý người dùng cục bộ.

## Định dạng tệp NPK

Các tệp NPK được lưu trữ dưới dạng kho lưu trữ nhị phân nén. Đây là định dạng tệp đóng chỉ được sử dụng bởi chính MikroTik. Nó không nhằm mục đích tạo các tiện ích bổ sung cho RouterOS thông qua bên thứ 3. Các tệp NPK do chính MikroTik duy trì và bạn có thể tải xuống các phiên bản nâng cấp của tệp này từ phần tải xuống của trang web [MikroTik](https://mikrotik.com/download).

Khi tệp NPK được tải lên bộ định tuyến, hệ điều hành bộ định tuyến sẽ không có hiệu lực trừ khi nó được khởi động lại. Do đó, cần phải khởi động lại để hệ điều hành bộ định tuyến được nâng cấp.

## Người giới thiệu

* [MikroTik - Nâng cấp hệ điều hành bộ định tuyến](https://mikrotik.com/download)
* [Cách tạo tệp NPK](https://forum.mikrotik.com/viewtopic.php?t=87126)

