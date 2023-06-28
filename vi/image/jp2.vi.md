{
  "date" : "2019-10-11",
  "keywords" :[ "tệp jp2", "định dạng tệp jp2", "tệp jp2 là gì", "tệp", "ví dụ jp2", "phần mở rộng tệp jp2","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Định dạng tệp hình ảnh",
  "description":"Tìm hiểu về định dạng tệp JP2 và các API có thể tạo và mở tệp JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Tệp JP2 là gì? ##

JPEG 2000 (**JP2**) là một hệ thống mã hóa hình ảnh và tiêu chuẩn nén hình ảnh tiên tiến nhất. Nó sử dụng công nghệ wavelet để mã hóa nội dung không mất dữ liệu ở bất kỳ chất lượng nào cùng một lúc. Hơn nữa, không bị ảnh hưởng đáng kể nào về hiệu quả mã hóa, JPEG 2000 có khả năng truy cập và giải mã cùng một nội dung một cách hiệu quả thành nhiều độ phân giải và chất lượng khác nhau. Các luồng mã trong JPEG 2000 có khả năng mở rộng đáng kể khi có các vùng quan tâm cung cấp khả năng truy cập ngẫu nhiên theo không gian.

JPEG 2000 nổi bật là một trong những tiêu chuẩn có khả năng mở rộng nhất. Các phần khác nhau của hình ảnh có thể được lưu trữ bằng các chất lượng khác nhau. Có thể đạt được mức tăng hiệu suất đáng chú ý bằng cách sắp xếp thứ tự luồng mã theo nhiều cách khác nhau. Tuy nhiên, JP2 yêu cầu các bộ mã hóa/giải mã phức tạp và thách thức về mặt tính toán, do tính linh hoạt này. So với JPEG, JPEG 2000 chỉ tạo ra các tạo tác vòng tạo ra các vòng ở gần mép hình ảnh và có thể bị mờ, trong khi JPEG sử dụng các khối tạo tác hình ảnh 8×8 có thể vừa là tạo vòng vừa tạo khối. Sở hữu tới 16384 thành phần đa dạng với kích thước tính bằng terapixel và độ chính xác có thể cao tới 38 bit/mẫu.

## Lịch sử ##

Năm 2000, ủy ban Nhóm chuyên gia chụp ảnh chung đã thiết kế JP2 với mục tiêu cải thiện tiêu chuẩn JPEG dựa trên biến đổi cosine rời rạc của riêng họ bằng phương pháp dựa trên wavelet mới này. Ủy ban JPEG nhằm mục đích cung cấp các phương pháp cơ bản của họ miễn phí giấy phép. Trong giấy phép JP2 giành được sự cạnh tranh giữa 20 công ty, họ đã giành chiến thắng cách biệt. JPEG 2000 đã được tuyên bố là một tiêu chuẩn ISO, mặc dù hầu hết các trình duyệt web chưa sẵn sàng tiếp tay cho JPEG 2000 kể từ năm 2017.

## Các bộ phận của hệ thống mã hóa hình ảnh JPEG 2000 ##

Sau đây là những phần chính cấu thành bộ tiêu chuẩn hoàn chỉnh cho JPEG 2000.


|Phần|Tiêu đề|Mô tả|Số
---|---|---|---|
|Phần 1|Hệ thống mã lõi| Xác định cú pháp của dòng mã. Các giai đoạn khác nhau liên quan đến việc giải mã hình ảnh JPEG 2000. Giải thích định dạng tệp cơ bản JP2, siêu dữ liệu và quyền IP sẽ được cung cấp.|ISO/IEC 15444-1
|Phần 2|Phần mở rộng|Xác định phần mở rộng cho luồng mã định dạng tệp và cho phép trình diễn mẫu HDR, đặc tả không gian màu, cắt xén, biến đổi hình học; hình ảnh động, siêu dữ liệu đa dạng và nhiều luồng mã.|ISO/IEC 15444-2
|Phần 3|Motion JPEG 2000 (MJ2 hoặc MJP2)|Giới thiệu định dạng tệp cho các chuỗi chuyển động, mã hóa hình ảnh trong một luồng mã độc lập.|ISO/IEC 15444-3
|Phần 4|Tuân thủ|Kiểm tra trạng thái các kỹ thuật mã hóa và giải mã cũng như kiểm tra tệp cho cả luồng mã trần và tệp JP2.|ISO/IEC 15444-4
|Phần 5|Phần mềm tham khảo|Bao gồm hai gói mã nguồn (Java, C) triển khai Hệ thống mã hóa lõi và có sẵn theo giấy phép nguồn mở.|ISO/IEC 15444-5
|Phần 6|Định dạng tệp ảnh ghép|Xác định định dạng tệp JPM và cho phép tạo ảnh tài liệu nhiều trang cho các ứng dụng giống như fax. Hỗ trợ sử dụng JBIG2 và JPEG.|ISO/IEC 15444-6
|Phần 8|JPEG 2000 Secured (JPSEC)|Đảm bảo tính bảo mật của giao dịch, nội dung và công nghệ, đồng thời cho phép các luồng JPEG 2000 bit được bảo mật.|ISO/IEC 15444-8
|Phần 9|JPIP|Xác định các công cụ trong môi trường nối mạng để truy cập vào siêu dữ liệu và hình ảnh, đồng thời nêu rõ các giao thức tương tác và hiệu quả|ISO/IEC 15444-9
|Phần 10|JP3D|Phần mở rộng thể tích của Phần 1 và giới thiệu kích thước Z. Mở rộng khái niệm về ô xếp, khối mã, khu bầu cử và các tính năng trợ năng theo vùng quan tâm 3D.|ISO/IEC 15444-10
|Phần 11|JPWL|Giải quyết vấn đề truyền tải được tổ chức tốt qua mạng không dây dễ xảy ra lỗi. Phần mở rộng này tương thích với bộ giải mã|ISO/IEC 15444-11
|Phần 13|Bộ mã hóa cấp đầu vào|Xác định triển khai bộ mã hóa cấp đầu vào của hệ thống mã hóa lõi.|ISO/IEC 15444-13
|Phần 14|JPXML|Một biểu diễn bằng XML và giải thích các đoạn đánh dấu và phương pháp truy cập dữ liệu bên trong của hình ảnh.|ISO/IEC 15444-14
|Phần 15|HTJ2K (Đang phát triển)|Chỉ định thuật toán mã hóa khối thay thế. Thuật toán cung cấp thông lượng tăng gấp 10 lần và khả năng mã hóa/giải mã không mất dữ liệu.|

## Định dạng tệp JP2 ##

JPEG 2000 xác định định dạng tệp cũng như dòng mã giống như JPEG-1. Mặc dù các mẫu hình ảnh chỉ được mô tả bởi JPEG 2000, nhưng JPEG-1 bao gồm các thông tin bổ sung khác về không gian màu và độ phân giải cần thiết để mã hóa hình ảnh. Nếu hình ảnh được lưu dưới dạng tệp JPEG 2000, thì **.jp2** được sử dụng làm phần mở rộng. Định dạng tệp này được cải thiện hơn nữa bằng phần mở rộng JPEG 2000 phần 2, xác định cơ chế hoạt hình và cấu hình của nhiều luồng mã thành một hình ảnh duy nhất. Phần mở rộng **.jpx** được sử dụng khi hình ảnh lưu bằng định dạng tệp mở rộng này. Vì dữ liệu dòng mã không được coi là chủ yếu được lưu trong các tệp, nên không có phần mở rộng tiêu chuẩn nào được xác định cho mục đích này. Mặc dù với mục đích thử nghiệm, nó thường có phần mở rộng là **.jpc** hoặc **.j2k**. Ngược lại với JPEG-1, JPEG 2000 chọn một cách khác để mã hóa siêu dữ liệu ở định dạng XML. Tiêu chuẩn 12234-1.4(của ủy ban ISO TC42) được sử dụng làm tài liệu tham khảo giữa các thẻ Exif và các thành phần XML. JPEG 2000 có thể chứa tiêu chuẩn ISO, XMP bên trong.

### Miếng, mảnh nhỏ ###
Các tệp JPEG 2000 bao gồm các khối liên tiếp. Mỗi đoạn có tiêu đề 8 byte: kích thước đoạn 4 byte (big-endian, byte cao đầu tiên) và loại đoạn 4 byte - một trong các chữ ký được xác định trước: "jP " hoặc "jP2".

Đoạn thứ hai phải thuộc loại "ftyp" và có loại phụ ở độ lệch 8. JPEG 2000 được xác định bởi loại phụ phải là một trong các giá trị: "jp2 " (loại tệp \*.JP2), "jp20" (tệp gõ \*.JPA), "jpm " (loại tệp \*.JPM), "jpx " (loại tệp \*.JPX).

Lặp lại các đoạn, cho đến khi phát hiện loại không xác định, chúng tôi soạn tệp hình ảnh/video JPEG 2000.

### Chuyển màu ###

Ban đầu, việc chuyển đổi hình ảnh từ không gian màu RGB sang không gian màu khác là bắt buộc. Với mục đích này, có hai cách: Biến đổi màu không thể đảo ngược (ICT) và Biến đổi màu có thể đảo ngược (RCT). Trước đây sử dụng không gian màu YC,,B,,C,,R, và phải được triển khai trong điểm fix/floating trong khi sau đó sử dụng không gian màu YUV đã sửa đổi và có thể đảo ngược về bản chất.// //Không giới hạn ở kiểu RGB, JPEG Ngôn ngữ 2000 sử dụng chuyển đổi nhiều thành phần.

### Lát gạch ###

Khi quá trình chuyển đổi màu hoàn tất, hình ảnh sẽ chuyển đổi thành các vùng hình chữ nhật được gọi là ô có thể được chuyển đổi và mã hóa riêng. Kích thước của tất cả các ô sẽ giống nhau hoặc toàn bộ hình ảnh có thể được coi là một ô duy nhất. Bộ giải mã tận dụng lợi thế của việc xếp ô và tiêu tốn ít bộ nhớ hơn hoặc có thể mã hóa một phần một số ô xếp. Mặc dù kỹ thuật này có nhược điểm là làm giảm chất lượng hình ảnh.

### Biến đổi wavelet ###

Hình ảnh sau khi sắp xếp được biến đổi wavelet có thể đảo ngược hoặc đảo ngược và được thực hiện bằng cách sử dụng sơ đồ tích chập hoặc nâng.

### Tỷ lệ nén ###

Tùy thuộc vào các đặc điểm vật lý của hình ảnh, mức tăng nén là 20% đạt được Dự đoán dự phòng không gian của JPEG 2000 đóng một vai trò quan trọng trong quá trình nén và hình ảnh có độ phân giải cao có xu hướng đạt được lợi thế nhất.

## Các ứng dụng được phục vụ bởi tiêu chuẩn ##

* Ghi, chỉnh sửa và lưu trữ video HD dựa trên khung hình
* Hình ảnh y tế & sinh trắc học
* hình ảnh vệ tinh, viễn thám và phát hiện chuyển động
* Giao tiếp máy khách/máy chủ, phân phối và lưu trữ mạng.
* Rạp chiếu phim kỹ thuật số, Đóng góp nguồn cấp dữ liệu HDTV trực tiếp, Công cụ nghe nhìn số hóa

## Người giới thiệu ##

* [Tổng quan về JPEG 2000](https://jpeg.org/jpeg2000/)
* [Hệ thống mã hóa hình ảnh JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

