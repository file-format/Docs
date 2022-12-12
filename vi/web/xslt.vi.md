{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "Ngôn ngữ biểu định kiểu mở rộng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp XSLT",
  "description":"Tìm hiểu về định dạng tệp XSLT và các API có thể tạo và mở tệp XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Tệp XSLT là gì?

Tệp có phần mở rộng .xslt là tệp Chuyển đổi ngôn ngữ biểu định kiểu mở rộng được sử dụng để chuyển đổi và tạo kiểu cho tệp XML bằng hướng dẫn XSL. Định dạng này được sử dụng để chuyển đổi các tài liệu XML thành các định dạng đầu ra tiêu chuẩn, chẳng hạn như tài liệu văn bản hoặc trang web .html. Việc chuyển đổi này tạo ra một tài liệu mới dựa trên nội dung của tài liệu XML hiện có. XSLT đang làm cho nó có khả năng tính toán tùy ý về mặt lý thuyết.

## Định dạng tệp XSLT

Định dạng tệp XLST chứa các hướng dẫn chuyển đổi ở định dạng văn bản thuần túy có thể được xem trong bất kỳ trình soạn thảo văn bản nào. Đã có ba lần sửa đổi ngôn ngữ.

* `XSLT 1.0` - XSLT 1.0 được xuất bản dưới dạng đề xuất của W3C vào tháng 11 năm 1999.
* `XSLT 2.0` - Nó bao gồm các sửa đổi như thao tác Chuỗi bằng cách sử dụng các biểu thức, hàm và toán tử thông thường để thao tác ngày, giờ và thời lượng, nhiều tài liệu đầu ra, nhóm và hệ thống loại phong phú hơn cũng như kiểm tra loại mạnh.
* `XSLT 3.0` - Nó đã trở thành một phần của Khuyến nghị W3C vào ngày 8 tháng 6 năm 2017 và các tính năng mới chính bao gồm chuyển đổi phát trực tuyến, Các gói để cải thiện tính mô-đun của các biểu định kiểu lớn, cải thiện khả năng xử lý các lỗi động, chẳng hạn như lệnh xsl:try, và hỗ trợ cho bản đồ và mảng, cho phép XSLT xử lý JSON cũng như XML.

### Ví dụ XSLT

Ví dụ sau được lấy từ [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## Người giới thiệu ##

* [XSLT - Theo Wikipedia](https://vi.wikipedia.org/wiki/XSLT)
* [Các yếu tố XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

