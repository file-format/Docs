{
  "date" : "2021-07-29",
  "keywords" :[ "tệp gpkg", "định dạng tệp gpkg", "tệp gpkg là gì", "tệp", "ví dụ gpkg", "phần mở rộng tệp gpkg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - Tệp định dạng GeoPackage",
  "description":"Tìm hiểu về định dạng tệp GPKG và API có thể tạo và mở tệp GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Tệp GPKG là gì?
Một tệp có phần mở rộng .gpkg bao gồm một hệ thống thông tin địa lý được triển khai dưới dạng bộ chứa cơ sở dữ liệu SQLite chứa các bảng dữ liệu và siêu dữ liệu với các định nghĩa điển hình, giới hạn định dạng, xác nhận tính toàn vẹn và ràng buộc nội dung. Nó được xuất bản vào năm 2014; được xác định bởi OGC (Open Geospatial Consortium) thay mặt cho quân đội Hoa Kỳ. Nhiều chính phủ, tổ chức thương mại và nguồn mở hỗ trợ rộng rãi GeoPackage.

## Định dạng tệp GPKG
GeoPackage được tạo thành tệp cơ sở dữ liệu SQLite 3 mở rộng; một tiêu chuẩn xác định một bộ quy tắc (quy ước bắt buộc) cho:
- Lưu trữ các tập hợp hình ảnh ma trận gạch
- Tính năng véc tơ
- Bản đồ raster ở các tỷ lệ khác nhau
- Siêu dữ liệu và lược đồ

Bạn có thể mở rộng GeoPackage bằng cách sử dụng các quy tắc mở rộng như được định nghĩa trong khoản 2.3 của tiêu chuẩn. Mục đích của việc thiết kế GeoPackage là tạo ra một cơ sở dữ liệu nhẹ nhất có thể và đưa nó vào một tệp duy nhất sẵn sàng sử dụng. Điều này làm cho nó trở nên lý tưởng cho các ứng dụng di động ở chế độ ngoại tuyến và chia sẻ nhanh trên bộ lưu trữ đám mây hoặc thiết bị lưu trữ USB, v.v.

### Nội dung GPKG
GeoPackages chứa một số bảng, giống như các cơ sở dữ liệu quan hệ khác. Các bảng này có thể là bảng do người dùng định nghĩa hoặc bảng siêu dữ liệu. GeoPackages bao gồm hai bảng siêu dữ liệu bắt buộc:

#### gpkg_contents
Mục lục cho GeoPackage. Các cột bắt buộc trong bảng này là:

- **table_name**: tên thật của bảng dữ liệu do người dùng định nghĩa;
- **data_type**: kiểu dữ liệu, ví dụ: tiêu đề, tính năng và thuộc tính;
- **mã định danh và mô tả**: văn bản con người có thể đọc được;
- **last_change**: ngày cung cấp thông tin về lần thay đổi cuối cùng, ở định dạng ISO 8601 ;
- **min_x, min_y, max_x và max_y**: phạm vi không gian của nội dung. ;
- **srs_id**: hệ quy chiếu không gian .

#### gpkg_spatial_ref_sys
Đối với nội dung tham chiếu không gian; bao gồm nhưng không giới hạn ở các ô và tính năng, mỗi hàng trong nội dung phải tham chiếu một hệ quy chiếu tọa độ; được lưu trữ trong bảng **gpkg_spatial_ref_sys**. Các cột bắt buộc trong bảng này là:

- **srs_name, description**: tên và mô tả có thể đọc được của con người đối với SRS;
- **srs_id**: mã định danh duy nhất cho SRS; cũng là khóa chính của bảng;
- **tổ chức**: Tên không phân biệt chữ hoa chữ thường của tổ chức xác định.
- **organization_coordsys_id**: ID số của SRS do tổ chức chỉ định;
- **definition**: Định nghĩa Văn bản Nổi tiếng của SRS.


## Người giới thiệu

* [Gói địa lý - theo Wikipedia)](https://en.wikipedia.org/wiki/GeoPackage)
* [Bắt đầu với GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

