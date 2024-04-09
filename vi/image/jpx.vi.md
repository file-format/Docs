{
  "date" : "2021-02-10",
  "keywords" :[ "tệp jpx", "định dạng tệp jpx", "tệp jpx là gì", "tệp", "ví dụ jpx", "phần mở rộng tệp jpx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Định dạng tệp hình ảnh",
  "description":"Tìm hiểu về định dạng tệp JPX và API có thể tạo và mở tệp JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Tệp JPX là gì? ##

Tệp có phần mở rộng .jpx là phần mở rộng của định dạng tệp JPEG 2000. Nó chủ yếu sử dụng kiểu nén JPEG 2000 và cũng cung cấp các tính năng nâng cao như nhiều lớp cho một hình ảnh, các không gian màu khác nhau, độ mờ và các luồng mã bị phân mảnh. JPX cũng cho phép các kiểu nén khác như JBIG, CCITT Group3, CCITT Group4, v.v. ngoài kiểu nén JPEG 2000. Định dạng tệp JPX đã được phê duyệt là tiêu chuẩn [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), nhưng không được đón nhận nồng nhiệt do việc sử dụng rộng rãi [JPEG ](/vi/image/jpeg/) định dạng tệp. Các ứng dụng có thể mở tệp JPX bao gồm Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 và CorelDraw Graphics Suite 2020.

## Tóm tắt lịch sử

Năm 2000, ủy ban Nhóm chuyên gia chụp ảnh chung đã thiết kế JP2 với mục tiêu cải thiện tiêu chuẩn JPEG dựa trên biến đổi cosine rời rạc của riêng họ bằng phương pháp dựa trên wavelet mới này. Ủy ban JPEG nhằm mục đích cung cấp các phương pháp cơ bản của họ miễn phí giấy phép. Trong giấy phép JP2 giành được sự cạnh tranh giữa 20 công ty, họ đã giành chiến thắng cách biệt. JPEG 2000 đã được tuyên bố là một tiêu chuẩn ISO, mặc dù hầu hết các trình duyệt web chưa sẵn sàng hỗ trợ JPEG 2000 kể từ năm 2017. Vào năm 2004, định dạng ISO/IEC 15444-2 đã được chấp nhận công khai dưới dạng phần mở rộng cho định dạng tệp JP2.

## Định dạng tệp JPX

Định dạng tệp JPX được xây dựng để đáp ứng các yêu cầu của ứng dụng cần cấu trúc dữ liệu ngoài chức năng được xác định bởi định dạng tệp [JP2](/vi/image/jp2/). Một tệp JP2 có phần mở rộng không tương thích có thể dẫn đến nhầm lẫn trên thị trường nơi một số trình đọc có thể giải thích một số tệp JP2 chứ không phải những tệp khác. JPX là giải pháp để tránh những vấn đề như vậy trong các ứng dụng.

### Nhận dạng tệp

Các tệp JPX được lưu trữ dưới dạng [JPF](/vi/image/jpf/) khi được lưu trữ trong hệ thống tệp máy tính truyền thống. Đó là lý do tại sao thuật ngữ JPX ít được sử dụng nhất so với JPF. Tệp JPX bắt đầu bằng các byte sau:

` 00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Tổ chức tệp

Tương tự như JP2, tệp JPX là tập hợp các hộp có cấu trúc nhị phân với các hộp được sắp xếp theo thứ tự liền kề. Hộp đầu tiên bắt đầu tệp với byte đầu tiên và byte cuối cùng của hộp cuối cùng biểu thị byte cuối cùng của tệp.
Cấu trúc nhị phân của hộp trong tệp JPX giống với cấu trúc được xác định trong định dạng tệp [JP2](/vi/image/jp2/).

### Lưu trữ CodeStream trong JPX

Định dạng tệp JPX cho phép dòng mã hình ảnh được chia thành các đoạn. Điều này cho phép sửa đổi một ô hình ảnh và ghi ô đã sửa đổi vào cuối tệp mà không cần ghi lại toàn bộ tệp. Định dạng tệp [JP2](/vi/image/jp2/) ban đầu hạn chế toàn bộ dòng mã được lưu trữ trong một phần liền kề của tệp, điều này có thể gây khó khăn cho các ứng dụng chỉnh sửa hình ảnh có thể muốn sửa đổi một ô hình ảnh và đạt khả năng hỗ trợ ở trên bằng định dạng tệp JPX. Sự phân mảnh của dòng mã hình ảnh làm cho định dạng tệp JPX vượt trội so với định dạng tệp JP2. Ngoài ra, định dạng tệp JPX cho phép kết hợp nhiều dòng mã và tạo ra kết quả hiển thị. Các dòng mã có thể được kết hợp dưới dạng tổng hợp và hoạt ảnh.

## Người giới thiệu ##

* [Tổng quan về JPEG 2000](https://jpeg.org/jpeg2000/)

