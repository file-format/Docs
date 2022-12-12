{
  "date" : "2019-10-11",
  "keywords" :[ "tệp gif", "định dạng tệp gif", "tệp gif là gì", "tệp", "ví dụ gif", "phần mở rộng tệp gif","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Định dạng tệp hình ảnh",
  "description":"Tìm hiểu về định dạng tệp GIF và API có thể tạo và mở tệp GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp GIF là gì? ##

GIF hoặc Định dạng trao đổi đồ họa là một loại hình ảnh được nén cao. Thuộc sở hữu của Unisys, GIF sử dụng thuật toán nén LZW không làm giảm chất lượng hình ảnh. Đối với mỗi hình ảnh, GIF thường cho phép tối đa 8 bit trên mỗi pixel và tối đa 256 màu được phép trên hình ảnh. Trái ngược với hình ảnh [JPEG](/vi/image/jpeg/), có thể hiển thị tới 16 triệu màu và khá gần với giới hạn của mắt người. Quay lại thời điểm internet xuất hiện, GIF vẫn là lựa chọn tốt nhất vì chúng yêu cầu băng thông thấp và tương thích với đồ họa sử dụng các vùng màu đồng nhất. GIF động kết hợp nhiều hình ảnh hoặc khung vào một tệp duy nhất và hiển thị chúng theo trình tự để tạo clip hoạt hình hoặc video ngắn. Các giới hạn màu lên tới 256 cho mỗi khung hình và có thể là mức ít phù hợp nhất để tái tạo các hình ảnh và ảnh khác có độ dốc màu.

## Định dạng tệp GIF ##

Về mặt khái niệm, các tệp GIF có vùng đồ họa có kích thước cố định được lấp đầy bởi không hoặc nhiều hình ảnh. Một số tệp GIF chia khu vực đồ họa có kích thước cố định hoặc các khối thành các hình ảnh phụ có khả năng hoạt động như khung hình động trong trường hợp GIF động. Định dạng GIF sử dụng độ sâu pixel từ 1 đến 8 bit để lưu trữ dữ liệu bitmap. Mô hình màu RGB và dữ liệu bảng màu luôn được sử dụng để lưu trữ hình ảnh. Tùy thuộc vào phiên bản, tiêu đề có độ dài cố định ("GIF87a" hoặc "GIF89a") xác định phần đầu của tệp GIF điển hình.

Hiện tại, có hai phiên bản GIF: 87a và 89a. Cái trước là định dạng GIF gốc trong khi cái sau là định dạng GIF mới. Ở định dạng tệp này, các đặc điểm của kích thước khối và pixel được đề cập trong Bộ mô tả màn hình logic có độ dài cố định. Sự tồn tại và kích thước của Bảng màu chung có thể được chỉ định bởi bộ mô tả màn hình, theo dõi các chi tiết khác nếu có. Đoạn giới thiệu là byte cuối cùng của tệp chứa một byte duy nhất của dấu chấm phẩy ASCII. Bố cục tệp GIF87a điển hình như sau:

### Tiêu đề ###

Tiêu đề chứa sáu byte và được sử dụng để chỉ định loại tệp là GIF. Mặc dù Bộ mô tả màn hình hợp lý được tách biệt khỏi tiêu đề thực nhưng đôi khi nó được coi là tiêu đề thứ hai. Cấu trúc tương tự được sử dụng để lưu trữ tiêu đề có thể lưu trữ Bộ mô tả màn hình hợp lý. Tất cả các tệp GIF đều bắt đầu bằng chữ ký 3 byte và sử dụng các ký tự “GIF” làm mã định danh. Phiên bản cũng có kích thước ba byte và khai báo phiên bản của tệp GIF.

### Bộ mô tả màn hình logic ###

Bộ mô tả hình ảnh có độ dài cố định chỉ định thông tin màn hình và màu sắc cần thiết để tạo hình ảnh GIF. Các trường Chiều cao và Chiều rộng chứa giá trị nhỏ nhất của độ phân giải màn hình, bắt buộc để hiển thị dữ liệu hình ảnh. Nếu thiết bị hiển thị không thể hiển thị độ phân giải đã chỉ định, thì cần phải điều chỉnh tỷ lệ để hiển thị hình ảnh phù hợp. Thông tin Bản đồ Màu và Màn hình được hiển thị theo bốn trường con của bảng bên dưới (trong khi bit 0 là bit ít quan trọng nhất):


|Bit|Trường con
---|---|
|0-2|Kích thước của Bảng màu tổng thể
|3|Cờ sắp xếp bảng màu
|4-6|Độ phân giải màu
|7|Cờ bảng màu toàn cầu

#### Bảng màu tổng thể ####

Bảng màu toàn cầu tùy chọn được đặt ngay sau Bộ mô tả màn hình hợp lý. Bảng này được ánh xạ để lập chỉ mục dữ liệu màu pixel bên trong dữ liệu hình ảnh. Trong trường hợp không có Bảng màu chung, mỗi hình ảnh trong tệp GIF sử dụng Màu cục bộ của nó. Tốt hơn là cung cấp bảng màu mặc định nếu thiếu cả Bảng màu toàn cầu và cục bộ. Một loạt các bộ ba ba byte bao gồm các thành phần của bảng màu. Mỗi byte đặc trưng cho một giá trị màu RGB. Các màu đỏ, lục và lam được sử dụng làm giá trị của từng thành phần bảng màu. Các mục nhập trong Bảng màu toàn cầu có tối đa 256 mục nhập và luôn biểu thị lũy thừa hai.

#### Dữ liệu hình ảnh ####

Dữ liệu hình ảnh lưu trữ một byte các biểu tượng chưa được mã hóa, theo sau là danh sách phụ được liên kết cùng với dữ liệu được mã hóa LZW.

#### Giới thiệu tóm tắt ####

Đoạn giới thiệu đại diện cho một byte dữ liệu là ký tự cuối cùng trong tệp. Giá trị của byte này là vĩnh viễn 3Bh và chỉ định kết thúc luồng dữ liệu. Mỗi tệp GIF phải có đoạn giới thiệu ở cuối mỗi tệp.

## Người giới thiệu ##

* [Định dạng tệp GIF](https://en.wikipedia.org/wiki/GIF)

