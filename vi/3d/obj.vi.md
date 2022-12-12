{
  "date" : "2019-10-11",
  "keywords" :[ "tệp obj", "định dạng tệp obj", "tệp obj là gì", "tệp", "ví dụ obj", "phần mở rộng tệp obj","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp OBJ",
  "description":"Tìm hiểu về định dạng tệp OBJ và API có thể mở và tạo tệp OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp OBJ là gì?

Các tệp **OBJ** được ứng dụng Advanced Visualizer của Wavefront sử dụng để xác định và lưu trữ các đối tượng hình học. Có thể truyền ngược và xuôi dữ liệu hình học thông qua các tệp OBJ. Cả hình học đa giác như điểm, đường thẳng, đỉnh kết cấu, mặt và hình học dạng tự do (đường cong và bề mặt) đều được định dạng OBJ hỗ trợ. Định dạng này không hỗ trợ hoạt ảnh hoặc thông tin liên quan đến ánh sáng và vị trí của cảnh.

Tệp OBJ thường là sản phẩm cuối cùng của quy trình tạo mô hình 3D do CAD (Thiết kế hỗ trợ máy tính) tạo ra. Thứ tự mặc định để lưu trữ các đỉnh là ngược chiều kim đồng hồ để tránh khai báo rõ ràng các quy tắc khuôn mặt. Mặc dù các tệp OBJ khai báo thông tin tỷ lệ trong dòng nhận xét nhưng không có đơn vị nào được khai báo cho tọa độ OBJ.

## Lịch sử định dạng 3D OBJ

Wavefront Technologies đã tạo định dạng tệp OBJ cho ứng dụng Advanced Visualizer của mình để lưu trữ các đối tượng hình học và dữ liệu 3D. Phiên bản 2.11 của nó được thay thế bằng phiên bản 3 mới được ghi lại. Định dạng tệp mở và đã được các nhà cung cấp khác triển khai cho ứng dụng đồ họa 3D của họ. Wavefront Technologies giữ định dạng tệp này là mã nguồn mở và trung lập.

## Định dạng tệp OBJ

Trong các đối tượng 3D, mã hóa hình học bề mặt là một công việc đầy thách thức mà định dạng tệp OBJ đã hoàn thành rất tốt. Định dạng này khá linh hoạt vì nó cung cấp một số lựa chọn để mã hóa hình dạng bề mặt. Sau đây là ba định dạng được phép có những ưu điểm và nhược điểm riêng:

### Tessellation với các mặt đa giác

Định dạng tệp OBJ tạo điều kiện cho người dùng tạo bề mặt mô hình 3D bằng các hình dạng hình học đơn giản hoặc phức tạp. Đối với mã hóa hình học bề mặt của một mô hình, một tệp lưu trữ các đỉnh và bình thường của mỗi đa giác. Mặc dù tessellation làm tăng độ thô cho mô hình, nhưng Cần phải khám phá sự cân bằng chính xác giữa kích thước của tệp và chất lượng in của nó.

### Đường cong dạng tự do

Định dạng tệp OBJ cho phép các đường cong bề mặt dạng tự do do người dùng xác định để chỉ định hình dạng bề mặt của mô hình. Vì các đường cong dạng tự do phức tạp hơn các mặt đa giác vì với ít tham số toán học, các đường cong có thể được xác định tốt nhất bằng các đường cong dạng tự do. Do đó, với ít dữ liệu hơn so với các dải ô đa giác, các đường cong dạng tự do được sử dụng để tạo mã hóa chất lượng cao cho bất kỳ mô hình 3D nào mà không cần mở rộng kích thước tệp.

### Bề mặt dạng tự do

Định dạng tệp OBJ cũng chỉ định việc ốp lát hình học bề mặt với các mảng bề mặt dạng tự do. Loại miếng vá bề mặt dạng tự do (NURBS) này rất phù hợp với các bề mặt không có kích thước xuyên tâm cứng như thân xe tải, cánh máy bay trực thăng hoặc thân tàu. Việc sử dụng các bề mặt dạng tự do rất thuận lợi vì chúng chính xác hơn để giữ cho kích thước tệp nhỏ hơn với độ chính xác cao hơn. Những bề mặt này là một phần thiết yếu của ngành hàng không vũ trụ và ô tô, nơi độ chính xác thấp là không thể chấp nhận được.

Các từ khóa sau được sắp xếp theo loại dữ liệu để xác định hình học bề mặt.


|Các phần tử|Các câu lệnh về bề mặt/đường cong dạng tự do|Các thuộc tính của bề mặt/đường cong dạng tự do
---|---|---|
|p|Điểm|parm|Giá trị tham số|deg|Độ
|l|Line|trim|Vòng cắt ngoài|bmat|Ma trận cơ sở
|f|Mặt|lỗ|Vòng cắt bên trong|bước|Cỡ bước
|curv|Curve|scrv|Đường cong đặc biệt|cstype|Loại đường cong hoặc bề mặt
|curv2|Đường cong 2D|sp|Điểm đặc biệt|**Kết nối và nhóm các bề mặt**
|surf|Bề mặt|kết thúc|Kết thúc tuyên bố|con|kết nối
|**Hiển thị/kết xuất thuộc tính**|g|Tên nhóm
|bevel|Nội suy vát|shadow_obj|Đúc bóng|s|Nhóm làm mịn
|lod|Mức độ chi tiết|trace_obj|Dò tia|mg|Nhóm hợp nhất
|d_interp|Nội suy giải tan|ctech|Kỹ thuật xấp xỉ đường cong|o|Tên đối tượng
|c_interp|Nội suy màu|stech|Kỹ thuật xấp xỉ bề mặt|
|usemtl|Tên tài liệu|mtllib|Thư viện tài liệu|
|**Các đỉnh hình học**|
|v|Đỉnh hình học|vn|Pháp tuyến của đỉnh|
|vt|Các đỉnh kết cấu|vp|Các đỉnh không gian tham số|

### Màu sắc và Kết cấu

Tệp OBJ cho phép lưu trữ thông tin về màu sắc và kết cấu ở định dạng tệp được liên kết có tên là Thư viện mẫu vật liệu (MTL). Các mô hình hình học nhiều màu kết xuất bằng cách sử dụng hai tệp này cùng nhau. Các tệp MTL dựa trên ASCII và hỗ trợ hiển thị trên máy tính bằng cách mô tả các đặc tính phản xạ ánh sáng của bề mặt bằng mô hình phản xạ Phong. Tiêu chuẩn đã được chấp nhận bởi một số lượng lớn các nhà cung cấp phần mềm, những người tận dụng lợi thế của nó để trao đổi tài liệu. Định dạng MTL hơi lỗi thời do không có hỗ trợ trong các công nghệ mới nhất như bản đồ phản chiếu và thị sai.

## Người giới thiệu

* [Tệp .obj của Wavefront](https://vi.wikipedia.org/wiki/Wavefront_.obj_file)

