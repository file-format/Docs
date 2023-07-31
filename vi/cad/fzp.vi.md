{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp FZP và API có thể tạo và mở tệp FZP.",
  "title" :"Định dạng tệp FZP - Tệp mô tả phần Fritzing XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Tệp FZP là gì?

Tệp FZP là một tệp XML được tạo bởi ứng dụng thiết kế và tạo mẫu mạch điện tử [Fritzing](https://fritzing.org/). Nó chứa thông tin về các thuộc tính, trình kết nối và bus của bộ phận ở định dạng tệp [XML](/vi/web/xml/). Các tệp FPZ không thể được sử dụng độc lập trong Fritzing. Thay vào đó, chúng được nhập như một phần của tệp lưu trữ FZPZ.

## Định dạng tệp FZP - Thông tin khác

Các tệp FZP là các tệp XML chứa thông tin về các thuộc tính, trình kết nối và xe buýt của bộ phận. Ngoài ra, các tệp FZP còn chứa thông tin về tiêu đề, mô tả, tác giả và ngày xuất bản của tệp FZP. Khi một tệp phần Fritzing được xuất, ứng dụng Fritzing sẽ tạo một kho lưu trữ nén [FZPZ](/vi/compression/fzpz/) chứa một tệp FZP và bốn tệp [SVG](/vi/page-description-language/svg/).

[Thông số định dạng tệp FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) hiện có trên Github của Fritzing.

## Ví dụ cấu trúc tệp FZP

Một tệp FZP điển hình có cấu trúc XML sau.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Người giới thiệu

* [Thông số định dạng tệp FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Phần mới với phần mở rộng fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

