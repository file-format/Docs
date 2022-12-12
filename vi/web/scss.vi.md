---
date: 2019-10-11
keywords: scss, .scss, định dạng tệp scss, cách mở tệp scss, biểu định kiểu cú pháp tuyệt vời, bộ tiền xử lý css, sass
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp SCSS - Sass Cascading Style Sheet
linktitle: SCSS
description: "Tìm hiểu về định dạng tệp SCSS và các API có thể tạo và mở tệp SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Tệp SCSS là gì? ##

SCSS là cú pháp thứ hai của Sass (Syntactally Awesome Stylesheet) sử dụng dấu ngoặc thay vì thụt đầu dòng. SCSS được thiết kế sao cho tệp CSS3 hợp lệ cũng là tệp SCSS hợp lệ. Các tệp SCSS được lưu trữ với phần mở rộng .scss.

## Tại sao nên sử dụng SCSS ##

Vì thiết kế của các trang web đang trở nên phức tạp dẫn đến các tệp [CSS](/vi/web/css/) lớn. Các tệp như vậy khó bảo trì hơn. Đây là lúc SCSS xuất hiện. SCSS giới thiệu các biến, lồng, trộn, nhập và kế thừa bộ chọn trong quá trình phát triển CSS. Những bổ sung này giúp làm việc với thiết kế thú vị hơn rất nhiều.

## Cách sử dụng tệp SCSS ##

Các tệp SCSS không được bao gồm trực tiếp trong tài liệu [HTML](/vi/web/html/) như CSS. Thay vào đó, các tệp SCSS được chuyển đổi thành tệp CSS được bao gồm trong tệp HTML. Để cài đặt SCSS trên hệ thống của bạn, hãy làm theo hướng dẫn trên [Trang web chính thức của Sass](https://sass-lang.com/install).
Để chuyển đổi SCSS sang CSS, bạn có thể chuyển đổi tệp SCSS đã lưu hoặc theo dõi các thay đổi và chuyển đổi khi tệp được lưu. Các lệnh cho cả hai được đưa ra dưới đây.

### Chuyển đổi một lần ###

Tham số đầu tiên là tệp SCSS nguồn và tham số thứ hai là tệp CSS đầu ra.

```cmd
sass main.scss main.css
```

### Theo dõi các thay đổi ###

Lệnh này có một cờ *watch** bổ sung để giữ cho lệnh chạy và ngay sau khi tệp SCSS được lưu, CSS đầu ra sẽ được tạo.

```cmd
sass --watch main.scss main.css
```

## Cú pháp SCSS ##

SCSS hỗ trợ các biến, lồng, trộn, nhập, kế thừa bộ chọn, v.v. Dưới đây là ví dụ về các tính năng này.

### Biến ###

Bằng cách sử dụng các biến, bạn có thể đặt thông tin có thể sử dụng lại, chẳng hạn như màu chính hoặc màu nền cho nút lưu. Điều này rất hữu ích nếu bạn cần thay đổi thông tin đó, bạn chỉ cần thay đổi thông tin đó tại một vị trí và nó sẽ cập nhật ở bất kỳ nơi nào nó được sử dụng.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS đã tạo**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Làm tổ ###

Bạn có thể lồng các bộ chọn CSS tương tự như cấu trúc phân cấp của HTML. Trong ví dụ dưới đây, span được lồng bên trong khối h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS đã tạo**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Hỗn hợp ###

Mixin có thể được sử dụng để nhóm các thuộc tính tương tự lại với nhau được sử dụng cùng nhau ở nhiều nơi. Bạn cũng có thể truyền tham số cho mixin.

**SCSS**

** Khai báo một mixin **

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Sử dụng mixin**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**CSS đã tạo**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Gia hạn ###

Mở rộng/Kế thừa rất hữu ích trong trường hợp các thuộc tính của một bộ chọn cần được chia sẻ với một bộ chọn khác. Trong ví dụ dưới đây, bộ chọn *.error-notice* lấy tất cả các thuộc tính của bộ chọn *.error-text* và thêm các thuộc tính đường viền và phần đệm.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**CSS đã tạo**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Nhập khẩu ###

Nhập khẩu có thể hữu ích trong việc tách các mối quan tâm. Bạn có thể chia các kiểu theo cách sao cho các kiểu đầu trang nằm trong một tệp riêng, các kiểu chân trang nằm trong một tệp riêng, tất cả các biến màu được sử dụng trong các kiểu có thể nằm trong một tệp riêng, v.v. Sử dụng kỹ thuật này, phong cách luôn có tổ chức. Bạn chỉ cần nhập các tệp trong tệp SCSS chính của mình như trong ví dụ bên dưới. Bạn không cần chỉ định phần mở rộng tệp trong hướng dẫn nhập. Sass biên dịch trực tiếp tất cả các tệp SCSS. Để tránh các tệp nhập được biên dịch trực tiếp, bạn có thể biến chúng thành các phần bằng cách thêm dấu gạch dưới (_) trước tên của chúng. Bạn có thể nhập các phần tương tự như các tệp SCSS bình thường mà không có dấu gạch dưới.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

CSS đầu ra sẽ có các kiểu từ tất cả các tệp đã nhập.

## Người giới thiệu ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

