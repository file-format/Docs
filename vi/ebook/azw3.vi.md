{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "phần mở rộng", "tệp", "định dạng", "sách điện tử", "Định dạng tệp Kindle", "Cấu trúc tệp AZW3" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp AZW3 và API có thể tạo và mở tệp AZW3.",
  "title" :"Tệp AZW3 là gì?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Tệp AZW3 là gì?

AZW3, còn được gọi là Kindle Format 8 (**KF8**), là phiên bản sửa đổi của định dạng tệp kỹ thuật số sách điện tử [AZW](/vi/ebook/azw/) được phát triển cho các thiết bị Amazon Kindle. Định dạng này là một cải tiến cho các tệp AZW cũ hơn và chỉ được sử dụng trên các thiết bị Kindle Fire với khả năng tương thích ngược với định dạng tệp gốc, ví dụ như [MOBI](/vi/ebook/mobi/) và AZW. Amazon đã giới thiệu định dạng KFX (KF phiên bản 10) sau KF8 được sử dụng trên các thiết bị Kindle mới nhất. Các tệp AZW3 có loại phương tiện internet application/vnd.amazon.mobi8-ebook. Các tệp AZW3 có thể được chuyển đổi sang một số định dạng tệp khác như [PDF](/vi/pdf/), [EPUB](/vi/ebook/epub/), [AZW](/vi/ebook/azw/), [DOCX](/vi/word-processing/docx/), và [RTF](/vi/word-processing/rtf/).

## Định dạng tệp AZ3/KF8 ##

Các tệp KF8 có bản chất là nhị phân và giữ nguyên cấu trúc của định dạng tệp MOBI dưới dạng tệp PDB. Như đã đề cập trước đó, tệp KF8 có thể bao gồm cả MOBI cũng như phiên bản KF8 mới hơn của EPUB sau này. Các chi tiết bên trong của định dạng đã được giải mã bởi [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), đây là một tập lệnh Python phân tích cú pháp cơ sở dữ liệu được biên dịch cuối cùng và trích xuất các tệp nguồn MOBI hoặc AZW từ cơ sở dữ liệu đó. Các tệp AZW3 (KF8) cũng nhắm mục tiêu phiên bản EPUB3 với khả năng tương thích ngược cho EPUB. KF8 biên dịch các tệp EPUB và tạo cấu trúc nhị phân dựa trên định dạng tệp PDB.

## Người giới thiệu ##

* [KF8 - Theo Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

