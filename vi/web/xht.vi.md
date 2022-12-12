{
  "date" : "2021-05-24",
  "keywords" :["xht", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "ngôn ngữ đánh dấu siêu văn bản mở rộng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHT",
  "description":"Tìm hiểu về định dạng tệp XHT và các API có thể tạo và mở tệp XHT.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Tệp XHT là gì?

Tệp có phần mở rộng .xht là tệp web được liên kết với loại tệp [XHTML](/vi/web/xhtml/) (Ngôn ngữ đánh dấu siêu văn bản mở rộng), bản thân tệp này là tệp đánh dấu dựa trên [XML](/vi/web/xml/). Cả hai tệp này đều tương tự như HTML nhưng có cú pháp giống XML chặt chẽ hơn. Các tệp XHT được thiết kế theo cách có cấu trúc hơn, liên quan đến ít tập lệnh hơn và chung chung ngoài việc sử dụng các phương tiện XML hiện có.

## Định dạng tệp XHT

Tệp XHT được tạo và lưu trữ dưới dạng tệp văn bản thuần túy với mã hóa UTF-8 theo mặc định. Nó chứa mã nguồn hoàn chỉnh của tài liệu XHTML có thể được mở và chỉnh sửa bằng bất kỳ trình soạn thảo văn bản nào hỗ trợ mã hóa Unicode. Ngoài các trình soạn thảo văn bản, hầu hết các trình duyệt web hiện đại đều có thể hiểu được định dạng tệp XHT và có thể mở bằng các trình duyệt này.

## Ví dụ XHT

Ví dụ sau đây về tài liệu XHT định nghĩa các khai báo XML.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## Người giới thiệu ##

* [Lịch sử XHTML: Từ những năm 1990 đến nay](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

