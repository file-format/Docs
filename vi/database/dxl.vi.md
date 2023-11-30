{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DXL và các API có thể tạo và mở tệp DTSX.",
  "title" :"Định dạng tệp DXL - Định dạng tệp ngôn ngữ XML Domino",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Tập tin DXL là gì?

Tệp DXL là tệp lưu trữ dữ liệu dựa trên XML được tạo cho phần mềm cộng tác kinh doanh cấp doanh nghiệp, Lotus Domino. Nó chứa dữ liệu liên quan đến cơ sở dữ liệu Lotus Domino như lược đồ, thành phần thiết kế, dạng xem, biểu mẫu, tài liệu và chính dữ liệu cơ sở dữ liệu. [XML](/vi/web/xml/) là định dạng tệp phổ biến có thể được đọc bởi các ứng dụng phần mềm được viết bằng bất kỳ ngôn ngữ lập trình nào. Nó cũng có thể đọc được và có thể được mở bằng bất kỳ trình soạn thảo văn bản nào. Đó là lý do tại sao tệp DXL cung cấp khả năng xuất dữ liệu ở định dạng tệp có thể hoán đổi cho nhau.

## Định dạng tệp DXL

Các tệp DXL được lưu ở định dạng tệp XML và có thể dễ dàng đọc được bởi các ứng dụng được viết bằng bất kỳ ngôn ngữ lập trình nào. Các tệp này lưu trữ dữ liệu và cài đặt trong các thẻ XML để phân loại dữ liệu cũng như sắp xếp dữ liệu theo đúng thứ tự

### Ví dụ đầu ra DXL

Sau đây là đoạn trích văn bản đầu ra cho một tài liệu Ghi chú.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## Người giới thiệu

* [Định dạng DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

