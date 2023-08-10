{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extension", "file", "file format", "Database File Type", "Database File Format", "Data Tier AppliCation Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DACPAC và API có thể tạo và mở tệp DACPAC.",
  "title" :"DACPAC - Gói ứng dụng tầng dữ liệu",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Tệp DACPAC là gì?

Tệp có phần mở rộng .dacpac (viết tắt của Data Tier AppliCation Package) là một tệp cơ sở dữ liệu, được tạo bằng ứng dụng lớp dữ liệu Microsoft SQL Server, chứa mô hình cơ sở dữ liệu để biểu diễn các đối tượng cơ sở dữ liệu. Vì nó chứa mô hình hoàn chỉnh của cơ sở dữ liệu nên nó được sử dụng để khôi phục cơ sở dữ liệu từ các chi tiết có sẵn trong mô hình. Các tệp DACPAC thường được bàn giao cho các nhóm triển khai để cài đặt tại cơ sở của khách hàng nhằm khôi phục cơ sở dữ liệu. Chúng có thể được mở bằng
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Định dạng tệp DACPAC - Thông tin khác

Các tệp gói dữ liệu DACPAC thực sự là các tệp ZIP được nén chứa một số tệp [XML](/vi/web/xml/) chứa thông tin về mô hình cơ sở dữ liệu, chẳng hạn như bảng và dạng xem, được sử dụng để khôi phục cơ sở dữ liệu. Để xem nội dung của tệp DACPAC, hãy đổi tên tệp từ .dacpac thành [.zip](/vi/compression/zip/) và giải nén kho lưu trữ zip bằng bất kỳ tiện ích giải nén nào.

Sau đây là một số tệp được tìm thấy bên trong tệp DACPAC.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Gốc.xml

* model.xml

Cần lưu ý rằng DACPAC không chứa DATA và các đối tượng cấp máy chủ khác. Tệp có thể chứa tất cả các loại đối tượng có thể được lưu giữ trong dự án SSDT.

## Người giới thiệu

* [Ứng dụng bậc dữ liệu - Lợi ích](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Triển khai ứng dụng bậc dữ liệu - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Cách tạo tệp DACPAC?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)

