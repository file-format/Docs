---
date: 2021-07-05
keywords: ssp, .ssp, định dạng file ssp, cách mở file ssp, Scala Server Page
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Định dạng tệp trang máy chủ Scala
linktitle: SSP
description: "Tìm hiểu về định dạng tệp SSP là gì và các API có thể tạo và mở tệp SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Tệp SSP là gì?

Một tệp có phần mở rộng .ssp là trang web được tạo bằng mã Scala cho các biểu thức thay vì chỉ HTML đơn giản. Nó hoạt động như một tập lệnh phía máy chủ bằng cách sử dụng kết hợp HTML và Scala. Các tệp này nằm trên máy chủ và được sử dụng để tạo các trang web tĩnh phục vụ cho người dùng. Bản thân Scala là ngôn ngữ lập trình đa năng có cú pháp quen thuộc với những người dùng đã làm việc với Velocity, JSP hoặc Erb. Các tệp SSP có thể được phân tích và đánh giá bằng cách sử dụng [Scalate](https://scalate.github.io/scalate/), một công cụ mẫu dựa trên Scala để tạo văn bản và đánh dấu.

## Định dạng tệp SSP - Thông tin khác

Các tệp SSP được lưu trong tệp văn bản thuần túy và có thể được đánh giá bằng cách sử dụng Scalate. Mẫu Ssp bao gồm văn bản thuần túy thường là tài liệu HTML. Nó có các thẻ Ssp được nhúng trong nó khiến các công cụ kết xuất hiển thị các phần khác nhau của tài liệu một cách linh hoạt. Các thẻ bắt đầu và kết thúc bằng chuỗi <% ... %> và ${ ... } và bất kỳ thứ gì ngoài các chuỗi này đều được coi là văn bản theo nghĩa đen.

### Ví dụ SSP

Ví dụ sau đây hiển thị mã SSP và đầu ra của nó khi nó được kết xuất bởi công cụ kết xuất.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Đầu ra như sau.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Người giới thiệu

- [Tham khảo SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

