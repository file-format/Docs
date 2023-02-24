{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","tệp", "định dạng", "loại tệp", "phần mở rộng","tệp 3DS là gì?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp 3DS và các API có thể mở và tạo tệp 3DS.",
  "title" :"Định dạng tệp 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tập tin 3DS là gì?

Tệp có phần mở rộng .3ds đại diện cho định dạng tệp lưới 3D Sudio (DOS) được Autodesk 3D Studio sử dụng. Autodesk 3D Studio đã có mặt trên thị trường định dạng tệp 3D từ những năm 1990 và hiện đã phát triển thành 3D Studio MAX để làm việc với mô hình, hoạt hình và kết xuất 3D. Tệp 3DS chứa dữ liệu để thể hiện cảnh và hình ảnh 3D và là một trong những định dạng tệp phổ biến để nhập và xuất dữ liệu 3D. Nó xem xét thông tin như vị trí camera, dữ liệu Lưới, thông tin ánh sáng, cấu hình khung nhìn, dữ liệu nhóm làm mịn, tham chiếu bitmap và thuộc tính để tạo đỉnh và đa giác để hiển thị cảnh.

## Định dạng tệp 3DS - Thông tin khác
Về cơ bản, 3DS là định dạng tệp nhị phân và tuân theo cấu trúc được xác định trước để lưu trữ và truy xuất dữ liệu. Định dạng tệp nhị phân cho phép định dạng tệp 3DS nhỏ hơn nhanh hơn so với các định dạng tệp dựa trên văn bản. Dữ liệu bên trong tệp 3DS được lưu trữ ở dạng khối.

### Đoạn 3DS

Mỗi đoạn trong tệp 3DS là một khối dữ liệu chứa ID, độ dài của khối cho vị trí của khối tiếp theo và chính dữ liệu đó. ID khối cho phép trình đọc định dạng tệp 3DS bỏ qua các khối mà chúng không nhận ra. Nó cũng giúp mở rộng định dạng. Mỗi đoạn lưu trữ thông tin liên quan đến hình dạng, ánh sáng và thông tin xem cùng nhau hiển thị cảnh. Các khối được sắp xếp theo cấu trúc phân cấp trong tệp 3DS và giống với biểu diễn cây Đối tượng Tài liệu XML.

**ID đoạn:** Hai byte đầu tiên của một đoạn đại diện cho một mã định danh đoạn cho phép trình đọc tệp quyết định xem xét nó trong khi đọc hay bỏ qua nó.

**Độ dài của đoạn:** ID đoạn được theo sau bởi một số nguyên 4 byte (bằng little-endian) đại diện cho độ dài của đoạn. Độ dài này cũng bao gồm độ dài của dữ liệu, độ dài của các khối con của nó và tiêu đề 6 byte.

**Tải trọng:** Độ dài của đoạn được theo sau bởi các byte dữ liệu thực tế cho đoạn, theo sau là các đoạn con của nó trong cùng một cấu trúc phân cấp có thể được mở rộng sâu đến nhiều cấp độ.

### Cấu trúc của một Chunk

Cấu trúc phân cấp của một chunk đơn giản như hình dưới đây:

**Một đoạn**

|bắt đầu|kết thúc|kích thước|tên
--- | --- | --- | ---
|0|1|2|ID Đoạn
|2|5|4|Đoạn tiếp theo

Các khối có một hệ thống phân cấp áp đặt cho chúng được xác định bằng ID của nó. Tệp 3ds có ID đoạn chính 4D4Dh. Đây luôn là đoạn đầu tiên của tệp. Với trong đoạn chính là các đoạn chính.

** Phần chính **

|id|Mô tả
--- | ---
|3D3D|Bắt đầu dữ liệu lưới đối tượng.
|B000|Bắt đầu dữ liệu khung hình chính.

Con trỏ Đoạn tiếp theo sau khối ID trỏ đến đoạn Chính tiếp theo.
Ngay sau một đoạn chính là một đoạn khác. Đây có thể là bất kỳ loại khối nào khác được phép trong phạm vi khối chính của nó.
Đối với mô tả Lưới (3D3D), chúng có thể là bội số bất kỳ của.

**Nhóm con của 3D3D - Khối lưới**


|id|Mô tả
--- | ---
|1100|không rõ
|1200|Màu nền.
|1201|không rõ
|1300|không rõ
|1400|không rõ
|1420|không rõ
|1450|không rõ
|1500|không rõ
|2100|Khối màu xung quanh
|2200|sương mù?
|2201|sương mù?
|2210|sương mù?
|2300|không rõ
|3000|không xác định
|4000|Khối đối tượng
|7001|không xác định
|AFFF|không xác định

**Chuỗi con của 4000 - Khối mô tả đối tượng**
Mục đầu tiên của Subchunk 4000 là một chuỗi ASCIIZ của tên đối tượng.
Hãy nhớ rằng một đối tượng có thể là lưới, đèn hoặc máy ảnh.

|id|Mô tả
--- | ---
|4010|không xác định
|4012|bóng?
|4100|Đối tượng đa giác tam giác
|4600|Ánh sáng
|4700|Máy ảnh

## Người giới thiệu

* [Định dạng tệp hình học - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32-htm.html)
* [3DS - Theo Wikipedia](https://vi.wikipedia.org/wiki/.3ds)
