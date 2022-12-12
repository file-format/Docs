{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg file", "apkg file format", "apkg file type", "file", "type", "What is an APKG file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Định dạng tệp bộ bài Flashcard Anki",
  "description" :"Tìm hiểu về tệp APKG là gì và các API có thể tạo và mở chúng.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Tệp APKG là gì?

Tệp có phần mở rộng .apkg là một bộ thẻ ghi chú được tạo để sử dụng trong ứng dụng phần mềm [Anki](https://ankiweb.net/about), một chương trình học tập dựa trên thẻ ghi chú. Nó chứa văn bản [HTML](/vi/web/html/) được tải và hiển thị trong ứng dụng Anki, đồng thời có thể có thêm hình ảnh và âm thanh để học bằng hình ảnh và âm thanh. Anki cho phép người dùng tạo các sàn flashcard Anki của riêng họ cũng như nhập các sàn flashcard của người dùng khác.

## Định dạng tệp APKG

Bộ bài Anki được tạo từ các mẫu được viết bằng HTML, một ngôn ngữ nổi tiếng và phổ biến để tạo các trang web. Việc tạo kiểu cho các bộ bài được thực hiện bằng CSS, ngôn ngữ được sử dụng để tạo kiểu cho các trang web. Kiểu dáng bao gồm các sửa đổi đối với:

* font-family - Tên của phông chữ sẽ được sử dụng trên thẻ.
* cỡ chữ - Kích thước của phông chữ tính bằng pixel.
* căn chỉnh văn bản - Xác định xem văn bản sẽ được căn chỉnh ở giữa, bên trái hay bên phải.
* color - Xác định màu của văn bản có thể là các tên màu đơn giản như "xanh dương", "đỏ", v.v. hoặc mã màu HTML.
* background-color - Xác định màu nền của thẻ

Thông tin kiểu dáng được chia sẻ giữa tất cả các thẻ, ảnh hưởng đến tất cả các thẻ khi thay đổi được thực hiện. Ví dụ sau sẽ sử dụng nền màu vàng trên tất cả các thẻ ngoại trừ thẻ đầu tiên:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Việc thay đổi kích thước hình ảnh trong thẻ Anki có thể được kiểm soát như sau.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Nhúng Javascript vào thẻ Anki

Có thể nhúng [Javascript](/vi/web/js/) vào thẻ Anki bằng các mẫu thẻ. Tuy nhiên, do mức độ nâng cao của Javascript, hỗ trợ của nó không được cung cấp. Ngoài ra, các thiết bị kết xuất có thể hiển thị ảnh hưởng của việc triển khai Javascript trong thẻ theo cách khác nhau, dẫn đến nhu cầu kiểm tra việc triển khai trên tất cả các thiết bị. Một số tính năng Javascript như window.alert, gây khó khăn cho việc gỡ lỗi mã Javascript mà bạn đã viết.

## Người giới thiệu ##

* [Tài liệu Anki](https://docs.ankiweb.net/intro.html)

