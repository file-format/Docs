{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp RST- Tệp văn bản được cấu trúc lại",
  "description":"Tìm hiểu về định dạng tệp RST và các API có thể tạo và mở tệp RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Tệp RST là gì?

Tệp RST là định dạng tệp tài liệu kỹ thuật, được sử dụng chủ yếu trong cộng đồng lập trình Python. Nó là một tệp văn bản được viết bằng ngôn ngữ đánh dấu reStructuredText áp dụng các kiểu và định dạng cho các tài liệu văn bản thuần túy để tạo tài liệu. Các tệp RST sử dụng nhận xét và thông tin khác trong mã chương trình Python để tạo tài liệu kỹ thuật của ứng dụng. Tuy nhiên, chúng cũng có thể chứa văn bản có thể được chuyển đổi thành các trang web đơn giản và [Sách điện tử](/vi/ebook/). Có thể sử dụng các trình soạn thảo văn bản như Github Atom, GNU Emacs (đa nền tảng), Microsoft Notepad (Windows), Apple TextEdit (Mac) và Vim (Linux) để mở tệp RST.

## Định dạng tệp RST

Các tệp RST chứa mã được viết bằng ngôn ngữ đánh dấu reStructuredText. Nó là một phần của dự án Docutils của Python Doc-SIG (Documentation Special Interest Group) cung cấp một bộ công cụ cho Python tương tự như Javadoc cho Java. Trình phân tích cú pháp cho định dạng tệp RST được nhúng trong Tài liệu và có thể trích xuất thông tin từ các chương trình Python để định dạng chúng thành tài liệu chương trình.

### văn bản tái cấu trúc Ví dụ RST

Hãy lấy một văn bản ví dụ được viết ở định dạng tệp RST như sau.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Khi văn bản này được nhập vào bộ xử lý rST chẳng hạn như Docutils, đầu ra sẽ như sau.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Tài liệu tham khảo ##

* [reStructuredText - theo Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

