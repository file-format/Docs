{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp KIT và các API có thể tạo và mở tệp KIT.",
  "title" :"Định dạng tệp KIT - Tệp CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Tệp KIT là gì?

Tệp có phần mở rộng .kit là tệp HTML được tạo bằng ứng dụng ngôn ngữ lập trình [CodeKit](https://codekitapp.com/). Nó chứa `nhập` và `biến` ngoài các tệp [HTML](/vi/web/html/) hiện có, làm cho nó trở nên lý tưởng cho các trang web tĩnh. CodeKit biên dịch các tệp KIT thành HTML có thể dễ dàng sử dụng làm tệp trang web tĩnh.

## Định dạng tệp KIT

Các tệp KIT là các tệp HTML bao gồm thêm các mục nhập và biến. Chúng được lưu trữ dưới dạng tệp văn bản thuần túy và có thể được mở bằng bất kỳ trình soạn thảo văn bản hoặc trình chỉnh sửa tệp web nào.

### Nhập tệp KIT

Hầu hết mọi loại tệp đều có thể được nhập vào tệp Kit. Sau đây là cú pháp nhập được sử dụng để nhập tệp vào tệp .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Khi một mục nhập được thêm vào tệp KIT và được lưu, nó sẽ được thay thế bằng văn bản của tệp được nhập. Bạn cũng có thể sử dụng @include thay vì @import.

### Nhập nhiều lần trong một tệp KIT

Bạn cũng có thể nhập nhiều tệp cùng lúc bằng cách sử dụng danh sách được phân tách bằng dấu phẩy:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Người giới thiệu

* [Kit là gì?](https://codekitapp.com/help/kit/)

