
{
  "date": "2023-01-05",
  "keywords": [
"tập tin pov",
"định dạng tập tin pov",
"tập tin pov là gì",
"tài liệu",
"ví dụ về pov",
"phần mở rộng tập tin pov",
"sự mở rộng",
"định dạng"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Tìm hiểu về định dạng tệp POV và các API có thể mở và tạo tệp POV.",
  "title": "POV - Sự kiên trì của tệp Vision",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-viv"
}
},
  "lastmod": "2023-01-05"
}

## Tập tin POV là gì?

Tệp POV là một tệp văn bản thuần túy chứa các hướng dẫn dành cho phần mềm dò tia POV-Ray. Các hướng dẫn này được viết bằng ngôn ngữ kịch bản đặc biệt dành riêng cho POV-Ray. Nó chỉ định cảnh sẽ được hiển thị, bao gồm các đối tượng 3D, vật liệu, ánh sáng và các thuộc tính khác xác định diện mạo của cảnh. Các tệp POV sử dụng ngôn ngữ kịch bản đặc biệt dành riêng cho POV-Ray và có thể được sử dụng để tạo các cảnh 3D phức tạp và chi tiết. Phần mở rộng tệp cho tệp POV thường là .pov hoặc .povray. Khi bạn mở tệp POV trong POV-Ray, phần mềm sẽ đọc hướng dẫn trong tệp và sử dụng chúng để tạo hình ảnh được hiển thị của cảnh.

Các tệp .pov thường được các nghệ sĩ và nhà thiết kế sử dụng để tạo đồ họa và hoạt hình 3D cho nhiều ứng dụng, bao gồm phim, truyền hình, trò chơi điện tử và tài liệu tiếp thị.

## Định dạng tệp POV

Tệp **.pov** thường bắt đầu bằng một loạt câu lệnh **#include**, được sử dụng để bao gồm các thư viện có màu sắc, họa tiết được xác định trước và các tài nguyên khác có thể được sử dụng trong cảnh. Sau đó, tệp xác định các đối tượng, vật liệu và các thuộc tính khác của cảnh bằng cách sử dụng một loạt khối. Có nhiều loại đối tượng, vật liệu và thuộc tính khác mà bạn có thể chỉ định trong tệp .pov, đồng thời bạn có thể sử dụng vòng lặp và câu lệnh điều kiện để tạo các cảnh phức tạp và chi tiết hơn.

## Ứng dụng phần mềm cho POV

Định dạng tệp .pov được sử dụng bởi phần mềm dò tia POV-Ray, vì vậy ứng dụng chính để mở tệp .pov chính là phần mềm POV-Ray. Bạn có thể tải xuống phiên bản mới nhất của POV-Ray từ trang web chính thức tại https://www.povray.org/.

Ngoài POV-Ray, còn có một số ứng dụng khác có thể mở và chỉnh sửa file .pov, bao gồm:

- BRL-CAD: Phần mềm tạo mô hình 3D mã nguồn mở có thể nhập và xuất tệp .pov
- MeshLab: Phần mềm xử lý lưới 3D có thể nhập và xuất tệp .pov
- Blender: Một phần mềm đồ họa 3D mã nguồn mở phổ biến có thể nhập và xuất các tệp .pov

Có thể có các ứng dụng phần mềm khác cũng có thể mở tệp .pov, vì vậy bạn có thể thử sử dụng trình xem tệp hoặc công cụ chuyển đổi nếu bạn không thể mở tệp .pov bằng các ứng dụng trên.

## Ví dụ về POV

Ví dụ: đây là tệp .pov mẫu xác định một cảnh có một hình trụ màu xanh lam:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Trong ví dụ này, khối camera chỉ định vị trí và hướng của camera trong cảnh, khối `light_source` khai báo nguồn sáng và chỉ định vị trí cũng như màu sắc của nó, và khối `xi lanh` khai báo một đối tượng hình trụ và chỉ định các điểm cuối của nó, bán kính và tính chất vật liệu. Khi bạn mở tệp .pov này trong phần mềm POV-Ray, nó sẽ hiển thị hình ảnh của một hình trụ màu xanh lam.

## Người giới thiệu
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Trang web tài liệu POV-Ray](http://www.povray.org/documentation/)

