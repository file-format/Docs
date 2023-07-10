{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SSF - Tệp định dạng lưu trữ tiêu chuẩn Trimble",
  "description":"Tìm hiểu về định dạng tệp SSF và các API có thể tạo và mở tệp SSF.",
  "linktitle" : "SSF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-24"
}

## Tệp SSF là gì?

Tệp có đuôi .ssf là định dạng tệp lưu trữ dữ liệu Địa không gian được các ứng dụng phần mềm GIS Điều hướng [Trimble](https://www.trimble.com) sử dụng. Nó lưu trữ dữ liệu GPS được ghi từ trường bằng thiết bị Trimble. Nhật ký GPS sau đó được nhập vào một trong các ứng dụng của bộ ứng dụng Trimble. Nhật ký GPS có trong SSF được sử dụng để tạo các hệ tọa độ tùy chỉnh. Có thể mở các tệp SSF bằng [Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/products-and-solutions/ssf-and-ddf-data-format-extensions-fme), Trimble Navigation GPS Pathfinder Tools SDK và ESRI ArcGIS cho Máy tính để bàn với Plug-in Trimble GPS Analyst.

## Định dạng tệp SSF - Thông tin khác

Khi dữ liệu GPS được truyền từ thiết bị Trimble sang máy tính để xử lý hậu kỳ, tất cả các tệp này được kết hợp với nhau thành một tệp .ssf duy nhất. Tệp thô chưa qua xử lý này được phần mềm xử lý hậu kỳ sử dụng để chỉnh sửa và hỗ trợ quản lý dữ liệu.

Các tệp SSF được lưu trữ vào đĩa dưới dạng định dạng tệp độc quyền của Trimble và các thông số kỹ thuật chi tiết của nó không có sẵn công khai. Nó dành riêng cho các thiết bị Trimble và đại diện cho dữ liệu của thiết bị GPS. Cho đến nay, không có giải pháp miễn phí phi thương mại nào có sẵn để đọc hoặc chuyển đổi các tệp SSF.

## Người giới thiệu

* [Bản tin Trimble](https://www.trimble.com/news/release.aspx?id=050510b)

