{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Định dạng tệp", "Mở", "Đọc", "Tạo", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DWF và API có thể tạo và mở tệp DWF.",
  "title" :"Định dạng tệp DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp DWF là gì?

Định dạng Web Thiết kế (DWF) thể hiện bản vẽ 2D/3D ở định dạng nén để xem, đánh giá hoặc in các tệp thiết kế. Nó chứa đồ họa và văn bản như một phần của dữ liệu thiết kế và giảm kích thước của tệp do định dạng nén của nó. Kích thước tệp giảm làm cho việc phân phối và truyền dữ liệu thiết kế phong phú trở nên hiệu quả. DWF không yêu cầu người nhận biết về việc sử dụng phần mềm CAD đã tạo bản vẽ gốc. Nội dung của định dạng tệp DWF có thể đơn giản và chỉ bao gồm một trang tính hoặc đủ phức tạp để có phông chữ, màu sắc và hình ảnh.

## Lược Sử ##

Autodesk đã giới thiệu định dạng tệp DWF vào năm 1995 như một phần của trình cắm Điều hướng Netscape, WHIP. Định dạng đã phát triển từ định dạng chỉ 2D để bao gồm nội dung 3D theo thời gian. Nhiều ứng dụng của bên thứ ba cũng sử dụng định dạng này.

## Định dạng tệp DWF ##

DWF là một định dạng mở, an toàn được thiết kế đặc biệt để chia sẻ dữ liệu thiết kế kỹ thuật phong phú. Nó độc lập với phần mềm ứng dụng, phần cứng và hệ điều hành ban đầu được sử dụng để tạo dữ liệu thiết kế đó. Điều này cho phép các thành viên trong nhóm không sử dụng các ứng dụng CAD tham gia vào các quy trình kỹ thuật số bằng cách xem các thiết kế tòa nhà, GIS hoặc sản phẩm. Một kho lưu trữ tệp DWF bao gồm một số tệp XML và tệp nhị phân được đóng gói cùng nhau trong một kho lưu trữ nén được tạo bằng nén [ZIP](/vi/compression/zip/). Bạn có thể đổi tên phần mở rộng tệp DWF thành ZIP và xem nội dung của tệp. Gói DWF có thể chứa nhiều loại dữ liệu thiết kế như đồ họa 2D, đồ họa 3D, siêu dữ liệu gói và phần cũng như các tệp tài nguyên khác.

**Tệp siêu dữ liệu DWF** – Tệp XML chứa thông tin liên quan đến siêu dữ liệu và cấu trúc (tác giả, tiêu đề, thời gian tạo, phần phụ thuộc, thứ tự phần, mô tả tệp tài nguyên, vai trò, kiểu bắt chước, v.v.) và liên quan đến phần (trang thông tin, siêu dữ liệu thiết kế, v.v.). Siêu dữ liệu cấu trúc được sử dụng để tạo các đối tượng logic (tập hợp các tệp để biểu thị một phần hoặc trang, v.v.).

**Tệp tài nguyên** – tệp phương tiện hoặc tệp nội dung khác được tham chiếu từ siêu dữ liệu gói/phần và thường là bản trình bày dữ liệu thiết kế ở các định dạng khác nhau (ZGL, W2D, [JPG](/vi/image/jpeg/), [PNG] (/vi/image/png/), AVI, XML, [TXT](/vi/word-processing/txt/), [DOC](/vi/word-processing/doc/), v.v.)

### Chi tiết định dạng tệp ###

Các tệp DWF được tổ chức thành ba phần chính như hình bên dưới.

* Tiêu đề nhận dạng tệp
* Tệp dữ liệu khối
* Đoạn giới thiệu chấm dứt tập tin

#### Tiêu đề định danh tệp ####

Tiêu đề định danh tệp cho phép nhận dạng các tệp DWF theo ứng dụng. Nó cũng xác định phiên bản thông số kỹ thuật DWF nào được sử dụng để mã hóa tệp. Đó là một tiêu đề 12 byte được sắp xếp như sau:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Nhân vật|(|D|W|F|(dấu cách)|V|0|0|.|3|0|)

Dưới đây là một bản tóm tắt của bảng này:

* Sáu byte đầu tiên của tiêu đề luôn đại diện cho các ký tự ASCII "(DWF V"
* 5 byte sau chứa thông tin về số phiên bản, ví dụ: "00.30" với giá trị phiên bản chính và phụ của định dạng

Các ứng dụng tạo tệp DWF phải chỉ định số phiên bản thấp nhất có thể mà ứng dụng trình đọc cần hỗ trợ để sử dụng dữ liệu đúng cách.

#### Khối dữ liệu tệp ####

Khối dữ liệu tệp bắt đầu ở byte thứ 13 của tệp DWF và là một chuỗi các cặp opcode và toán hạng, như trong bảng sau.

|Trường 1|Trường 2|Trường 3|Trường 4|Trường 5|Trường 5
--- | --- |--- | --- |--- | --- |
|opcode|toán hạng|opcode|toán hạng|opcode|toán hạng

Tệp DWF có thể chứa các cặp opcode-toán hạng dưới dạng ASCII có thể đọc được cũng như mã nhị phân hoặc kết hợp cả hai. Tất cả các thao tác DWF đều có dạng opcode/toán hạng ASCII có thể đọc được và hầu hết các thao tác cũng có dạng opcode/toán hạng nhị phân được mã hóa. Các mã hoạt động ở dạng byte đơn cho phép thực hiện hơn 200 thao tác. ASCII mở rộng và nhị phân mở rộng là những trường hợp ngoại lệ. Các giá trị của Opcodes có thể nằm trong khoảng từ 0-255 với một số trường hợp ngoại lệ. Ngoại trừ hai loại opcode đặc biệt ASCII mở rộng và mã nhị phân mở rộng, trình đọc tệp phải biết cách tính độ dài toán hạng.

##### Mã bị cấm #####

Các biểu diễn ASCII cho những điều sau đây không thể được sử dụng làm opcodes:

Không thể sử dụng các biểu diễn ASCII sau đây làm opcodes:

* Không gian (0x20)
* Thẻ (0x09)
* Dấu gạch nối (0x2D)
* Chữ số ASCII 0-9 (0x30 - 0x39)
* Vận chuyển trở lại (0x0D)
* Nguồn cấp dữ liệu (0x0A)
* Dấu nháy đơn (0x27)
* Dấu ngoặc kép (0x22)
* Khoảng thời gian (0x2E)
* Dấu ngoặc đơn (0x28 và 0x29)
* Dấu ngoặc nhọn (0x7B và 0x7D)
* Dấu ngoặc vuông (0x5B và 0x5D)
* Dấu gạch chéo ngược (0x5C)

#### Đoạn giới thiệu kết thúc tệp ####

Đoạn giới thiệu kết thúc tệp cho DWF chỉ đơn giản là một mã hành động đặc biệt cho biết phần cuối của tệp. Một số ứng dụng có thể lưu trữ dữ liệu không phải DWF sau opcode kết thúc. Đoạn giới thiệu như bên dưới:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Nhân vật|(|E|n|d|0|f|D|W|F|)

## Người giới thiệu ##

* [DWF - Theo Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Định dạng dữ liệu WHIP](http://paulbourke.net/dataformats/whip/)
* [http://blogs.msdn.com/opc/archive/2009/05/18/adventures-in-packaging-episode-1.aspx](http://blogs.msdn.com/opc/archive/2009 /05/18/adventures-in-packaging-episode-1.aspx)

