{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp WSDL - Tệp ngôn ngữ mô tả dịch vụ web",
  "description":"Tìm hiểu về tệp WSDL là gì và các API có thể tạo và mở tệp WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Tệp WSDL là gì?

Tệp WSDL là tệp Ngôn ngữ mô tả dịch vụ web được viết bằng ngôn ngữ XML để mô tả các dịch vụ Web. Nó chứa thông tin về các điểm cuối hoặc giao diện để kết nối với thế giới bên ngoài ở định dạng được chấp nhận rộng rãi. [Thông số định dạng tệp WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (được duy trì bởi W3C.org) xác định các điều khoản xuất bản nguồn cấp dữ liệu để trao đổi dữ liệu nhằm có truy cập ứng dụng từ xa qua các cổng và điểm cuối.

## Định dạng tệp WSDL - Thông tin khác

Các tệp WSDL được lưu dưới dạng tệp XML mà con người có thể đọc được và có thể được mở trong bất kỳ trình soạn thảo văn bản nào để xem nội dung.

## Mô tả dịch vụ WSDL

Thông số kỹ thuật định dạng tệp WSDL 2.0 mô tả dịch vụ WSDL bao gồm hai giai đoạn:

- Giai đoạn trừu tượng
- Giai đoạn bê tông

Khả năng sử dụng lại của các thiết kế mô tả và mối quan tâm độc lập được quản lý bởi một dịch vụ Web. Điều này đạt được bằng cách sử dụng một số loại phần tử khác nhau bao gồm các loại (định nghĩa kiểu dữ liệu), thông báo (dữ liệu được truyền đạt), hoạt động (hành động) và giao thức được dịch vụ sử dụng. Tất cả đều được quản lý ở mức trừu tượng. Liên kết của các chi tiết định dạng dây và vận chuyển được chỉ định bởi liên kết, nhóm các điểm cuối lại với nhau để thực hiện một giao diện chung.

### Những công nghệ nào có thể được sử dụng để giao tiếp với các dịch vụ WSDL?

Một số công nghệ khác nhau có thể được sử dụng để giao tiếp với các dịch vụ WSDL bao gồm các ứng dụng ASP.NET, C/C++ và Java.

## Ví dụ WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

Trong ví dụ này, "thuật ngữ thuật ngữ" portType xác định thao tác một chiều được gọi là "setTerm".

## Người giới thiệu

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Thông số định dạng tệp WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

