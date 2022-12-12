---
date: 2019-10-11
keywords: js, .js, định dạng file js, cách mở file js, file javascript
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp JS
linktitle: JS
description: "Tìm hiểu về định dạng tệp JS và các API có thể tạo và mở tệp JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Tệp JS là gì? ##

JS (JavaScript) là các tệp chứa mã JavaScript để thực thi trên các trang web. Các tệp JavaScript được lưu trữ với phần mở rộng .js. Bên trong tài liệu [HTML](/vi/web/html/), bạn có thể nhúng mã JavaScript bằng cách sử dụng \ <script>\</script> thẻ hoặc bao gồm tệp JS. Tương tự như tệp [CSS](/vi/web/css/), tệp JS có thể được đưa vào nhiều tài liệu HTML để có thể sử dụng lại mã. JavaScript có thể được sử dụng để thao tác HTML DOM.

## Lược Sử ##

JavaScript lần đầu tiên được vận chuyển như một phần của Trình duyệt Điều hướng vào tháng 9 năm 1995 với tên LiveScript của Netscape. Nó được đổi tên thành JavaScript ba tháng sau đó. Năm 1996, trình thông dịch của Bộ điều hướng được thiết kế ngược của Microsoft để tạo ra JScript. JScript được phát hành cùng với Internet Explorer và rất khác so với JavaScript.

Netscape đã gửi JavaScript tới ECMA International dẫn đến việc phát hành chính thức đặc tả ECMAScript đầu tiên vào năm 1997. ECMAScript 2 được phát hành vào năm 1998, ECMAScript 3 vào năm 1999 và công việc trên ECMAScript 4 bắt đầu vào năm 2000 nhưng chưa bao giờ đạt được kết quả.

Jesse James Garrett vào năm 2005 đã phát hành sách trắng trong đó ông đặt ra thuật ngữ *Ajax*. Điều này đã sử dụng JavaScript làm xương sống để tạo các ứng dụng web tải dữ liệu ở chế độ nền và tránh tải lại toàn bộ trang. Điều này dẫn đến việc tạo ra các thư viện như JQuery, Prototype, Dojo, v.v.

Google đã phát hành trình duyệt Chrome với công cụ JavaScript V8 vào năm 2008. Đầu năm 2009, một thỏa thuận đã được thực hiện để kết hợp tất cả các công việc có liên quan và thúc đẩy JavaScript phát triển. Điều này dẫn đến việc phát hành Tiêu chuẩn ECMAScript 5 vào tháng 12 năm 2009.

## Cách sử dụng tệp JS ##

Để sử dụng tệp JS, bạn đưa nó vào tài liệu HTML. Bạn sử dụng thẻ link để gộp file như hình bên dưới.

```html
<script src="site.js"></script>
```

Thuộc tính *src* của thẻ *script* chứa đường dẫn đến tệp JS. Bằng cách này, chức năng JS được thêm vào tài liệu HTML.

## Cú pháp JS ##

Các tệp JavaScript có thể chứa các biến, toán tử, hàm, điều kiện, vòng lặp, mảng, đối tượng, v.v. Dưới đây là tổng quan ngắn gọn về cú pháp của JavaScript.

- Mỗi câu lệnh kết thúc bằng dấu chấm phẩy (;).
- Sử dụng từ khóa *var* để khai báo biến.
- Hỗ trợ các toán tử số học ( + - * / ) để tính giá trị.
- Chú thích một dòng được thêm vào // và chú thích nhiều dòng được bao quanh bởi /* và */.
- Tất cả các mã định danh đều phân biệt chữ hoa chữ thường, tức là *modelNo* và *modelno* là hai biến khác nhau.
- Các chức năng được xác định bằng cách sử dụng từ khóa *function*.
- Mảng có thể được định nghĩa bằng dấu ngoặc vuông [].
- JS hỗ trợ các toán tử so sánh như ==, != , >=, !==, v.v.
- Các lớp có thể được định nghĩa bằng cách sử dụng từ khóa *class*.

## Ví dụ sử dụng JS ##

Phần sau đây trình bày một tệp JavaScript ví dụ sử dụng đơn giản.

### Tài liệu HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Mã JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Người giới thiệu ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

