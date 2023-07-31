{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp BCP và các API có thể tạo và mở tệp BCP.",
  "title" :"BCP - Định dạng tệp sao chép hàng loạt máy chủ SQL",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Tệp BCP là gì?

BCP (Định dạng sao chép hàng loạt) là định dạng dữ liệu kỹ thuật của Microsoft SQL Server xác định cấu trúc dữ liệu để lưu trữ các giá trị loại dữ liệu cơ sở dữ liệu khác nhau để nhập/xuất. Định dạng xác định đầy đủ cách giải thích của từng cột dữ liệu để có thể đọc được tập hợp các giá trị được chỉ định trong tệp dữ liệu. Tiện ích [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) sử dụng định dạng tệp BCP để đọc dữ liệu từ một tập tin như vậy và xác định nó.


## Định dạng tệp BCP

Tệp định dạng BCP là một tài liệu XML xác định thứ tự cột, tên và kiểu dữ liệu. Nó cho phép người dùng nhập/xuất số lượng lớn dữ liệu từ tệp dữ liệu chỉ định các trường này. Điều này hữu ích khi nhập hàng loạt giá trị dữ liệu từ các tệp dữ liệu. Số lượng và thứ tự của các trường dữ liệu trong tệp dữ liệu có thể khác với thứ tự trong các cột của bảng đích. Đây là lúc tệp định dạng dữ liệu BCP trợ giúp bằng cách chỉ định thứ tự và loại cột để nhập dữ liệu.

Cấu trúc của tệp định dạng được biểu diễn dưới dạng sau.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Các loại dữ liệu BCP

|Kiểu dữ liệu|Phạm vi|Biểu diễn|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) đến 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|Nhị phân|1 đến 8000 byte|định dạng chuỗi Unicode được mã hóa thập lục phân `Binary = 32000OCTET`|
|Bit|0 hoặc 1|chuỗi Unicode đơn giản Bit = "0" / "1"|
|Char|1 đến 8000|Định dạng chuỗi Unicode, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET với n = 4 x (2.147.483.647)|
|Ngày|0001-01-01 đến 9999-12-31|Định dạng chuỗi YYYY-MM-DD|
|DateTime|1753-01-01 00:00:00.000 đến 9999-12-31 23:59:59.997| Định dạng chuỗi Unicode YYYY-MM-DD hh:mm:ss[.nnn]|
|DateTime2|0001-01-01 00:00:00.0000000 đến 9999-12-31 23:59:59.9999999.| Định dạng chuỗi Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn]|
|DateTimeOffset|0001-01-01 00:00:00.0000000 đến 9999-12-31 23:59:59.9999999 theo múi giờ Giờ Phối hợp Quốc tế (UTC)| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] định dạng chuỗi|
|Số thập phân|-1038 + 1 đến 1038 – 1|Định dạng chuỗi Unicode `Decimal = ["-"] 0*38DIGIT [".."0*38DIGIT]`|
|Float|-1,79E+308 đến -2,23E-308; 0; từ 2.23E-308 đến 1.79E+308|Định dạng chuỗi Unicode|
|Hình ảnh|chuỗi byte nằm trong khoảng từ 0 đến 231 – 1 (2,147,483,647)|định dạng chuỗi Unicode được mã hóa thập lục phân|
|Int|-231 (-2,147,483,648) đến 231 – 1 (2,147,483,647)|Định dạng chuỗi Unicode|

## Người giới thiệu

* [Định dạng BCP - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

