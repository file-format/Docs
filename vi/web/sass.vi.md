---
date: 2019-10-11
keywords: sass, .sass, định dạng tệp sass, cách mở tệp sass, biểu định kiểu cú pháp tuyệt vời, bộ tiền xử lý css, sass
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp Sass
linktitle: Sass
description: "Tìm hiểu về định dạng tệp Sass và các API có thể tạo và mở tệp Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Tệp SASS là gì? ##

Sass (các biểu định kiểu tuyệt vời về mặt cú pháp) là một ngôn ngữ kịch bản tiền xử lý. Nó được biên dịch thành [CSS](/vi/web/css/) và được lưu trữ với phần mở rộng .sass. Sass bao gồm hai cú pháp, cú pháp ban đầu dựa trên các vết lõm sử dụng phần mở rộng .sass và SCSS mới hơn với định dạng khối như CSS sử dụng phần mở rộng .scss.

## Tại sao nên sử dụng Sass ##

Sass thực sự hữu ích trong việc duy trì các kiểu vì nó cung cấp nhiều tính năng như giới thiệu các biến, lồng, trộn, nhập và kế thừa bộ chọn giúp làm việc với các kiểu thú vị.

## Cách sử dụng tệp SASS ##

Các tệp SASS không được bao gồm trực tiếp trong tài liệu [HTML](/vi/web/html/) mà được chuyển đổi thành các tệp CSS được bao gồm trong các tệp HTML. Bạn có thể cài đặt Sass cho hệ thống của mình bằng cách làm theo hướng dẫn trên [Trang web chính thức của Sass](https://sass-lang.com/install).

Sass có thể được chuyển đổi thành CSS bằng cách chuyển đổi tệp SASS đã lưu hoặc bằng cách theo dõi các thay đổi và chuyển đổi khi tệp được lưu. Các lệnh cho cả hai được đưa ra dưới đây.

### Chuyển đổi một lần ###

Tham số đầu tiên của lệnh là tệp SASS nguồn và tham số thứ hai là tệp CSS đầu ra.

```cmd
sass main.sass main.css
```

### Theo dõi các thay đổi ###

Có thể chạy lệnh trên với một cờ *watch* bổ sung để giữ cho lệnh chạy và ngay sau khi tệp Sass được lưu, CSS đầu ra sẽ được tạo.

```cmd
sass --watch main.sass main.css
```

## Cú pháp Sass ##

Sass hỗ trợ các biến, lồng, trộn, nhập, kế thừa bộ chọn, v.v. Dưới đây là ví dụ về các tính năng này.

### Biến ###

Các biến có thể được sử dụng để đặt thông tin có thể sử dụng lại, chẳng hạn như màu chính hoặc phần đệm cho một nút. Điều này có thể hữu ích nếu trong tương lai bạn cần thay đổi thông tin đó, bạn chỉ cần thay đổi thông tin đó tại một vị trí và nó sẽ cập nhật ở mọi nơi.

**Ngổ ngáo**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

Bộ chọn CSS có thể được lồng vào nhau tương tự như cấu trúc phân cấp của HTML. Trong ví dụ sau, span được lồng bên trong khối h1.

**Ngổ ngáo**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

Mixin được sử dụng để nhóm các thuộc tính tương tự lại với nhau được sử dụng ở nhiều nơi. Mixins cũng hỗ trợ các tham số.

**Ngổ ngáo**

** Khai báo một mixin **

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Sử dụng mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Mở rộng/Kế thừa có thể tỏ ra hữu ích trong trường hợp các thuộc tính của một bộ chọn cần được chia sẻ với một bộ chọn khác. Trong ví dụ bên dưới, bộ chọn *.error-notice* lấy tất cả các thuộc tính của bộ chọn *.error-text* và thêm các thuộc tính đường viền và phần đệm.

**Ngổ ngáo**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

Việc nhập có thể hữu ích nếu bạn cấu trúc các kiểu của mình thành các tệp khác nhau dựa trên chức năng hoặc bất kỳ cấu trúc nào khác mà bạn tuân theo. Bạn có thể nhập tất cả các tệp này vào một tệp SASS chính mà sau này được chuyển đổi thành CSS. Trong khi nhập, bạn không cần chỉ định phần mở rộng tệp trong hướng dẫn nhập. Sass biên dịch trực tiếp tất cả các tệp SASS. Để tránh các tệp nhập được biên dịch trực tiếp, bạn có thể biến chúng thành các phần bằng cách thêm dấu gạch dưới (_) ở đầu tên của chúng. Các phần được nhập tương tự như các tệp Sass bình thường.

**Ngổ ngáo**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

CSS đầu ra sẽ có các kiểu từ tất cả các tệp đã nhập.

## Người giới thiệu ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

