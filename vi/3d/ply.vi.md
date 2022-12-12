{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "file", "extension", "format", "3D file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp PLY và các API có thể tạo và mở tệp PLY.",
  "title" :"PLY - Định dạng tệp 3D đa giác",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PLY là gì?

PLY, Định dạng tệp đa giác, đại diện cho định dạng tệp 3D lưu trữ các đối tượng đồ họa được mô tả dưới dạng tập hợp các đa giác. Mục đích của định dạng tệp này là thiết lập một loại tệp đơn giản và dễ sử dụng, đủ chung để hữu ích cho nhiều loại mô hình. Định dạng tệp PLY có dạng ASCII cũng như định dạng Nhị phân để lưu trữ nhỏ gọn và để lưu và tải nhanh. Định dạng tệp được sử dụng bởi các ứng dụng khác nhau cung cấp hỗ trợ đọc tệp 3D.

Các đối tượng ở định dạng PLY được mô tả bởi một tập hợp các đỉnh, mặt và các phần tử khác, cùng với các thuộc tính như màu sắc và hướng bình thường có thể được gắn vào các phần tử này. Các thuộc tính khác cũng có thể được lưu trữ với đối tượng bao gồm:

* Tiêu chuẩn bề mặt
* tọa độ kết cấu
* minh bạch
* phạm vi dữ liệu tự tin
* thuộc tính cho mặt trước và mặt sau của đa giác

Một đối tượng được biểu thị bằng định dạng PLY có thể là kết quả của nhiều nguồn khác nhau, chẳng hạn như các đối tượng được số hóa bằng tay, các đối tượng đa giác từ các ứng dụng mô hình hóa, dữ liệu phạm vi, hình tam giác từ các khối diễu hành, dữ liệu địa hình và mô hình phóng xạ.

## Tóm tắt lịch sử

Định dạng PLY được phát triển vào những năm 1990 bởi Greg Turk và những người khác trong phòng thí nghiệm đồ họa Stanford và đó là lý do tại sao nó còn được gọi là Định dạng Tam giác Stanford. Định dạng tệp có phiên bản 1.0 kể từ đó và không có thêm sửa đổi nào được thực hiện.

## Định dạng tệp PLY

Một đối tượng PLY đơn giản bao gồm tập hợp các phần tử để biểu diễn đối tượng. Nó bao gồm một danh sách các bộ ba (x,y,z) của một đỉnh và một danh sách các mặt thực sự là chỉ số của danh sách các đỉnh. Đỉnh và mặt là hai ví dụ về các phần tử và phần lớn tệp PLY bao gồm hai phần tử này. Các thuộc tính mới cũng có thể được tạo và gắn vào các phần tử của một đối tượng, nhưng chúng phải được thêm vào sao cho các chương trình cũ không bị hỏng khi gặp các thuộc tính mới này. Các thuộc tính như vậy cũng có thể bị loại bỏ bằng cách đọc các ứng dụng. Hơn nữa, các phần tử mới có thể được tạo và các thuộc tính cũng có thể được xác định bằng phần tử này.

### Cấu trúc tệp

Cấu trúc tệp của định dạng tệp PLY như sau:

|trường
---|
|Tiêu đề tập tin
|Danh sách đỉnh
|Danh sách khuôn mặt
|Danh sách các yếu tố khác

#### Cấu trúc ví dụ

Chúng tôi sẽ sử dụng ví dụ dưới đây trong cuộc thảo luận tiếp theo của chúng tôi cho các phần khác nhau của định dạng tệp PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Tiêu đề tệp

Tiêu đề định dạng tệp PLY bao gồm văn bản ASCII cho cả ASCII cũng như định dạng nhị phân. Phần bắt đầu và kết thúc của phần tiêu đề được xác định bởi các từ khóa tiêu đề lớp và tiêu đề cuối. Phần đầu của tiêu đề có từ ma thuật ply được người đọc sử dụng để nhận dạng định dạng tệp PLY. Dòng tiếp theo hiển thị số phiên bản cho tệp này. Nhận xét ở định dạng tệp PLY bắt đầu bằng từ khóa nhận xét ở đầu mỗi dòng nhận xét.

#### Từ khóa phần tử

Sau đó, từ khóa phần tử cho biết nội dung bên trong tệp. Tiếp theo là các thuộc tính cho loại phần tử cụ thể đó, trong đó mỗi thuộc tính có loại và thứ tự thuộc tính được chỉ định như hình bên dưới:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Trong ví dụ cụ thể này, phần tử đỉnh cụ thể có 3 thuộc tính kiểu float với thứ tự được chỉ định.

#### Các kiểu Kiểu dữ liệu

Có hai loại kiểu dữ liệu mà một thuộc tính có thể có.

`Scalar`: Các kiểu dữ liệu vô hướng như hình bên dưới:

|#Tên|#Loại|#Số byte
|ký tự|ký tự|1
|uchar|ký tự không dấu|1
|ngắn|số nguyên ngắn|2
|ushort|số nguyên ngắn không dấu|2
|int|Số nguyên|4
|uint|Số nguyên không dấu|4
|phao|phao chính xác đơn|4
|double|phao chính xác kép|8

`Danh sách`: Có một dạng định nghĩa thuộc tính đặc biệt sử dụng kiểu dữ liệu danh sách. Một ví dụ về điều này là từ tệp khối ở trên:

`danh sách thuộc tính uchar int vertex_index`

Điều này có nghĩa là thuộc tính "vertex_index" trước tiên chứa một ký tự không dấu cho biết thuộc tính chứa bao nhiêu chỉ số, tiếp theo là một danh sách chứa nhiều số nguyên đó. Mỗi số nguyên trong danh sách có độ dài thay đổi này là chỉ số của một đỉnh.

## Người giới thiệu ##

* [Định dạng tệp PLY](http://paulbourke.net/dataformats/ply/)
* [PLY - Theo Wikipedia](https://vi.wikipedia.org/wiki/PLY_(file_format))

