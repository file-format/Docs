{
  "date" : "2019-10-11",
  "keywords" :[ "tệp mng", "định dạng tệp mng", "tệp mng là gì", "tệp", "ví dụ mng", "phần mở rộng tệp mng","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp MNG - Định dạng tệp đồ họa mạng nhiều hình ảnh",
  "description":"Tìm hiểu về định dạng tệp MNG và API có thể tạo và mở tệp MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp MNG là gì?

Tệp có phần mở rộng .mng là định dạng tệp Đồ họa mạng nhiều hình ảnh tương tự như định dạng hình ảnh [PNG](/vi/image/png/) nhưng hỗ trợ hình ảnh động. Nó được phát triển để tránh làm quá tải định dạng PNG với tính năng hoạt ảnh bổ sung. MNG cũng tương tự như tệp [GIF](/vi/image/gif/) nhưng nén nhiều hơn và hỗ trợ tính năng alpha đầy đủ. Loại phương tiện MIME không chính thức cho các tệp MNG là video/x-mng. Các tệp MNG có thể được mở trong các ứng dụng như ImageMagik và IrfanView.

## Định dạng tệp MNG

Định dạng tệp MNG tương tự như định dạng của PNG và sử dụng cùng một cấu trúc khối như được xác định trong thông số kỹ thuật của PNG. Bộ giải mã MNG phải có khả năng giải mã các luồng dữ liệu PNG mà không chỉ định bất kỳ cờ đặc biệt nào cho các lệnh giải mã. MNG nhóm nhiều hình ảnh lại với nhau thành một "khung", với một số hình ảnh được sử dụng làm sprite để di chuyển từ vị trí này sang vị trí khác. Cơ chế cho phép sử dụng lại dữ liệu hình ảnh mà không cần truyền lại. [Thông số kỹ thuật MNG](http://www.libpng.org/pub/mng/spec/) có thể được tham khảo để nhà phát triển tham khảo.

### Chữ ký MNG

Luồng dữ liệu MNG bắt đầu bằng chữ ký 8 byte chứa:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Điều này tương tự như chữ ký PNG nhưng chứa MNG thay vì PNG.

### Khung MNG

Một khung MNG bao gồm hình ảnh hai chiều của các hình ảnh nhỏ hơn. Mỗi hình ảnh nhỏ có thể được truy cập bằng cách sử dụng kết hợp chỉ mục hàng và cột. Định dạng này có khả năng lưu trữ dữ liệu "voxel" ba chiều được sắp xếp theo một loạt các mặt phẳng hai chiều. Mỗi mặt phẳng được đại diện bởi một luồng dữ liệu PNG hoặc Delta-PNG. Mỗi luồng dữ liệu Delta-PNG xác định một hình ảnh là sự khác biệt so với hình ảnh PNG gốc. Điều này cung cấp một cách thể hiện các hình ảnh tiếp theo nhỏ gọn hơn nhiều so với việc sử dụng một luồng dữ liệu PNG hoàn chỉnh cho mỗi hình ảnh.

## Người giới thiệu ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Định dạng MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

