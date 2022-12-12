---
date: 2022-05-09
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Định dạng tệp PYM - Tệp tiền xử lý vĩ mô PYM
linktitle: PYM
description: "Tìm hiểu về định dạng tệp PYM và các API có thể tạo và mở tệp PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Tệp PYM là gì?

Tệp PYM là tệp tiền xử lý macro dựa trên ngôn ngữ lập trình Python. Nó được phát triển bởi VRVis Research và lưu trữ các phím tắt macro. Khi tệp PYM được diễn giải bởi giai đoạn tiền xử lý của trình thông dịch Python, các phím tắt này được mở rộng để thay thế cho toàn văn của chúng. Ngoài ra, thao tác tùy chọn thứ ba có thể được thực hiện bởi bộ tiền xử lý macro là bao gồm tệp. Các tệp PYM có thể được mở trong các trình soạn thảo văn bản như Notepad, Notepad ++, Apple TextEdit và VI trên Linux.

## Định dạng tệp PYM

Các tệp PYM được lưu dưới dạng tệp văn bản thuần túy vào đĩa. Tệp PYM cũng có thể bao gồm các tệp khác bằng cách sử dụng chỉ thị `#include`.

### Cú pháp PYM

Các câu lệnh PYM được bao gồm giữa các dấu ""#begin python và "#end python" như được hiển thị bên dưới.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Mở rộng vĩ mô PYM

Việc mở rộng macro PYM được biểu thị bằng hai chuỗi nghĩa là <[ và ]>. Đây là những thẻ html đặc biệt và có thể xuất hiện ở bất kỳ đâu trong một dòng. Một ví dụ nhỏ về PYM như sau.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

Đầu ra của việc chạy này thông qua PYM như sau:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Người giới thiệu ##

* [PYM - Bộ tiền xử lý vĩ mô dựa trên Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Thông dịch viên PYM](https://github.com/interpreters/pym)

