{
  "date" : "2021-07-28",
  "keywords" :[ "tệp ntf", "định dạng tệp ntf", "tệp ntf là gì", "tệp", "ví dụ ntf", "phần mở rộng tệp ntf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Tệp định dạng chuyển quốc gia",
  "description":"Tìm hiểu về định dạng tệp NTF và API có thể tạo và mở tệp NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Tệp NTF là gì?
Các tệp có phần mở rộng .ntf được gọi là tệp **Định dạng chuyển giao quốc gia (NTF)**; chủ yếu được sử dụng bởi Cơ quan Khảo sát Vũ khí Vương quốc Anh (OS); đặc biệt cho việc truyền dữ liệu không gian địa lý. Nó được quản lý bởi Viện tiêu chuẩn Anh. Nó đã trở thành định dạng truyền tiêu chuẩn cho dữ liệu kỹ thuật số Khảo sát bom mìn. Phép chiếu Lưới quốc gia của Vương quốc Anh, là một loại Transverse Mercator, chứa tất cả thông tin được tham chiếu địa lý cho các tệp NTF.

## Định dạng tệp NTF
Định dạng tệp NTF thuộc sở hữu của Ordnance Survey ở Vương quốc Anh; được thư viện GDB hỗ trợ để nhập. Phiên bản hiện tại của định dạng tệp NTF là 2.0. Định dạng tệp này được giới thiệu để giải quyết hạn chế của phân đoạn vectơ **PCIDSK** chỉ có một trường thuộc tính cho mỗi cấu trúc, nhưng có nhiều loại thuộc tính có thể được trích xuất bằng dữ liệu vectơ. Để giải quyết vấn đề, định dạng tệp NTF được cấu thành là có hai phân đoạn. Mỗi đoạn bao gồm các vectơ giống nhau, nhưng có các thuộc tính khác nhau. Phân đoạn đầu tiên của tệp vectơ NTF chứa các vectơ có số mã tính năng làm thuộc tính. Đoạn thứ hai chứa các vectơ có giá trị là thuộc tính.

### Hệ quy chiếu tọa độ
Thư viện GDB đại diện cho dữ liệu raster và vector với các đặc điểm chiếu TM thích hợp:

- Kinh độ tham chiếu: 49.0
- Vĩ độ tham chiếu: 2.0
- Sai hướng đông: 400000
- Định hướng sai: -100000
- Tỷ lệ: 0,9996012717
- Ellipsoid: Air 1830 (E009)
Không có hỗ trợ nào để cập nhật hoặc ghi các tệp NTF cũng như không thể liên kết các tệp DTM.

### Ví dụ Ogrinfo
Ví dụ sau sử dụng **ogrinfo** trên tệp NTF để truy xuất số lớp:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Người giới thiệu

* [Định dạng chuyển quốc gia của Vương quốc Anh (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Bản đồ web - Minh họa bởi Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

