{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Nén", "Tệp", "Phần mở rộng", "Định dạng tệp", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp LZH",
  "description":"Tìm hiểu về định dạng tệp LZH và API có thể tạo và mở tệp LZH.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Tệp LZH là gì? ##

Một tệp có phần mở rộng .lzh và .lha thường liên quan đến định dạng tệp nén lưu trữ. Định dạng tệp này giống với các định dạng nén tệp khác như [ZIP](/vi/compression/zip/), [RAR](/vi/compression/rar/), v.v. Mục đích chính của các định dạng tệp này là giảm kích thước của tệp. định dạng để dễ dàng gửi cũng như giữ chúng lại với nhau ở dạng nén. AS so với các công ty phương Tây khác Các tệp LZH rất phổ biến ở Nhật Bản và thường được sử dụng để nén dữ liệu trò chơi điện tử. Tiện ích bổ sung LZH dành cho Windows 7 được tích hợp sẵn trong phiên bản Windows 7 tiếng Nhật. Lần đầu tiên Microsoft phát hành Tiện ích bổ trợ Thư mục Microsoft Nén (LZH) cho phiên bản Windows XP tiếng Nhật. Định dạng tệp này được triển khai với các điều khoản và tính năng nén được sử dụng bởi thuật toán Lempel-Ziv và Haruyasu

## Đặc điểm kỹ thuật LZH ##

Phương pháp nén của kho lưu trữ LZH được hiển thị dưới dạng chuỗi văn bản năm byte, chẳng hạn như -lz1-. Đây là các byte thứ ba đến thứ bảy trong tệp nén.

|Thông số kỹ thuật|Mô tả|
---|---|
|Tiện ích mở rộng | .lzh, .lha|
|Loại phương tiện| ứng dụng/x-lzh-nén|
|Mã Loại| "LHA_" (LHA-SPACE)|
|UTI| công khai.archive.lha|
|Được phát triển bởi| Haruyasu Yoshizaki (Yoshi)|
|Loại| Nén|
|Mở rộng từ| LArc|

## Sự cố khi mở tệp LZH ##

Sau đây là một số vấn đề có thể khiến định dạng tệp LZH hoạt động kém:
  

* Tập tin có thể bị hỏng. Để giải quyết vấn đề này, hãy tải xuống lại tệp hoặc yêu cầu người gửi gửi lại tệp
* Nguyên nhân thứ 2 là file bị nhiễm virus trường hợp này scan file đúng cách
* Liên kết không chính xác đến tệp LZH
* Xóa mô tả của LZH
* Không đủ tài nguyên phần cứng
* Trình điều khiển lỗi thời của thiết bị

## Người giới thiệu ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
