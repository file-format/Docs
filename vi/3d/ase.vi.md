{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","tệp", "định dạng", "loại tệp", "phần mở rộng","tệp ASE là gì?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp ASE và các API có thể mở và tạo tệp ASE.",
  "title" :"ASE - Tệp xuất cảnh Autodesk ASCII",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Tệp ASE là gì?

Tệp có phần mở rộng .ase là định dạng tệp Xuất cảnh Autodesk ASCII, là biểu diễn ASCII của cảnh, chứa thông tin 2D hoặc 3D trong khi xuất dữ liệu cảnh bằng Autodesk. Autodesk cung cấp các tùy chọn để bao gồm các thành phần cảnh trong khi xuất dữ liệu cảnh. Bạn có thể bao gồm định nghĩa Lưới cùng với thông tin về đỉnh và mặt, Mô tả vật liệu, chuyển đổi dữ liệu hoạt ảnh cho các đối tượng, định nghĩa lưới hoàn chỉnh của mỗi n khung hình, dữ liệu hoạt ảnh cho máy ảnh và đèn và cài đặt khớp IK.

## Định dạng tệp ASE - Thông tin khác

Các tệp ASE là các tệp văn bản được lưu trữ ở định dạng ASCII có thể được mở trong bất kỳ trình soạn thảo văn bản nào. Tệp ASE có thể chứa các loại thông tin sau do Autodesk cung cấp.

### Tùy chọn đầu ra

* `Định nghĩa lưới` - Xuất định nghĩa của từng lưới, bao gồm thông tin đỉnh và mặt cho các đối tượng hình học. Ngoài ra, bật tính năng này sẽ bật các mục trong hộp nhóm Tùy chọn lưới, được mô tả bên dưới.
* `Materials` - Bao gồm phần mô tả vật liệu. Nếu một vật liệu không được gán cho một đối tượng, màu khung dây của nó sẽ được xuất. Tất cả các cấp của cây tài liệu đều được bao gồm, vì vậy điều này có thể tạo ra rất nhiều văn bản.
* `Phím hoạt ảnh chuyển đổi` - Bao gồm dữ liệu hoạt ảnh chuyển đổi cho các đối tượng. Nếu đối tượng là máy ảnh mục tiêu hoặc đèn chiếu, điều này sẽ bao gồm dữ liệu hoạt hình mục tiêu.
* `Lưới hoạt hình` - Xuất định nghĩa lưới hoàn chỉnh của mọi n khung hình. Tần số được chỉ định bởi spinner Đầu ra Bộ điều khiển, được mô tả bên dưới. Mỗi khối chứa thông tin giống nhau được chỉ định trong hộp nhóm Tùy chọn lưới, được mô tả bên dưới. Bật tính năng này có thể tạo ra một tệp lớn, ngay cả đối với các cảnh nhỏ.
* `Cài đặt máy ảnh/ánh sáng hoạt hình` - Xuất dữ liệu hoạt ảnh cho máy ảnh và đèn, chẳng hạn như màu sắc, cường độ, độ mờ, độ lệch bản đồ, v.v. Xuất ra một khối sau mỗi n khung hình, như được chỉ định bởi công cụ quay vòng Đầu ra của Bộ điều khiển.
* `Inverse Kinematic Joints` - Xuất cài đặt khớp IK trong nhánh Hierarchy.

### Các loại đối tượng

Các mục ở đây cho phép bạn chỉ định loại đối tượng nào bạn muốn đưa vào đầu ra. Bạn có thể bao gồm các đối tượng hình học, hình dạng, máy ảnh, đèn và các đối tượng trợ giúp.

* Hình học
* Hình dạng
* Máy ảnh
* Đèn
* Người trợ giúp

### Tùy chọn lưới

* `Quy tắc lưới` - Xuất các quy tắc mặt và đỉnh. Pháp tuyến của mặt được liệt kê đầu tiên, tiếp theo là pháp tuyến của ba đỉnh đỡ mặt. Bật tính năng này sẽ tạo ra một tệp lớn hơn nhiều.
* `Tọa độ ánh xạ` - Xuất danh sách các đỉnh và mặt ánh xạ, theo cấu trúc TVert và TVFace được mô tả trong Bộ công cụ phát triển phần mềm 3ds Max. Nếu một đối tượng sử dụng ánh xạ khuôn mặt, danh sách bản đồ khuôn mặt được xuất có chứa tọa độ UVW cho từng khuôn mặt.
* `Màu của đỉnh` - Xuất các màu của đỉnh.

### Đầu ra bộ điều khiển

* `Sử dụng khóa` - Xuất giá trị khóa. Nếu bộ điều khiển không sử dụng phím, thì phương pháp Force Sample sẽ được sử dụng. Trong trường hợp bộ điều khiển biến đổi, tùy chọn Sử dụng Phím chỉ hoạt động nếu tất cả các bộ điều khiển biến đổi là Tuyến tính/TCB hoặc Bezier. Nếu một trong các rãnh biến đổi sử dụng một loại bộ điều khiển khác, thì phương pháp Force Sample sẽ được sử dụng cho tất cả các rãnh biến đổi.
* `Lấy mẫu` - Lấy giá trị bộ điều khiển mẫu dựa trên tần số được chỉ định trong Khung trên mỗi Bộ điều khiển mẫu.

## Người giới thiệu

* [Autodesk - Xuất sang ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

