{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - Định dạng lưới nhị phân ArcInfo của ESRI",
  "description":"Tìm hiểu về định dạng tệp ADF và API có thể tạo và mở tệp ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Tệp ADF là gì?

Tệp có phần mở rộng .adf là định dạng tệp dữ liệu raster được sử dụng bởi các ứng dụng phần mềm ESRI như ArcGIS, ArcView và ArcInfo. Dữ liệu không gian được lưu trữ dưới dạng lưới nhị phân có nguồn gốc từ ESRI. Lưới được tạo thành từ các hàng và cột của các ô có thể là số nguyên cũng như dấu phẩy động. Lưới số nguyên trong tệp ADF biểu thị dữ liệu rời rạc và lưới dấu phẩy động biểu thị dữ liệu liên tục. Một định dạng tệp ESRI phổ biến khác là tệp [SHP](/vi/gis/shp/) biểu thị thông tin Không gian địa lý ở dạng dữ liệu vectơ được các ứng dụng Hệ thống Thông tin Địa lý (GIS) sử dụng.

## Định dạng tệp ADF - Thông tin khác

Các tệp ADF được lưu dưới dạng tệp nhị phân vào đĩa trong lưới nhị phân. Lưới số nguyên có các thuộc tính được lưu trữ trong bảng thuộc tính giá trị (VAT). Mỗi giá trị duy nhất trong lưới có một bản ghi trong VAT trong đó bản ghi lưu trữ giá trị duy nhất và số lượng ô trong lưới được biểu thị bằng giá trị đó.

Lưới dấu chấm động không có VAT.

### Cấu trúc lưới

Bên trong tệp ADF, các lưới được triển khai bằng cách sử dụng cấu trúc dữ liệu raster lát gạch. Đơn vị cơ bản bên trong cấu trúc dữ liệu raster này là một khối ô hình chữ nhật. Mỗi khối được lưu trữ trên đĩa và được nén trong cấu trúc tệp có độ dài thay đổi, được gọi là ô xếp. Mỗi khối được lưu trữ dưới dạng một bản ghi có độ dài thay đổi.

Trình quét GRID được lưu trữ trong không gian làm việc, trong đó không gian làm việc chứa một thư mục con thông tin và một thư mục con cho mỗi GRID. Có một số tệp vị trí địa lý và dữ liệu thuộc tính cho lưới tương ứng. Thư mục con Thông tin chứa một số tệp duy trì thông tin nhất định về GRID và các bộ dữ liệu khác, chẳng hạn như phạm vi bảo hiểm, trong không gian làm việc.

## Người giới thiệu ##

* [Định dạng lưới ESRI](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [Câu hỏi thường gặp: Cấu trúc tệp của Lưới Arc/INFO là gì?](https://support.esri.com/en/technical-article/000008526)

