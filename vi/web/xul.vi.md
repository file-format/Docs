{
  "date" : "2021-05-24",
  "keywords" :["xul", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "Ngôn ngữ giao diện người dùng XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - Tệp ngôn ngữ giao diện người dùng XML",
  "description":"Tìm hiểu về định dạng tệp XUL và các API có thể tạo và mở tệp XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Tệp XUL là gì?

Tệp có phần mở rộng .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) là viết tắt của Ngôn ngữ giao diện người dùng XML) là tệp ngôn ngữ đánh dấu dựa trên [XML](/vi/web/xml/) dành cho tạo giao diện người dùng. Nó được Mozilla phát triển dành cho các nhà phát triển để tạo các thành phần giao diện người dùng đồ họa tương tự như các ngôn ngữ đánh dấu khác được sử dụng để tạo các trang web. XUL đã được Mozilla sử dụng rộng rãi trong trình duyệt Firefox của mình, nơi nó sử dụng cơ sở mã Mozilla. Kết xuất XUL được thực hiện bằng cách sử dụng
[Công cụ tắc kè](https://en.wikipedia.org/wiki/Gecko_(software)). Các nhánh của Firefox như Pale Moon, Basilisk và Waterfox vẫn hỗ trợ các tiện ích bổ sung XUL. Các tệp XUL được xác định bằng loại MIME: application/vnd.mozilla.xul+xml.

## Định dạng tệp XUL

Các tệp XUL được viết bằng văn bản thuần túy dựa trên định dạng tệp XML và được hiển thị bằng công cụ Gecko. Ba phần chính của cấu trúc XUL là:

* `Nội dung` - Điều này bao gồm các khai báo của cửa sổ và các phần tử giao diện người dùng có trong chúng.
* `Skin` - Nó bao gồm mọi biểu định kiểu, hình ảnh và các tệp liên quan đến chủ đề khác. Sự xuất hiện của một cửa sổ được mô tả trong biểu định kiểu.
* `Locale` - Văn bản hiển thị trong một cửa sổ được lưu trữ riêng biệt và người dùng có thể sử dụng nhiều bộ tệp ngôn ngữ.

### Ví dụ XUL

Ví dụ sau tạo ba nút được xếp chồng lên nhau theo hướng dọc.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Người giới thiệu

* [XUL - Theo Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [Tài liệu lưu trữ XUL - Bởi Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

