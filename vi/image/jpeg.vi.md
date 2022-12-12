{
  "date" : "2019-11-25",
  "keywords" :[ "tệp jpeg", "định dạng tệp jpeg", "tệp jpeg là gì", "tệp", "ví dụ jpeg", "phần mở rộng tệp jpeg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Định dạng tệp hình ảnh",
  "description":"Tìm hiểu về định dạng tệp JPEG và API có thể tạo và mở tệp JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Tệp JPEG là gì? ##

JPEG là một loại định dạng hình ảnh được lưu bằng phương pháp nén mất dữ liệu. Hình ảnh đầu ra, là kết quả của quá trình nén, là sự đánh đổi giữa kích thước bộ nhớ và chất lượng hình ảnh. Người dùng có thể điều chỉnh mức độ nén để đạt được mức chất lượng mong muốn đồng thời giảm kích thước bộ nhớ. Chất lượng hình ảnh bị ảnh hưởng đáng kể nếu nén 10:1 được áp dụng cho hình ảnh. Giá trị nén càng cao, chất lượng hình ảnh càng giảm.

## Thông số kỹ thuật định dạng tệp ##

Định dạng tệp hình ảnh JPEG đã được chuẩn hóa bởi Nhóm chuyên gia chụp ảnh chung và do đó có tên là JPEG. Định dạng này là lựa chọn lưu trữ và truyền ảnh chụp trên web. Hầu như tất cả các Hệ điều hành hiện nay đều có trình xem hỗ trợ trực quan hóa hình ảnh JPEG, thường được lưu trữ với phần mở rộng JPG. Ngay cả các trình duyệt web cũng hỗ trợ hiển thị hình ảnh JPEG. Trước khi đi vào các thông số kỹ thuật của định dạng tệp JPEG, cần phải đề cập đến quy trình tổng thể gồm các bước liên quan đến việc tạo JPEG.

### Các bước nén JPEG ###

**Chuyển đổi:** Hình ảnh màu được chuyển đổi từ RGB thành hình ảnh độ chói/sắc độ (Mắt nhạy cảm với độ chói, không nhạy cảm với sắc độ, do đó phần sắc độ có thể mất nhiều dữ liệu và do đó có thể được nén ở mức độ cao.

**Lấy mẫu xuống:** Lấy mẫu xuống được thực hiện cho thành phần màu chứ không phải cho thành phần độ sáng. Lấy mẫu xuống được thực hiện theo tỷ lệ 2:1 theo chiều ngang và 1:1 theo chiều dọc (2h 1 V). Do đó, hình ảnh giảm kích thước vì thành phần 'y' không được chạm vào, chất lượng hình ảnh không giảm đáng kể.

**Sắp xếp theo nhóm:** Các pixel của từng thành phần màu được sắp xếp theo nhóm 8×2 pixel được gọi là “đơn vị dữ liệu” nếu số hàng hoặc cột không phải là bội số của 8, hàng dưới cùng và cột ngoài cùng bên phải được nhân đôi.

**Biến đổi Cosine rời rạc:** Biến đổi Cosine rời rạc ( DCT) sau đó được áp dụng cho từng đơn vị dữ liệu để tạo bản đồ 8×8 của các thành phần được biến đổi. DCT liên quan đến việc mất một số thông tin do độ chính xác hạn chế của số học máy tính. Điều này có nghĩa là ngay cả khi không có bản đồ, chất lượng hình ảnh sẽ bị giảm một chút nhưng thường là rất nhỏ.

**Lượng tử hóa:** Mỗi thành phần trong số 64 thành phần được biến đổi trong đơn vị dữ liệu được chia cho một số riêng gọi là 'Hệ số lượng tử hóa (QC)', sau đó được làm tròn thành số nguyên. Đây là nơi thông tin bị mất không thể cứu vãn, QC lớn gây ra nhiều tổn thất hơn. Nói chung, hầu hết các công cụ JPEG đều cho phép sử dụng các bảng QC được khuyến nghị bởi tiêu chuẩn JPEG.

**Mã hóa:** 64 hệ số đã biến đổi được lượng tử hóa (Hiện là số nguyên) của mỗi đơn vị dữ liệu được mã hóa bằng cách sử dụng kết hợp mã hóa RLE và Huffman.

**Thêm tiêu đề:** Bước cuối cùng thêm tiêu đề và tất cả các tham số JPEG được sử dụng và xuất kết quả.

Bộ giải mã JPEG sử dụng các bước ngược lại để tạo ảnh gốc từ ảnh nén.

### Cấu trúc tệp ###

Ảnh JPEG được biểu diễn dưới dạng một chuỗi các phân đoạn trong đó mỗi phân đoạn bắt đầu bằng một điểm đánh dấu. Mỗi điểm đánh dấu bắt đầu bằng byte 0xFF theo sau là cờ đánh dấu để biểu thị loại điểm đánh dấu. Tải trọng theo sau bởi điểm đánh dấu là khác nhau tùy theo loại điểm đánh dấu. Các loại điểm đánh dấu JPEG phổ biến được liệt kê dưới đây:

|Tên viết tắt|Byte|Tải trọng|Tên|Nhận xét
---|---|---|---|---|
|SOI|0xFF, 0xD8|không có|Bắt đầu hình ảnh|
|S0F0|0xFF, 0xC0|kích thước thay đổi|Bắt đầu khung hình|
|S0F2|0xFF, 0xC2|kích thước thay đổi|Bắt đầu khung hình|
|DHT|0xFF, 0xC4|kích thước biến|Xác định bảng Huffman|
|DQT|0xFF, 0xDB|kích thước biến|Xác định (các) Bảng lượng tử hóa|
|DRI|0xFF, 0xDD|4 byte|Xác định khoảng thời gian khởi động lại|
|SOS|0xFF, 0xDA|kích thước biến|Bắt đầu quét|
|RSTn|0xFF, 0xD//n//(/vi//n//#0..7)|không có|Khởi động lại|
|APPn|0xFF, 0xE//n//|kích thước biến|Ứng dụng cụ thể|
|COM|0xFF, 0xFE|kích thước thay đổi|Nhận xét|
|EOI|0xFF, 0xD9|không có|Cuối Ảnh|

Trong dữ liệu được mã hóa entropy, sau bất kỳ byte 0xFF nào, bộ mã hóa sẽ chèn một byte 0x00 trước byte tiếp theo, do đó dường như không có điểm đánh dấu ở nơi không có ý định, ngăn lỗi định khung. Bộ giải mã phải bỏ qua byte 0x00 này. Kỹ thuật này, được gọi là [nhồi byte](https://en.wikipedia.org/wiki/Byte_stuffing) (xem phần thông số kỹ thuật JPEG F.1.2.3), chỉ được áp dụng cho dữ liệu được mã hóa entropy, không áp dụng cho dữ liệu tải trọng đánh dấu . Tuy nhiên, hãy lưu ý rằng dữ liệu được mã hóa entropy có một vài điểm đánh dấu của riêng nó; cụ thể là các dấu Đặt lại (0xD0 đến 0xD7), được sử dụng để tách các khối dữ liệu được mã hóa entropy độc lập để cho phép giải mã song song và các bộ mã hóa có thể tự do chèn các dấu Đặt lại này theo các khoảng thời gian đều đặn (mặc dù không phải tất cả các bộ mã hóa đều làm điều này).

