{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp APPCACHE - Định dạng tệp kê khai bộ đệm HTML5",
  "description" :"Tìm hiểu về tệp APPCACHE là gì và các API có thể tạo và mở tệp APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Tệp APPCACHE là gì?

Tệp APPCACHE là một tệp văn bản chứa danh sách các tài nguyên được trình duyệt lưu vào bộ đệm để truy cập ngoại tuyến vào các ứng dụng web. Điều này rất hữu ích khi không có kết nối internet. Trong tình huống như vậy, trình duyệt sử dụng tài nguyên bộ đệm ngoại tuyến để cung cấp quyền truy cập vào nội dung web. Tệp APPCACHE chứa các tài nguyên web như hình ảnh (ví dụ: **[PNG](/vi/image/png/)**, **[WEBP](/vi/image/webp/)**, v.v.), biểu định kiểu **([ CSS])(/vi/web/css/)** và các tệp script (chẳng hạn như các tệp Javascript **[JS](/vi/web/js/)**).

Các ứng dụng có thể **mở tệp APPCACHE** bao gồm các trình duyệt web như Google Chrome, Safari và Firefox.

## Định dạng tệp APPCACHE - Thông tin khác

Các tệp APPCACHE là các tệp văn bản đơn giản, cung cấp quyền truy cập ngoại tuyến vào các trang web để chạy mà không cần kết nối internet. Sự hiện diện của APPCACHE chỉ định một trang là khả dụng ngoại tuyến.

### Cách tham chiếu tệp APPCACHE?

Trong trang HTML của bạn, tệp APPCACHE được tham chiếu như sau.

```
<html manifest="example.appcache">
  ...
</html>
```

## Cấu trúc của tệp kê khai APPCACHE

Tệp kê khai APPCACHE đơn giản trông như sau.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Đây là một ví dụ đơn giản nhất và cũng có thể có những cấu trúc phức tạp hơn.

## Ưu điểm của Bản kê khai APPCACHE

Việc sử dụng giao diện bộ đệm mang lại cho các ứng dụng web những lợi thế sau.

1. Duyệt ngoại tuyến - Giao diện bộ đệm cho phép người dùng cuối duyệt toàn bộ trang web của bạn khi họ ngoại tuyến
1. Tốc độ - bộ đệm cho phép truy cập tốc độ cao vào nội dung ngoại tuyến trực tiếp từ đĩa
1. Khả năng truy cập mọi lúc - Trong trường hợp trang web của bạn gặp sự cố, người dùng vẫn có quyền truy cập vào nội dung trang web và có thể có được trải nghiệm ngoại tuyến

## Người giới thiệu

* [Hướng dẫn cho người mới bắt đầu về Tệp kê khai AppCache](https://web.dev/appcache-beginner/)

