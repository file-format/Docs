{
  "date" : "2020-03-16",
  "keywords" :[ "Tệp STL", "Định dạng", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp STL và API có thể tạo và mở tệp STL.",
  "title" :"Định dạng tệp STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Tập tin STL là gì?

STL, viết tắt của stereolithrography, là một định dạng tệp có thể hoán đổi cho nhau, đại diện cho hình học bề mặt 3 chiều. Định dạng tệp được sử dụng trong một số lĩnh vực như tạo mẫu nhanh, in 3D và sản xuất có sự trợ giúp của máy tính. Nó đại diện cho một bề mặt dưới dạng một loạt các tam giác nhỏ, được gọi là các mặt, trong đó mỗi mặt được mô tả bằng một hướng vuông góc và ba điểm đại diện cho các đỉnh của tam giác. Dữ liệu kết quả được các ứng dụng sử dụng để xác định mặt cắt ngang của hình dạng 3D được tạo bởi fabber. Không có sẵn thông tin ở định dạng tệp STL để thể hiện màu sắc, kết cấu hoặc các thuộc tính mô hình [CAD](/vi/cad/) phổ biến khác.

## Lược Sử ##

Sự phát triển của định dạng tệp STL bắt đầu từ năm 1987. Định dạng này được phát triển bởi 3D Systems để sử dụng trong các máy in 3D thương mại. Phiên bản sửa đổi của định dạng tệp STL, được gọi là STL 2.0, đã được đề xuất vào năm 2009 với các bản cập nhật cho định dạng tệp.

## Thông số kỹ thuật định dạng tệp ##

Tệp STL biểu thị hình dạng bề mặt bằng cách sử dụng các mặt. Các mặt xác định bề mặt của đối tượng 3D và được xác định duy nhất bởi một đơn vị bình thường, là một đường vuông góc với tam giác có chiều dài 1,0 và bởi ba đỉnh. Có tổng cộng 12 số được lưu trữ cho mỗi khía cạnh dưới dạng Bình thường và mỗi đỉnh được chỉ định bởi ba tọa độ mỗi cạnh. Tệp StL không chứa bất kỳ thông tin tỷ lệ nào; các tọa độ là trong các đơn vị tùy ý.

Các thông số kỹ thuật của định dạng tệp STL có thể được kiểm tra từ hai khía cạnh sau.

### Định hướng các khía cạnh ###

Hướng của một mặt được xác định theo hướng của pháp tuyến đơn vị và thứ tự liệt kê các đỉnh. Hướng của các mặt được chỉ định theo hai cách như sau:

* Hướng của pháp tuyến là hướng ra ngoài
* Các đỉnh được liệt kê theo thứ tự ngược chiều kim đồng hồ từ ngoài vào, tuân theo quy tắc bàn tay phải.

### Quy tắc đỉnh tới đỉnh ###

Theo quy tắc này, mỗi tam giác chia sẻ hai đỉnh với mỗi tam giác liền kề của nó. Như vậy, một đỉnh của tam giác này không thể nằm trên cạnh của tam giác kia.

## Định dạng tệp ##

STL có sẵn trong ASCII cũng như các biểu diễn nhị phân cho định dạng tệp nhỏ gọn.

### Định dạng STL ASCII ###

Phiên bản ASCII của định dạng tệp STL được viết bằng ASCII thuần túy. Tuy nhiên, do kích thước lớn, định dạng tệp không được chọn là định dạng thích hợp hơn để sử dụng. Cú pháp của tệp ASCII STL như sau:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Các từ in đậm đại diện cho các từ khóa phải luôn được viết thường. Các ký hiệu in nghiêng là các biến sẽ được thay thế bằng các giá trị do người dùng chỉ định. Dữ liệu số trong các dòng **facet normal** và **vertex** là số float có độ chính xác đơn, ví dụ: 1.23456E+789. Một tọa độ **facet normal** có thể có một dấu trừ phía trước; tọa độ **đỉnh** có thể không.

### Định dạng nhị phân STL ###

Định dạng nhị phân sử dụng biểu diễn số nguyên và dấu phẩy động của IEEE. Định dạng tệp được biểu diễn như sau:

|Trường|Thông tin|
---|---|
|Tiêu đề|80 ký tự|
|Số tam giác|Số nguyên không dấu endian nhỏ 4 byte|
|Dữ liệu cho mỗi tam giác|12 số dấu phẩy động 32 bit|

Một cái nhìn chi tiết hơn về định dạng tệp được hiển thị bên dưới.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Người giới thiệu ##

* [Định dạng STL](http://www.fabbers.com/tech/STL_Format)
* [STL - theo Wikipedia](https://vi.wikipedia.org/wiki/STL_(file_format))

