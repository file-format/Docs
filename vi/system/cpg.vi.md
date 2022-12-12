{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp CPG - Tệp trang mã ESRI",
  "description":"Tìm hiểu về định dạng tệp CPG và API có thể tạo và mở tệp CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Tệp CPG là gì?

Tệp CPG là một tệp tùy chọn được yêu cầu là ESRI Shapefile được sử dụng để chỉ định trang mã để xác định bộ ký tự sẽ được sử dụng. Chúng được lưu trữ ở định dạng tệp văn bản thuần túy và chứa thông tin về mã hóa được áp dụng để tạo tệp hình dạng. Trong trường hợp tệp CPG không có sẵn, thì tệp hình dạng sẽ sử dụng mã hóa mặc định của hệ thống. Một tệp CPG, nếu có, phải có cùng tiền tố với tiền tố của tệp [SHP](/vi/gis/shp/), ví dụ: đường.shp, đường.cpg.

Các tệp CPG có thể được mở bằng ESRI ArcGIS Pro.

### Định dạng tệp CPG - Thông tin thêm

Khi xem tệp hình dạng trong ArcCatalog hoặc bất kỳ ứng dụng ArcGIS nào khác, bạn chỉ thấy tệp hình dạng đó. Nhưng trên thực tế, shapefile sử dụng các tệp liên quan khác được đọc cùng với tệp hình dạng chính. Tệp CPG cũng là một trong số này nếu nó xuất hiện cùng với tệp SHP chính.

## Người giới thiệu

* [Phần mở rộng tệp Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

