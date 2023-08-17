{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","tệp xbrl", "định dạng tệp xbrl", "loại tệp xbrl", "tệp", "loại", "tệp xbrl là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Định dạng tệp báo cáo tài chính và kinh doanh",
  "description":"Tìm hiểu về định dạng tệp XBRL và các API có thể tạo và mở tệp XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Tệp XBRL là gì?

Tệp có phần mở rộng .xbrl (Ngôn ngữ báo cáo kinh doanh có thể mở rộng) là một khuôn khổ toàn cầu và có sẵn miễn phí để trao đổi thông tin kinh doanh. Nó hiện được sử dụng rộng rãi như một trong những định dạng tiêu chuẩn đã thay thế các báo cáo trên giấy cũ hơn bằng các bản ghi kỹ thuật số hữu ích và chính xác hơn. Dữ liệu được trao đổi bằng các tệp XBRL bao gồm sổ cái, chi tiết tài chính và bảng cân đối kế toán. Nó hỗ trợ các thẻ dữ liệu cho phép xử lý dữ liệu từ giai đoạn chuẩn bị cho đến giai đoạn phân tích thông tin kinh doanh các loại. Có thể mở các tệp XBRL bằng phần mềm như Rivet Software Dragon View XBRL Viewer và các API như [Aspose.Finance](https://products.aspose.com/finance/).

## Định dạng tệp XBRL

XBRL là một tiêu chuẩn quốc tế mở cho báo cáo kinh doanh kỹ thuật số được sử dụng rộng rãi trên toàn cầu. Đó là ngôn ngữ dựa trên [XML](/vi/web/xml/) sử dụng các phần tử XBRL, được gọi là thẻ, để mô tả từng mục dữ liệu kinh doanh nhằm xây dựng dữ liệu để sắp xếp và phân tích báo cáo. Thông số định dạng tệp XBRL được XBRL International, Inc phát triển và xuất bản với [XBRL phiên bản 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) hiện tại có sẵn cho người dùng.

### Cấu trúc tài liệu XBRL

Thông tin đầy đủ về [thẻ XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) có thể được các lập trình viên giới thiệu để viết các ứng dụng để làm việc với định dạng tệp này. Một XBRL bao gồm một thể hiện XBRL và một tập hợp các nguyên tắc phân loại.

**`XBRL Instance`** - Phiên bản XBRL bắt đầu bằng<xbrl> phần tử gốc. Một tài liệu XML lớn có thể chứa nhiều hơn một phiên bản XBRL được nhúng trong đó.

**`XBRL Taxonomy`** - [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) được định nghĩa là cấu trúc lược đồ XML và tập hợp các phần tử liên kết bên ngoài được tham chiếu trực tiếp. Lược đồ phân loại có thể mở rộng hiển thị các tham chiếu cơ sở liên kết như sau.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Người giới thiệu ##

* [XBRL - Theo Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Ngôn ngữ báo cáo kinh doanh có thể mở rộng (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

