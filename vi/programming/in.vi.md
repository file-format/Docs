{
  "date" : "2022-04-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp IN - Tệp đầu vào Autoconf",
  "description":"Tìm hiểu về định dạng tệp IN và các API có thể tạo và mở tệp IN.",
  "linktitle" : "IN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-26"
}

## Tệp IN là gì?

Tệp IN là tệp đầu vào mà GNU Autoconf sử dụng khi xây dựng ứng dụng. Khi quá trình cấu hình được chạy, tập lệnh Autoconf (tệp .AC) có thể tham chiếu đến một hoặc nhiều tệp ".in" hoặc ".h.in". Tệp IN xác định các biến được tham chiếu trong quá trình cài đặt chương trình, chẳng hạn như số phiên bản và ngày phát hành của ứng dụng. Các tệp IN cũng có thể được sử dụng để xác định sự hiện diện hay vắng mặt của các tính năng trong một bản cài đặt cụ thể. Có thể sử dụng các ứng dụng như Notepad và Notepad++ để mở và chỉnh sửa tệp IN.

## Định dạng tệp IN - Thông tin khác

Autoconf là một thành phần của hệ thống xây dựng GNU tạo ra các bản dựng ứng dụng tùy chỉnh cho các nền tảng khác nhau. Đây là một trong một số công cụ xây dựng GNU. Các công cụ khác bao gồm Automake, Gnulib và Libtool. Không cần sự can thiệp thủ công của người dùng, các tập lệnh này có thể điều chỉnh các gói cho nhiều loại hệ thống giống như UNIX. Autoconf tạo tập lệnh cấu hình gói từ tệp mẫu liệt kê các tính năng của hệ điều hành mà gói có thể sử dụng dưới dạng lệnh gọi macro M4

## Người giới thiệu

* [Autoconf](https://www.gnu.org/software/autoconf/)

