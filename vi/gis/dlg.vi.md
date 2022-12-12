{
  "date" : "2021-07-30",
  "keywords" :[ "tệp dlg", "định dạng tệp dlg", "tệp dlg là gì", "tệp", "ví dụ dlg", "phần mở rộng tệp dlg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Định dạng Chỉ mục Hình dạng Shapefile",
  "description":"Tìm hiểu về định dạng tệp DLG và các API có thể tạo và mở tệp DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Tệp DLG là gì?
Một tệp có phần mở rộng .dlg chứa Biểu đồ đường kỹ thuật số là một tính năng bản đồ bản đồ được hiển thị ở dạng véc tơ kỹ thuật số do Cơ quan Khảo sát Địa chất Hoa Kỳ (USGS) quản lý. Các tệp DLG có sẵn ở hai định dạng khác nhau:
1. **Định dạng tùy chọn**: Một định dạng dễ sử dụng kết hợp độ dài bản ghi logic 80 byte, hệ tọa độ nền UTM và các liên kết cấu trúc liên kết có trong các phần tử đường, nút và vùng.
2. **Định dạng chuẩn truyền dữ liệu không gian (SDTS)**: định dạng hỗ trợ truyền dữ liệu không gian giữa các hệ thống máy tính khác nhau.

## Định dạng tệp DLG
Định dạng tệp DLG được thiết kế cho bản đồ USGS và được truyền ở quy mô lớn, trung bình và nhỏ với tối đa chín loại tính năng khác nhau. Các tệp DLG có các định dạng Tiêu chuẩn truyền dữ liệu không gian và tùy chọn (SDTS) có cấu trúc tô pô để sử dụng trong các ứng dụng bản đồ và GIS.
### Thông số kỹ thuật của Định dạng tệp DLG
Các tệp DLG được phân phối ở ba tỷ lệ khác nhau:

1. **Quy mô lớn** - thường tương ứng với:
- USGS 7,5- x 7,5 phút
- Loạt bản đồ địa hình tứ giác tỷ lệ 1:24.000 và 1:25.000
- Tỷ lệ 1:63,360 cho Alaska
- Tỷ lệ 1:30.000 cho Puerto Rico
 

2. **Quy mô trung bình** - bắt nguồn từ USGS:

- 30- x 60 phút

- Dòng bản đồ tỷ lệ 1:100.000
3. **Tỷ lệ nhỏ** - bắt nguồn từ các bản đồ mặt cắt tỷ lệ 1:2.000.000 của USGS của National Atlas of the United States
### Danh mục dữ liệu
Chín loại lớp hoặc tính năng khác nhau có sẵn trong các tệp DLG:
1. Hệ thống Khảo sát Đất đai Công cộng (PLSS)
2. Ranh giới (BD)
3. Giao thông vận tải (TR)
4. Thủy văn (HY)
5. Siêu âm (HP)
6. Tính năng phi thực vật (NV)
7. Kiểm soát và đánh dấu khảo sát (SM)

8. Tính năng nhân tạo (MS)

9. Lớp phủ bề mặt thực vật (SC)

Các tệp DLG quy mô lớn cung cấp tất cả chín lớp, trong khi quy mô trung bình cung cấp năm lớp PLSS, BD, TR, HY và HP. Các DLG quy mô nhỏ cung cấp năm lớp PLSS, BD, TR, HY và MS.

## Người giới thiệu

* [Biểu đồ đường kỹ thuật số - theo Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


