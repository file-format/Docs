{
  "date" : "2021-02-25",
  "keywords" :[ "tệp bdf", "định dạng tệp bdf", "tệp bdf là gì", "tệp", "ví dụ bdf", "phần mở rộng tệp bdf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Định dạng phân phối bitmap Glyph",
  "description":"Tìm hiểu về định dạng tệp BDF và các API có thể tạo và mở tệp BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Tệp BDF là gì?
Các tệp BDF là dạng có thể đọc được của con người và thường được phân phối dưới dạng mã hóa ASCII. Tệp bắt đầu với thông tin chung có liên quan đến phông chữ hoàn chỉnh, tiếp theo là thông tin và ảnh bitmap cho các nét tượng trưng riêng lẻ. Dữ liệu trong đó hiển thị phông chữ cho một hướng kích thước duy nhất. Các số liệu để sử dụng theo nhiều hướng có thể được bao gồm trong một tệp. Trong tệp BDF, mỗi mục được chứa trên một dòng văn bản riêng trong tệp. Khoảng trắng được sử dụng để phân tách các mục trên một dòng.

## Định dạng tệp BDF
BDF viết tắt cho Định dạng phân phối bitmap Glyph; thuộc sở hữu của Adobe là một định dạng tệp để lưu phông chữ kiểu bitmap. Nội dung có dạng tệp văn bản dành cho máy tính cũng như con người có thể đọc được. BDF được sử dụng đặc biệt trong môi trường Unix X Window. Nó đã được thay thế rộng rãi bằng định dạng phông chữ PCF được cho là hiệu quả hơn và bằng phông chữ OpenType và TrueType.
### Cấu trúc tệp BDF
Tệp phông chữ BDF bao gồm ba phần:

- một phần chung áp dụng cho tất cả các nét trong một phông chữ.
- một phần với một mục riêng biệt cho mỗi glyph.
- câu lệnh ENDFONT.

## Thí dụ
Đây là một phông chữ ví dụ có chứa một glyph, cho chữ hoa ASCII 'A'. Các khai báo toàn cục của nó bắt đầu bằng dòng "STARTFONT" và kết thúc bằng dòng "CHARS"
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Người giới thiệu
* [Định dạng phân phối Glyph Bitmap](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Đặc tả định dạng phân phối bitmap Glyph (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

