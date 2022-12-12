{
  "date" : "2019-10-11",
  "keywords" :[ "tệp psd", "định dạng tệp psd", "tệp psd là gì", "tệp", "ví dụ psd", "phần mở rộng tệp psd","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Định dạng tệp ảnh Photoshop",
  "description":"Tìm hiểu về định dạng tệp PSD và API có thể tạo và mở tệp PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PSD là gì?

PSD, Tài liệu Photoshop, đại diện cho định dạng tệp gốc của Adobe Photoshop được sử dụng để thiết kế và phát triển đồ họa. Các tệp PSD có thể bao gồm các lớp hình ảnh, lớp điều chỉnh, mặt nạ lớp, chú thích, thông tin tệp, từ khóa và các yếu tố cụ thể khác của Photoshop. Các tệp Photoshop có phần mở rộng mặc định là .PSD và có chiều cao và chiều rộng tối đa là 30.000 pixel và giới hạn độ dài là hai gigabyte.

## Thông số định dạng tệp PSD ##

Dữ liệu trong tệp PSD được lưu trữ theo thứ tự byte lớn về cuối. Điều này ngụ ý hoán đổi các số nguyên ngắn và dài khi đọc hoặc viết trên nền tảng Windows. Định dạng tệp Photoshop được chia thành năm phần chính. Nó có nhiều điểm đánh dấu độ dài có thể được sử dụng để di chuyển từ phần này sang phần tiếp theo. Các điểm đánh dấu độ dài thường được đệm bằng byte để làm tròn đến khoảng 2 hoặc 4 byte gần nhất. Năm phần chính là:

* Tiêu đề tệp
* Dữ liệu chế độ màu
* Tài nguyên hình ảnh
* Thông tin lớp và mặt nạ
* Dữ liệu hình ảnh

Để phù hợp, dữ liệu phải được ghi vào tất cả các trường này trong phần, vì Photoshop có thể cố gắng đọc toàn bộ phần. Nó cũng ngụ ý rằng các số 0 được ghi vào các trường bị bỏ qua trong khi ghi vào một tệp. Trường độ dài trong các phần được phân định bằng độ dài nên được sử dụng để quyết định thời điểm ngừng đọc. Trong hầu hết các trường hợp, trường độ dài cho biết số lượng byte, không phải bản ghi, theo sau. Những điểm sau đây cần được ghi nhớ trong khi đọc một tập tin.

* Các giá trị trong cột "Độ dài" trong tất cả các bảng đều tính bằng byte.
* Tất cả các giá trị được định nghĩa là chuỗi Unicode bao gồm:
* Trường có độ dài 4 byte, biểu thị số ký tự trong chuỗi (không phải byte).
* Chuỗi giá trị Unicode, hai byte cho mỗi ký tự.

### Tiêu đề tệp ###

Tiêu đề tệp chứa các thuộc tính cơ bản của hình ảnh.

|Chiều dài|Mô tả
---|---|
|4|Chữ ký: luôn bằng '8BPS' . Đừng cố đọc tệp nếu chữ ký không khớp với giá trị này.
|2|Phiên bản: luôn bằng 1. Đừng cố đọc tệp nếu phiên bản không khớp với giá trị này. (~*~*PSB~*~* phiên bản là 2.)
|6|Reserveed: phải bằng không.
|2|Số lượng kênh trong hình ảnh, bao gồm bất kỳ kênh alpha nào. Phạm vi được hỗ trợ là 1 đến 56.
|4|Chiều cao của hình ảnh tính bằng pixel. Phạm vi được hỗ trợ là 1 đến 30.000.
|4|Chiều rộng của hình ảnh tính bằng pixel. Phạm vi được hỗ trợ là 1 đến 30.000.
|2|Depth: số bit trên mỗi kênh. Các giá trị được hỗ trợ là 1, 8, 16 và 32.
|2|Chế độ màu của tệp. Các giá trị được hỗ trợ là: Bitmap # 0; Thang độ xám #1; Đã lập chỉ mục #2; RGB #3; CMYK #4; Đa kênh #7; Bộ đôi #8; Phòng thí nghiệm #9.

### Phần Dữ liệu Chế độ Màu ###

Phần dữ liệu chế độ màu được cấu trúc như sau:


|Chiều dài|Mô tả
---|---|
|4|Độ dài của dữ liệu Màu sau
|biến|Dữ liệu màu

Dữ liệu chế độ màu chỉ khả dụng cho màu được lập chỉ mục và bộ đôi như được xác định bởi trường chế độ trong phần Tiêu đề tệp. Đối với tất cả các chế độ khác, phần này được biểu thị bằng các giá trị 0 4 byte. Đối với hình ảnh màu được lập chỉ mục, độ dài là 768 và dữ liệu màu chứa bảng màu cho hình ảnh, theo thứ tự không xen kẽ. Đối với hình ảnh Duotone, dữ liệu màu chứa thông số kỹ thuật của bộ đôi (định dạng của nó không được ghi lại). Các ứng dụng khác đọc tệp Photoshop có thể coi hình ảnh bộ đôi là hình ảnh màu xám và chỉ giữ nguyên nội dung của thông tin bộ đôi khi đọc và ghi tệp.

### Phần Tài nguyên Hình ảnh ###

Phần thứ ba của tệp chứa tài nguyên hình ảnh. Nó bắt đầu với một trường độ dài, theo sau là một loạt các khối tài nguyên.


|Chiều dài|Mô tả
---|---|
|4|Độ dài của phần tài nguyên hình ảnh. Chiều dài có thể bằng không.
|Biến|Tài nguyên hình ảnh (Khối tài nguyên hình ảnh)

Tài nguyên hình ảnh được sử dụng để lưu trữ dữ liệu không phải pixel được liên kết với hình ảnh, chẳng hạn như đường dẫn công cụ bút. Chúng được gọi là khối tài nguyên vì chúng chứa dữ liệu được lưu trữ trong tài nguyên của Macintosh trong các phiên bản đầu tiên của Photoshop. Cấu trúc cơ bản của khối tài nguyên hình ảnh như sau:


|Chiều dài|Mô tả
---|---|
|4|Chữ ký: '8BIM'
|2|Số nhận dạng duy nhất cho tài nguyên. ID tài nguyên hình ảnh chứa danh sách ID tài nguyên được Photoshop sử dụng.
|Biến|Tên: Chuỗi Pascal, được đệm để làm cho kích thước bằng nhau (tên null bao gồm hai byte 0)
|4|Kích thước thực của dữ liệu tài nguyên theo sau
|Biến|Dữ liệu tài nguyên, được mô tả trong các phần về các loại tài nguyên riêng lẻ. Nó được đệm để làm cho kích thước đồng đều.

Tài nguyên hình ảnh sử dụng một số số ID tiêu chuẩn.

### Thông tin về Lớp và Mặt nạ ###

Phần thứ tư của tệp Photoshop chứa thông tin về lớp và mặt nạ, chẳng hạn như số lớp, kênh trong lớp, phạm vi hòa trộn, phím lớp điều chỉnh, lớp hiệu ứng và tham số mặt nạ. Nếu không có lớp hoặc mặt nạ nào, phần này được biểu thị bằng trường 4 byte có giá trị bằng không. Cần đặc biệt chú ý đến độ dài của các phần trong khi đọc phần này do các giá trị bằng 0. Việc sắp xếp phần Layer và Mask như sau:


|Chiều dài|Mô tả
---|---|
|4|Độ dài của lớp và phần thông tin mặt nạ. (Độ dài PSB là 8 byte.)
|Biến|Thông tin lớp
|Biến|Thông tin mặt nạ lớp chung
|Biến|Chuỗi khối được gắn thẻ chứa nhiều loại dữ liệu khác nhau.

#### Thông tin lớp ####

Bảng sau đây cho thấy tổ chức cấp cao của thông tin lớp.


|Chiều dài|Mô tả
---|---|
|4|Độ dài của phần thông tin lớp, được làm tròn thành bội số của 2. (Độ dài PSB là 8 byte.)
|2|Số lớp. Nếu đó là số âm, thì giá trị tuyệt đối của nó là số lớp và kênh alpha đầu tiên chứa dữ liệu về độ trong suốt của kết quả được hợp nhất.
|Biến|Thông tin về mỗi lớp. Xem Bản ghi lớp mô tả cấu trúc của thông tin này cho mỗi lớp.
|Biến|Dữ liệu hình ảnh kênh. Chứa một hoặc nhiều bản ghi dữ liệu hình ảnh cho mỗi lớp. Các lớp theo thứ tự như trong thông tin lớp

### Dữ liệu hình ảnh ###

Dữ liệu pixel hình ảnh được chứa trong phần Dữ liệu hình ảnh của tệp. Sắp xếp dữ liệu trong phần Dữ liệu ảnh theo thứ tự phẳng, tức là dữ liệu màu đỏ đầu tiên, sau đó là dữ liệu xanh, v.v. Mỗi mặt phẳng được lưu trữ theo thứ tự dòng quét, không có byte đệm, Phần dữ liệu ảnh được sắp xếp theo định dạng như trong bảng sau.

|Chiều dài|Mô tả
---|---|
|2|Phương pháp nén: *0 = Dữ liệu hình ảnh thô * 1 = RLE nén dữ liệu hình ảnh bắt đầu với số lượng byte cho tất cả các dòng quét (hàng * kênh), với mỗi số lượng được lưu dưới dạng giá trị hai byte. Dữ liệu nén RLE theo sau, với mỗi dòng quét được nén riêng. Nén RLE là cùng một thuật toán nén được sử dụng bởi PackBits thường trình ROM Macintosh và tiêu chuẩn TIFF. *2 = ZIP không có dự đoán *3 = ZIP có dự đoán.
|Biến|Dữ liệu hình ảnh. Thứ tự phẳng = RRR GGG BBB, v.v.

## Người giới thiệu ##

* [Thông số định dạng tệp PSD - Bởi Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Định dạng tệp Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

