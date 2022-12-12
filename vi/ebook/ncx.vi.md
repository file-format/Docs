{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "Tệp XML Điều khiển Điều hướng EPUB", "phần mở rộng", "định dạng", "Sách điện tử", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp XML Điều khiển Điều hướng EPUB (NCX) và các API có thể tạo và mở tệp NCX.",
  "title" :"NCX - Tệp XML điều hướng điều hướng EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Tệp NCX là gì? ##

Tệp NCX được viết tắt là tệp Điều khiển Điều hướng cho XML, thường được đặt tên là toc.ncx. Tệp này bao gồm mục lục phân cấp cho tệp EPUB. Thông số kỹ thuật cho NCX được phát triển cho Sách nói kỹ thuật số (DTB) và định dạng tệp này được duy trì bởi **DAISY Consortium** và không phải là một phần của thông số kỹ thuật EPUB. Tệp NCX bao gồm một loại mime **application/x-dtbncx+xml** trong đó.

## Đặc điểm kỹ thuật NCX ##

Tệp NCX chứa nhiều loại thẻ XML khác nhau. Các thẻ meta như `meta name="dtb:uid"` được sử dụng để đề cập đến ID. Phần tử `meta name="dtb:depth"` được đặt bằng độ sâu của phần tử thẻ `navMap`. Các phần tử `navPoint` có thể được lồng vào nhau để tạo mục lục phân cấp. Nội dung của `navLabel` là văn bản xuất hiện trong mục lục được tạo bởi hệ thống đọc sử dụng .ncx. Nội dung của phần tử `navPoint` trỏ đến một tài liệu nội dung được liệt kê trong tệp kê khai và cũng có thể bao gồm một mã định danh phần tử

Mô tả về các ngoại lệ nhất định đối với thông số kỹ thuật NCX như được sử dụng trong EPUB. Tại đây bạn có thể xem ví dụ về tệp NCX:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## Người giới thiệu ##

* [EPUB Từ Wikipedia](https://en.wikipedia.org/wiki/EPUB)
* [Những tệp cần đưa vào toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

