{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Tệp ODTTF - Định dạng tệp phông chữ OpenType bị xáo trộn",
  "description": "Tìm hiểu về định dạng tệp ODTTF và các API có thể tạo và mở tệp ODTTF.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-vif"
}
},
  "lastmod": "2023-01-13"
}

## Tệp ODTTF là gì?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Bạn có thể mở tệp ODTTF bằng Pagemark XpsViewer, Apple Safari bằng Pagemark XpsPlugin, Mozilla Firefox với Pagemark XpsPlugin,
Chế độ xem NiXPS và Chỉnh sửa NiXPS.

## Định dạng tệp ODTTF

Cấu trúc định dạng tệp nội bộ của định dạng tệp ODTTF không được biết vì chúng được lưu trữ dưới dạng định dạng được nhúng. Chúng có thể được nhúng trong các tài liệu kỹ thuật số như .PDF hoặc .DOCX.

## Người giới thiệu
 * [Thông số phông chữ OpenType của Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [Tổng quan về TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

