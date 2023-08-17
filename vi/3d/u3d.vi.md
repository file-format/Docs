{
  "date" : "2019-10-11",
  "keywords" :[ "tệp u3d", "định dạng tệp u3d", "tệp u3d là gì", "tệp", "ví dụ u3d", "phần mở rộng tệp u3d","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Định dạng tệp 3D phổ quát",
  "description":"Tìm hiểu về định dạng tệp U3D và các API có thể mở và tạo tệp U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp U3D là gì?

**U3D** (3D phổ quát) là định dạng tệp nén và cấu trúc dữ liệu dành cho đồ họa máy tính 3D. Nó chứa thông tin mô hình 3D như lưới tam giác, ánh sáng, bóng đổ, dữ liệu chuyển động, đường và điểm có màu sắc và cấu trúc. Định dạng được chấp nhận là tiêu chuẩn [ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) vào tháng 8 năm 2005. Tài liệu 3D [PDF](/vi/pdf/) hỗ trợ U3D các đối tượng nhúng và có thể được xem trong Adobe Reader (phiên bản 7 trở đi).

Định dạng U3D được phát triển nhằm mục đích thiết lập một tiêu chuẩn chung cho việc lưu trữ và trao đổi dữ liệu ba chiều. Tuy nhiên, định dạng được sử dụng chính trong mã hóa cho PDF 3D thay vì được sử dụng làm định dạng trao đổi. Acrobat 3D chuyển đổi loại tệp 3D được hỗ trợ thành U3D hoặc PRC khi chuyển đổi thành PDF.

## Định dạng tệp U3D

Các tệp U3D ở định dạng tệp nhị phân đã trải qua bốn phiên bản như được mô tả trong tài liệu tham khảo [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/), dẫn đến cập nhật thông số kỹ thuật với mỗi ấn bản. Tiêu chuẩn tệp PDF ISO-32000 chấp nhận U3D là loại chú thích và đa phương tiện được phép.

Phiên bản đầu tiên của U3D tập trung vào các biểu diễn chính của các thuộc tính đồ họa 3D như hình học, màu sắc, kết cấu, ánh sáng, xương và hoạt hình dựa trên biến đổi. Ấn bản thứ hai và thứ ba đã sửa một số lỗi trong ấn bản đầu tiên, với phiên bản thứ ba là loại được sử dụng phổ biến nhất trong phần mềm công nghiệp. Phiên bản thứ tư cung cấp các định nghĩa cho các nguyên hàm bậc cao hơn (các mặt cong). [Thông số kỹ thuật của U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) có sẵn trực tuyến để người dùng tham khảo trên trang web ECMA.

### Các loại dữ liệu trong tệp U3D

Tệp nhị phân sẽ chứa các loại sau: U8, U16, U32, U64, I16, I32, F32, F64 và String.

* U8 : Số nguyên 8 bit không dấu
* U16 : Số nguyên 16 bit không dấu
* U32 : Một số nguyên 32 bit không dấu
* U64 : Số nguyên 64 bit không dấu
* I16 : Số nguyên 16 bit có dấu
* F32: Một phao chính xác đơn của IEEE.
* F64: Một phao chính xác kép của IEEE.
* Chuỗi: Các chuỗi trong tệp U3D bắt đầu bằng một số nguyên 16 bit không dấu xác định tổng độ dài của các ký tự trong chuỗi. Các chuỗi luôn được xử lý phân biệt chữ hoa chữ thường.

## Cấu trúc tệp U3D

Tệp U3D chứa một chuỗi các khối. Có 3 loại khối khác nhau trong mỗi tệp U3D.

* Khối tiêu đề tệp
* Khối khai báo
* Khối tiếp tục

Trình tải xác định phần cuối của một khối nếu dữ liệu trong khối đó không cần thiết hoặc nếu không có bộ giải mã cho loại khối đó.

{{< figure src="../u3d.png" alt="Định dạng tệp U3D" >}}

### Khối tiêu đề tệp
Khối tiêu đề tệp chứa thông tin tệp được tải để xác định cách đọc tệp.

### Khối khai báo

Các khối khai báo chứa thông tin về các đối tượng trong tệp. Các đối tượng trong một khối khai báo phải được xác định.

### Khối tiếp tục

Thông tin bổ sung cho các đối tượng được khai báo trong khối Khai báo được cung cấp trong khối tiếp tục. Mỗi Khối tiếp tục phải được liên kết với một Khối khai báo.


## Người giới thiệu ##

* [Định dạng tệp U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Thông số kỹ thuật định dạng tệp ECMA U3D](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

