{
  "date" : "2019-10-11",
  "keywords" :["xml", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "ngôn ngữ đánh dấu mở rộng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp XML",
  "description":"Tìm hiểu về định dạng tệp XML và các API có thể tạo và mở tệp XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp XML là gì?

XML là viết tắt của Extensible Markup Language tương tự như **[HTML](/vi/web/html/)** nhưng khác ở chỗ sử dụng thẻ để xác định đối tượng. Toàn bộ ý tưởng đằng sau việc tạo định dạng tệp XML là để lưu trữ và vận chuyển dữ liệu mà không phụ thuộc vào phần mềm hoặc công cụ phần cứng. Sự phổ biến của nó là do nó có thể đọc được cả ở người và máy. Điều này cho phép nó tạo ra các giao thức dữ liệu chung dưới dạng các đối tượng được lưu trữ và chia sẻ qua mạng, chẳng hạn như World Wide Web (WWW). Chữ "X" trong XML có nghĩa là có thể mở rộng, ngụ ý rằng ngôn ngữ có thể được mở rộng thành bất kỳ số lượng ký hiệu nào theo yêu cầu của người dùng. Chính vì những tính năng này mà nhiều định dạng tệp tiêu chuẩn sử dụng nó, chẳng hạn như Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/vi/web/xhtml/)** và **[SVG](/vi/page-description-language/svg/)**.

## Định dạng tệp XML

Định dạng tệp XML dựa trên Mô hình Đối tượng Tài liệu XML (DOM) là API lập trình cho các tài liệu HTML và XML. XML DOM định nghĩa một phương pháp tiêu chuẩn để truy cập và thao tác các phần tử tài liệu XML. Nó tạo ra một dạng xem cấu trúc cây của một tài liệu XML có thể được sử dụng để truy cập tất cả các phần tử thông qua cây DOM. Các phần tử hiện có có thể được sửa đổi/xóa cũng như các phần tử mới có thể được tạo trong cây XML. Mỗi phần tử của một tài liệu XML được gọi là một nút. XML DOM được hiển thị trong hình dưới đây.

{{< figure src="../XML DOM.png" alt="DOM XML" >}}

### Cách tiếp cận chung của XML

Sức mạnh của XML làm cho nó trở thành một ngôn ngữ chung để truyền dữ liệu qua mạng bằng cách đơn giản hóa việc truyền tải dữ liệu và thay đổi nền tảng. Điều này cũng đảm bảo có thể trao đổi dữ liệu giữa các hệ thống không tương thích bằng cách lưu trữ dữ liệu ở định dạng văn bản thuần túy. HTML dùng để biểu diễn dữ liệu trên web, trong khi XML dùng để trao đổi dữ liệu. Các cặp thẻ đánh dấu được sử dụng bên trong XML xác định các thành phần chính của cấu trúc sẽ được ứng dụng đọc sử dụng.

## Ví dụ XML

Sau đây là một ví dụ đơn giản về danh mục đĩa CD trong đó mỗi bản ghi chứa thông tin về đĩa CD chẳng hạn như nghệ sĩ, quốc gia, công ty, giá cả và năm sản xuất.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Người giới thiệu

* [XML - Theo Wikipedia](https://en.wikipedia.org/wiki/XML)

