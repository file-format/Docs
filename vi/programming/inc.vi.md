{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Phần mở rộng tệp INC - Tệp INC là gì?",
  "description":"Tìm hiểu về INC Bao gồm định dạng tệp và các API có thể tạo và mở tệp INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Tệp INC là gì?

Tệp INC là một tệp bao gồm được mã nguồn của chương trình phần mềm sử dụng để tham chiếu thông tin tiêu đề. Nó tương tự như [định dạng tệp .h](/vi/programming/h/) và chứa các khai báo, hàm, tiêu đề hoặc macro có thể được sử dụng lại bởi các tệp mã nguồn như C++. Các tệp INC được sử dụng bởi nhiều ngôn ngữ lập trình như C, [C++](/vi/programming/cpp/), Pascal, [PHP](/vi/programming/php/) và [Java](/vi/programming/java/). Có thể sử dụng các trình soạn thảo văn bản như Microsoft Notepad, Notepad++ và TextEdit để mở tệp INC.

## Định dạng tệp INC - Thông tin khác

Tệp INC được lưu dưới dạng tệp văn bản thuần túy với tất cả các khai báo được bao gồm theo cú pháp khai báo. Một tệp INC cũng có thể tham chiếu các tệp INC khác. Sau khi được tạo, tệp INC sẽ trở thành một phần của dự án và có thể được tham chiếu từ các tệp nguồn như C++. Nó có thể được tham chiếu bởi nhiều tệp nguồn để tránh trùng lặp.

## Nội dung tệp INC

Các tệp INC có thể bao gồm các thông tin sau.

**`Biến`** - Trong trường hợp Lập trình hướng đối tượng (OOP), tệp tiêu đề lớp chứa các định nghĩa về tất cả các biến cấp lớp có thể truy cập qua các tệp mã nguồn triển khai

**`Tuyên bố phương thức`** - Tất cả các khai báo phương thức được bao gồm trong tệp tiêu đề .h để có thể truy cập được trên nhiều tệp triển khai.

**`Định nghĩa hàm không nội tuyến`** - Các tệp tiêu đề cũng có thể chứa định nghĩa của một phương thức không nội tuyến.

## Nhược điểm của việc sử dụng tệp INC trong PHP

PHP là các tập lệnh phía máy chủ chạy trên máy chủ và trả lại kết quả cho các trang web đang gọi. Nếu tệp PHP đang tham chiếu tệp INC và máy chủ không được định cấu hình để phân tích cú pháp tệp .inc (rất phổ biến), người dùng có thể xem mã nguồn php trong tệp .inc bằng cách truy cập thư mục URL. Vì vậy, người ta phải cẩn thận khi sử dụng tệp INC làm tệp bao gồm trong PHP.

## Người giới thiệu

* [Sử dụng INC trong PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

