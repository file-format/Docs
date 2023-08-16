---
date: 2019-10-11
keywords: css, .css, định dạng file css, cách mở file css, cascading style sheet
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp CSS
linktitle: CSS
description: "Tìm hiểu về định dạng tệp CSS và các API có thể tạo và mở tệp CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Tệp CSS là gì? ##

CSS (Cascading Style Sheets) là các tệp mô tả cách các phần tử HTML được hiển thị trên màn hình, giấy, v.v. Với HTML, bạn có thể có các kiểu được nhúng hoặc các kiểu có thể được xác định trong biểu định kiểu bên ngoài. Để nhúng các kiểu, \ <style>\</style> thẻ được sử dụng. Các biểu định kiểu bên ngoài được lưu trữ trong các tệp có phần mở rộng .css. Với CSS bên ngoài, bạn có thể đưa nó vào nhiều trang HTML để cập nhật kiểu của các trang đó. Ngay cả một tệp CSS duy nhất cũng có thể được sử dụng để tạo kiểu cho một trang web hoàn chỉnh.

## Lược Sử ##

CSS1 được phát hành vào năm 1996 với Bert Bos là đồng tác giả. Nhóm làm việc CSS đã bắt đầu giải quyết các vấn đề chưa được giải quyết trong CSS1. Điều này dẫn đến việc tạo ra CSS2 vào tháng 11 năm 1997, được xuất bản dưới dạng đề xuất của W3C vào ngày 12 tháng 5 năm 1998. Phiên bản này đã thêm hỗ trợ cho các thiết bị dành riêng cho phương tiện như máy in, phông chữ có thể tải xuống, bảng và định vị thành phần. Tháng 6 năm 1999, CSS3 trở thành đề xuất của W3C. Điều này chia tài liệu thành các mô-đun trong đó mỗi mô-đun có các tính năng mở rộng được xác định trong CSS2.

## Cách sử dụng tệp CSS ##

Để sử dụng tệp CSS, bạn đưa nó vào phần đầu của tài liệu HTML. Bạn sử dụng thẻ link để gộp file như hình bên dưới.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

thuộc tính *href* của thẻ liên kết chứa đường dẫn đến tệp CSS. Bằng cách này, các kiểu áp dụng có trong tệp CSS đi kèm sẽ được áp dụng cho tài liệu HTML.

## Cú pháp CSS ##

Một quy tắc CSS bao gồm hai thành phần, bộ chọn và phần khai báo. Bộ chọn trỏ đến một phần tử trong tài liệu HTML. Nó có thể là thẻ thành phần, tên lớp, tên id, nhiều thẻ hiển thị phân cấp, v.v. Một khai báo chứa định nghĩa kiểu bao gồm thuộc tính và giá trị. Thuộc tính xác định thuộc tính của phần tử mà bạn muốn thay đổi và giá trị xác định giá trị mới của nó. Mỗi quy tắc CSS có thể có nhiều khai báo. Sau đây là một ví dụ về quy tắc CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Trong ví dụ trên, chúng ta có **h1** làm bộ chọn để chọn tất cả các thẻ h1 trong tài liệu HTML. Quy tắc có hai khai báo, một cho độ đậm của phông chữ và một cho màu sắc. *font-weight* và *color* là các thuộc tính và *700* và *forestgreen* lần lượt là các giá trị của chúng.

## Ví dụ sử dụng CSS ##

Phần sau đây trình bày tài liệu HTML mẫu và biểu định kiểu được sử dụng để tạo kiểu cho nó. Hình ảnh so sánh cũng được thêm vào để so sánh các tài liệu HTML được tạo kiểu và đơn giản

### Tài liệu HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Biểu định kiểu CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### So sánh đầu ra ###

Phía bên trái của hình ảnh hiển thị tài liệu HTML mà không áp dụng các kiểu và phía bên phải hiển thị tài liệu HTML với các kiểu được áp dụng.

{{< figure src="../CssExample.jpg" alt="hình ảnh ví dụ" >}}

## Người giới thiệu ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

