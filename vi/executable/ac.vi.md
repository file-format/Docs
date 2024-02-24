{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Tìm hiểu về định dạng tệp AC và các API có thể tạo và mở tệp ACCDB.",
  "title" : "Định dạng tệp AC - Tệp tập lệnh Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-vi",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Một tập tin AC là gì?

Tệp AC là tệp tập lệnh Autoconf. **Autoconf** là gói macro M4 có thể mở rộng, tạo ra các tập lệnh shell để tự động định cấu hình các gói mã nguồn phần mềm. Các tập lệnh này có thể điều chỉnh các gói cho phù hợp với nhiều loại hệ thống giống UNIX mà không cần sự can thiệp thủ công của người dùng. Autoconf tạo tập lệnh cấu hình cho gói từ tệp mẫu liệt kê các tính năng của hệ điều hành mà gói có thể sử dụng, dưới dạng lệnh gọi macro M4.

Producing configuration scripts using Autoconf requires GNU M4. Bạn nên cài đặt GNU M4 (ít nhất là phiên bản 1.4.6, mặc dù khuyến nghị là 1.4.13 hoặc mới hơn) trước khi định cấu hình Autoconf, để tập lệnh cấu hình của Autoconf có thể tìm thấy nó. Các tập lệnh cấu hình do Autoconf tạo ra là độc lập nên người dùng không cần phải có Autoconf (hoặc GNU M4).

## Làm cách nào để mở tập tin AC?

AC là viết tắt của Cấu hình tự động. Đó là một tập lệnh được tạo bởi GNU Autoconf cho phép mã nguồn phần mềm được điều chỉnh phù hợp với các hệ thống giống Posix khác nhau bằng cách kiểm tra các tính năng cần thiết trong gói. Tập lệnh được gọi là tệp AC.

## Các thành phần chính của Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools là tập hợp các gói có liên quan, khi được sử dụng cùng nhau sẽ loại bỏ nhiều khó khăn liên quan đến việc tạo phần mềm di động. Những công cụ này, cùng với một số tệp đầu vào được cung cấp ngược dòng tương đối đơn giản, được sử dụng để tạo hệ thống xây dựng cho một gói.

**Tổng quan cơ bản về cách các thành phần chính của công cụ tự động khớp với nhau.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Trong một thiết lập đơn giản:

- Chương trình `autoconf` tạo tập lệnh cấu hình từ `configure.in` hoặc `configure.ac`.
- Chương trình `automake` tạo Makefile.in từ Makefile.am.
- Tập lệnh `configure` được chạy để tạo một hoặc nhiều tệp Makefile từ tệp Makefile.in.
- Chương trình `make` sử dụng Makefile để biên dịch chương trình.

## Người giới thiệu
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Cơ bản về Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



