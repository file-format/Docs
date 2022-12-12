{
  "date" : "2019-10-11",
  "keywords" :[ "tệp psb", "định dạng tệp psb", "tệp psb là gì", "tệp", "ví dụ psb", "phần mở rộng tệp psb","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Định dạng tệp hình ảnh lớn của Photoshop",
  "description":"Tìm hiểu về định dạng tệp PSB và API có thể tạo và mở tệp PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PSB là gì?
Adobe photoshop lưu tệp ở hai định dạng. Các tệp có kích thước 30.000 x 30.000 pixel được lưu với phần mở rộng PSD và các tệp lớn hơn PSD lên tới 300.000 x 300.000 pixel được lưu với phần mở rộng PSB được gọi là “Photoshop Big”. Cụ thể hơn, các tệp PSB có thể lớn tới 4 EB (hơn 4,2 tỷ GB) với hình ảnh có chiều cao và chiều rộng lên tới 300.000 pixel. Mặt khác, PSD có thể có dung lượng tối đa lên tới 2 GB và kích thước hình ảnh là 30.000 pixel.

PSB còn được gọi là kích thước định dạng lớn cho photoshop và hỗ trợ tất cả các tính năng của photoshop như lớp, hiệu ứng và bộ lọc. Photoshop có thể chuyển đổi tệp PSB thành [PSD](/vi/image/psd/), [JPG](/vi/image/jpeg/) , [PNG](/vi/image/png/), [EPS](/vi/page-description-language/eps/), [GIF](/vi/image/gif/) cũng như các định dạng khác. Định dạng tài liệu lớn của Photoshop khả dụng khi tính năng ngăn xử lý tệp của hộp thoại tùy chọn của Photoshop được bật.

## Thông tin định dạng tệp ##

Định dạng tệp Photoshop được chia thành năm phần chính với nhiều điểm đánh dấu độ dài để di chuyển giữa các phần.

|Định dạng tệp
---|
|Tiêu đề tập tin
|Dữ liệu chế độ màu
| Tài nguyên hình ảnh
|Thông tin về lớp và mặt nạ
|(((
Dữ liệu hình ảnh
)))

### Tiêu đề tệp ###

Tiêu đề tệp có độ dài cố định là 26 byte và chứa các thuộc tính cơ bản của hình ảnh.

Chữ ký BYTE [4] – Bằng '8BPS'.

Phiên bản WORD [2] – Số phiên bản, PSD #1, PSB #2.

BYTE Dự trữ [6] – Dự trữ và luôn bằng không.

Kênh WORD [2] – Số lượng kênh màu trong hình ảnh bao gồm các kênh alpha. Giá trị của nó nằm trong khoảng từ 1 đến 56.

Hàng DÀI [4] – Chiều cao của hình ảnh tính bằng pixel, PSD 1-30.000, PSB 1-300.000.

Cột DÀI [4] – Chiều rộng của hình ảnh tính bằng pixel, PSD 1-30.000, PSB 1-300.000.

WORD Depth [2] – Số bit trên mỗi kênh. Các giá trị được hỗ trợ là 1,8,16 và 32.

Chế độ WORD [2] – Chế độ màu của tệp.

#### Chế độ Mô tả ####


|Chế độ|Mô tả
---|---|
|0|Bitmap (đơn sắc)
|1|Thang xám
|2|Đã lập chỉ mục
|3|RGB
|4|CMYK
|7|Đa kênh
|8|Duotone (bán cung)
|9|Phòng thí nghiệm

### Dữ liệu chế độ màu ###

Sau phần tiêu đề tệp, phần dữ liệu chế độ màu theo sau. Khối bắt đầu bằng Số DÀI cho biết độ dài của khối tính bằng byte. Cấu trúc của dữ liệu chế độ màu như sau:

4 byte – Độ dài của dữ liệu màu sau.

Biến – Dữ liệu màu

Nếu giá trị trường chế độ trong phần tiêu đề không phải là Màu được lập chỉ mục hoặc màu kép, độ dài của khối sẽ bằng 0 và sẽ không có dữ liệu sau trường độ dài.

Đối với Hình ảnh màu được lập chỉ mục, độ dài sẽ là 768 byte sẽ chứa bảng màu 256. Đối với Duotone, dữ liệu sẽ chứa thông số màn hình và các thông tin liên quan khác.

### Tài nguyên hình ảnh ###

Tiếp theo phần dữ liệu chế độ màu, khối thứ ba là phần tài nguyên hình ảnh. Bốn byte đầu tiên là một số DÀI chỉ định độ dài của khối theo sau là một loạt các khối tài nguyên. Cấu trúc của khối tài nguyên hình ảnh như sau:

Loại BYTE [4] – Chữ ký '8BIM'

WORD ID [2] – ID tài nguyên hình ảnh. Có một danh sách ID tài nguyên có thể được nhìn thấy từ liên kết tham chiếu.

Tên BYTE [Biến] – Tên: Chuỗi Pascal có độ dài chẵn. ** **

Kích thước DÀI [4] – Kích thước thực tế của dữ liệu tài nguyên theo sau.

Dữ liệu BYTE [Biến} – Dữ liệu tài nguyên. Nó được đệm để làm cho kích thước đồng đều.

Một số định dạng tài nguyên được giải thích ngắn gọn dưới đây:

**Định dạng tài nguyên lưới và đường căn:** Thông tin lưới và đường căn được lưu trữ trong khối tài nguyên. Các khối tài nguyên này chứa tiêu đề hướng dẫn và lưới 16 byte, theo sau là khối thông tin hướng dẫn 5 byte.

**Định dạng tài nguyên hình thu nhỏ:** Thông tin hình thu nhỏ được lưu trữ trong khối tài nguyên hình ảnh để hiển thị xem trước bao gồm tiêu đề 28 byte và hình thu nhỏ JFIF trong RGB.

**Định dạng tài nguyên của bộ lấy mẫu màu:** Thông tin về bộ lấy mẫu màu được lưu trữ trong khối tài nguyên hình ảnh với tiêu đề 8 byte, theo sau là khối thông tin về bộ lấy mẫu màu có độ dài thay đổi.

### Thông tin về Lớp và Mặt nạ ###

Khối thứ tư là khối thông tin lớp và mặt nạ và chứa thông tin về các lớp và mặt nạ. Thông tin lớp được lưu trữ đầu tiên và sau đó là thông tin mặt nạ.

**Thông tin lớp:** Thông tin lớp bắt đầu bằng giá trị DÀI cho biết độ dài của thông tin lớp. Sau đó, có số lượng giá trị WORD hiển thị số lượng bản ghi lớp cần theo dõi.

[8] – chiều dài của các lớp

[2] – Đếm lớp

[Biến] – Thông tin về từng lớp.

[Biến] – Dữ liệu hình ảnh kênh.** **

**Thông tin về mặt nạ:** Cấu trúc mặt nạ có định dạng như sau:


|Cấu trúc dữ liệu|Tên trường| Sự mô tả
---|---|---|
|CÂU| Không gian màu lớp phủ| (Không có tài liệu)
|BYTE[8]| Thành phần màu| Thành phần màu 4x2 byte
|CÂU| Độ mờ| 0#trong suốt, 1#đục
|BYTE| loại| 0#đảo ngược, 1#được bảo vệ, 128#sử dụng giá trị được lưu trữ
|BYTE| đệm| đặt thành không

### Dữ liệu hình ảnh ###

Phần cuối cùng chứa dữ liệu pixel của hình ảnh. Dữ liệu hình ảnh được lưu trữ dưới dạng một chuỗi theo trình tự trong các mặt phẳng, tức là đầu tiên tất cả dữ liệu màu đỏ, sau đó là tất cả dữ liệu màu xanh lá cây, v.v. WORD ở đầu mỗi dòng hiển thị kích thước tính bằng byte liên quan đến từng dòng quét.

[2] – Phương pháp nén:

[Biến] – Dữ liệu hình ảnh theo thứ tự phẳng, tức là RRRR, GGGG, BBBB, v.v.

Phương pháp nén:

0 – Raw Dữ liệu hình ảnh

1 – RLE nén

2 – Zip không dự đoán

3 – Zip với dự đoán

## Tài liệu tham khảo ##

* [Định dạng tệp PSB - Bởi Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

