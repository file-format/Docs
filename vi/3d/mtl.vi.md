{
"date" :  "2023-10-11",
   "keywords":[
"mtl",
"tập tin mtl",
"tệp thư viện mẫu tài liệu mtl obj",
"cách mở tập tin mtl",
"tài liệu",
"phần mở rộng tập tin mtl",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Định dạng tệp MTL - Tệp thư viện mẫu tài liệu OBJ",
   "description":"Tìm hiểu về định dạng tệp Thư viện mẫu vật liệu MTL OBJ và các API có thể tạo và mở tệp MTL.",
"linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Tập tin MTL là gì?

Tệp MTL, viết tắt của **Thư viện mẫu vật liệu**, là định dạng tệp đồng hành được sử dụng trong mô hình và đồ họa máy tính 3D. Nó thường được liên kết với **Định dạng tệp OBJ Wavefront**, đây là định dạng phổ biến để lưu trữ mô hình 3D cũng như các vật liệu và kết cấu liên quan của chúng.

## Thư viện mẫu vật liệu

Đây là thông tin quan trọng về các tệp MTL:

1. **Định nghĩa vật liệu**: Tệp ".mtl" chứa các định nghĩa về vật liệu được áp dụng cho đối tượng 3D trong tệp OBJ tương ứng. Mỗi định nghĩa vật liệu chỉ định các thuộc tính khác nhau, chẳng hạn như bản đồ màu sắc, độ bóng, độ trong suốt và kết cấu.
    





2. **Định dạng dựa trên văn bản**: Tệp ".mtl" thường là tệp văn bản thuần túy, nghĩa là chúng có thể dễ dàng chỉnh sửa bằng trình soạn thảo văn bản. Mỗi định nghĩa vật liệu bao gồm một tập hợp các câu lệnh và những câu lệnh này xác định các thuộc tính của vật liệu.
    





3. **Ánh xạ họa tiết**: Một trong những chức năng thiết yếu của tệp ".mtl" là xác định cách ánh xạ họa tiết (tệp hình ảnh) lên bề mặt của mô hình 3D. Nó chỉ định đường dẫn của tệp kết cấu và cách gói hoặc áp dụng nó cho mô hình.
    





4. **Ví dụ về câu lệnh MTL**: Dưới đây là một số câu lệnh ví dụ mà bạn có thể tìm thấy trong tệp ".mtl":
    





- `newmtl MaterialName`: Điều này xác định vật liệu mới có tên "MaterialName."
- `Ka rgb`: Màu xung quanh của vật liệu, được chỉ định bằng giá trị RGB.
- `Kd rgb`: Màu khuếch tán của vật liệu, được chỉ định bằng giá trị RGB.
- `Ks rgb`: Màu đặc trưng của vật liệu, được xác định bằng giá trị RGB.
- `Giá trị Ns`: Độ bóng hoặc số mũ đặc trưng của vật liệu.
- `map_Kd textfile.jpg`: Chỉ định bản đồ kết cấu khuếch tán cho vật liệu.
5. **Nhiều tài liệu**: Một tệp OBJ có thể tham chiếu nhiều tài liệu và mỗi tài liệu được xác định trong tệp ".mtl". Điều này cho phép tạo ra các mô hình 3D phức tạp với các vật liệu khác nhau được áp dụng cho các bộ phận khác nhau.
    





6. **Khả năng tương thích**: Tệp ".mtl" được hỗ trợ rộng rãi bởi phần mềm tạo mô hình 3D và công cụ kết xuất, giúp chuyển mô hình 3D và tài liệu của chúng giữa các ứng dụng phần mềm khác nhau.

## Làm cách nào để mở tệp MTL?

Tệp MTL là các tệp dựa trên văn bản, vì vậy chúng có thể được mở bằng bất kỳ trình soạn thảo văn bản nào, bao gồm cả

- Sổ tay (Windows)
- Notepad++ (Windows)
- Mã Visual Studio
- Văn bản tuyệt vời
- Nguyên tử
- Chỉnh sửa văn bản (macOS)

Các chương trình mở hoặc tham chiếu tệp MTL bao gồm

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

**SubType:** Tệp hình ảnh 3D

## Người giới thiệu
* [Tệp Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

