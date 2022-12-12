{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp ACCDT và API có thể tạo và mở tệp ACCDT.",
  "title" :"ACCDT - Định dạng tệp cơ sở dữ liệu mẫu Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Tệp ACCDT là gì?

Tệp có phần mở rộng .accdt là tệp mẫu cơ sở dữ liệu Microsoft Access có chứa các thành phần cơ sở dữ liệu được xác định trước. Các phần tử này là tập hợp các cấu trúc xác định ứng dụng cơ sở dữ liệu, chẳng hạn như lược đồ cơ sở dữ liệu để lưu trữ dữ liệu, mô tả bố cục cho dạng xem dữ liệu và siêu dữ liệu mô tả cơ sở dữ liệu. Là các tệp mẫu, các tệp ACCDT có thể được sử dụng để tạo cơ sở dữ liệu dựa trên các cài đặt mẫu có sẵn trong các tệp này. Các tệp cơ sở dữ liệu kết quả được lưu dưới dạng tệp [ACCDB](/vi/database/accdb/) và được điền bằng dữ liệu trong các bảng. Microsoft Access 2007 trở đi có thể mở tệp ACCDT.

## Định dạng tệp ACDT

Các tệp mẫu ACCDT dựa trên các thông số kỹ thuật của Office Open XML và tất cả dữ liệu được chứa trong gói ZIP. Thông tin về cấu trúc và nội dung của cơ sở dữ liệu được chứa trong tệp [XML](/vi/web/xml/) và tệp văn bản và được liên kết với nhau thông qua các mối quan hệ. Bạn có thể đổi tên tệp ACCDT thành phần mở rộng [.zip](/vi/compression/zip/) và sử dụng bất kỳ phần mềm nén nào để trích xuất nội dung của kho lưu trữ ZIP.

### Cấu trúc tệp

Các tệp ACCDT là các gói chứa tập hợp các phần liên quan. Mỗi **phần** lưu trữ thông tin về nội dung của ứng dụng cơ sở dữ liệu bằng định dạng XML, văn bản và nhị phân, bao gồm:

* Đối tượng cơ sở dữ liệu
* Siêu dữ liệu được liên kết
* Cấu trúc của gói

#### Bưu kiện

Gói là tệp lưu trữ [ZIP](/vi/compression/zip/) chứa nhiều phần và tuân thủ Quy ước đóng gói mở được chỉ định trong [ISO/IEC-29500-2](https://go.microsoft.com/fwlink/ ?LinkId=150883). Các tệp ACCDT phải chứa ít nhất một phần siêu dữ liệu Mẫu phải là mục tiêu của mối quan hệ. Siêu dữ liệu mẫu này là phần bắt đầu của tệp ACCDT.

#### Phần

Một phần là một luồng byte có loại được liên kết để chỉ định bản chất và loại nội dung được lưu trữ trong đó. Việc liệt kê các bộ phận xác định các bộ phận hợp lệ, các kiểu nội dung hợp lệ và các mối quan hệ bắt buộc giữa tất cả các bộ phận trong một gói.

#### Mối quan hệ

`Mối quan hệ gói` - trong đó đích là một phần và nguồn là toàn bộ gói.

`Mối quan hệ giữa các phần` - trong đó đích là một phần và nguồn là một phần trong gói.

`Mối quan hệ rõ ràng` - nơi tài nguyên được tham chiếu từ nội dung của phần nguồn bằng cách tham chiếu phần tử mối quan hệ theo giá trị của thuộc tính ID của nó.

`Mối quan hệ ngầm định` - một mối quan hệ không rõ ràng.

`Mối quan hệ nội bộ` - trong đó mục tiêu là một phần trong gói.

`Mối quan hệ bên ngoài` - trong đó mục tiêu là tài nguyên bên ngoài không có trong gói.

## Người giới thiệu ##

* [Định dạng tệp mẫu truy cập](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

