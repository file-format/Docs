{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PDF/A",
  "description":"Tìm hiểu về định dạng tệp PDF/A và các API có thể tạo và mở tệp PDF/A.",
  "linktitle" : "PDF/A",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/A là gì? #

PDF/A là định dạng tiêu chuẩn ISO để lưu trữ tài liệu điện tử ở định dạng PDF. Lý do cơ bản ra đời của nó là đáp ứng yêu cầu lưu trữ lâu dài. Tiêu chuẩn đảm bảo việc mở các tệp lưu trữ ngay cả sau một thời gian dài bằng cách áp đặt các giới hạn nhất định đối với các phần không thể thiếu của tài liệu để đạt được sự phù hợp. Định dạng này hiện được áp dụng rộng rãi trên tất cả các ngành công nghiệp. Trình xem PDFA/A như Adobe Acrobat Reader, đảm bảo rằng các tệp được lưu với định dạng này có thể được mở ngay cả trong tương lai theo thông tin được chia sẻ bởi Tiêu chuẩn này.

## Phiên bản PDF/A ##

PDF/A đã được chấp nhận là Tiêu chuẩn ISO vào tháng 10 năm 2005. Kể từ đó, nó đã được cải tiến liên tục và một số tiêu chuẩn khác đã được phát triển theo thời gian. Thông tin về các tiêu chuẩn PDF/A được xuất bản theo thời gian và chi tiết của chúng như sau:

* **PDF/A-1:** được xuất bản vào tháng 10 năm 2005 dưới dạng ISO 19005-1 và dựa trên PDF 1.4
* **PDF/A-2:** được xuất bản vào tháng 6 năm 2011 dưới tên ISO 19005-2 và dựa trên PDF 1.7 (ISO 32000-1:2008)
* **PDF/A-3:** xuất bản vào tháng 10 năm 2012 dưới tên ISO 19005-3 và dựa trên PDF 1.7 (ISO 32000-1:2008)

## PDF/A-1 ##

Tiêu chuẩn PDF/A-1 dựa trên phiên bản PDF 1.4 gốc. Tiêu chuẩn PDF/A-1 xác định hai cấp độ tuân thủ cho các tệp PDF.

### PDF/A-1a ###

Nó phù hợp với Cấp độ A và đáp ứng tất cả các yêu cầu trong thông số kỹ thuật của Tiêu chuẩn PDF/A-1. PDF/A-1a đảm bảo rằng văn bản có thể trích xuất được từ tài liệu. Nó cũng đảm bảo rằng quá trình đọc tự nhiên của tài liệu văn bản tích hợp vẫn còn nguyên vẹn. PDF/A áp đặt yêu cầu về khả năng trình bày văn bản trên màn hình giảm do được tái cấu trúc, được gọi là "PDF được gắn thẻ". Nó nhằm mục đích tăng khả năng truy cập các tệp phù hợp cho người dùng bị suy giảm thể chất bằng cách cho phép phần mềm hỗ trợ.

### PDF/A-1b ###

PDF/A-1b là mức tuân thủ thấp hơn và xử lý hình thức trực quan của tài liệu điện tử đối với tiêu chuẩn ISO 19005. Nó đảm bảo rằng văn bản và nội dung khác trên các trang được sao chép đồng nhất. Tuân thủ Cấp độ B này biểu thị sự tuân thủ tối thiểu để đảm bảo rằng giao diện trực quan được hiển thị của tệp tuân thủ có thể duy trì lâu dài.

## PDF/A-2 ##

PDF/A-2 đã được ISO Standard phát hành vào tháng 7 năm 2011 dưới dạng một tiêu chuẩn mới được gọi là ISO 32001-1. Tiêu chuẩn mới này không chỉ được hưởng lợi từ tất cả các tính năng của các phiên bản PDF cho đến 1.7 mà còn được giới thiệu như một tiêu chuẩn mới. PDF/A-2 bao gồm các tính năng sau đây như một phần của tiêu chuẩn mới này.

* PDF/A-2 đi kèm với sự hỗ trợ của [JPEG2000](/vi/image/jp2/) rất hữu ích trong trường hợp tài liệu được quét.
* Nó hỗ trợ nhúng các bộ sưu tập PDF/A có thể được sử dụng để tạo tệp PDF chứa có các tệp tương tự khác
* Nó hỗ trợ toàn bộ tính năng minh bạch của các tệp PDF so với PDF/A-1 nơi nó được hỗ trợ một phần.
* PDF/A-2 cung cấp hỗ trợ cho nội dung tùy chọn hữu ích cho các ứng dụng bản đồ và bản vẽ kỹ thuật. Đây còn được gọi là các lớp có thể hiển thị hoặc ẩn theo yêu cầu của người xem.
* Nó chỉ định các yêu cầu đối với siêu dữ liệu XMP tùy chỉnh
* Thêm một số loại chú thích mới hơn vào danh sách các loại chú thích bị cấm. Ngoài ra, một số loại nhận xét mới hơn như nhận xét chỉnh sửa văn bản đã được thêm vào danh sách các mục được chấp nhận.

## PDF/A-3 ##

PDF/A-3 bao gồm tất cả các yêu cầu tuân thủ của Cấp 2 và cho phép nhúng các định dạng tệp bổ sung (chẳng hạn như XML, [CSV](/vi/spreadsheet/csv/), [CAD](/vi/cad/), [xử lý văn bản](/vi/word-processing/) , [bảng tính](/vi/spreadsheet/) và những thứ khác) vào tài liệu tuân thủ PDF/A.

## Người giới thiệu ##

* [PDF/A - Theo Wikipedia](https://en.wikipedia.org/wiki/PDF/A)
* [Sách trắng: PDF/A – Khái niệm cơ bản](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)

