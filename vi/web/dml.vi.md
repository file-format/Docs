{
  "date" : "2021-05-25",
  "keywords" :[ "DML","tệp DML", "định dạng tệp DML", "loại tệp DML", "tệp", "loại", "tệp DML là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - Tệp HTML DynaScript",
  "description":"Tìm hiểu về định dạng tệp DML và API có thể tạo và mở tệp DML.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Tệp DML là gì?

Tệp có phần mở rộng .dml là tệp mã trang tập lệnh web được tạo bằng DyanScript. DynaScript là ngôn ngữ kịch bản [HTML](/vi/web/html/) động tương thích với ECMAScript và cung cấp hầu hết các tính năng giống như ngôn ngữ kịch bản khác. Nó tương tự như mã ColdFusion và mã Microsoft Active Server Pages (ASP). Các tệp DML có thể được mở và xem trong các trình duyệt web tiêu chuẩn tương tự như các trang HTML khác.

## Định dạng tệp DML

Các tệp DML được tạo ở định dạng tệp văn bản thuần túy và có thể được mở bằng trình chỉnh sửa văn bản để xem mã. Viết mã bằng ngôn ngữ kịch bản DML có thể được sử dụng để tự động tạo HTML trên các trang DML được lưu trữ phía máy chủ. DynaScripts được xây dựng từ các yếu tố ngôn ngữ sau:


* Thẻ SCRIPT - Chúng được nhúng trong tài liệu dưới dạng nhận xét HTML. Một nhận xét HTML được đánh dấu bằng \ <!-- tag.
* Literals - Đây là những giá trị cố định trong tệp DynaScript. Ví dụ về những điều này bao gồm các số nguyên chẳng hạn như 123 , 0x3F , 0123, số dấu phẩy động chẳng hạn như 456.789 , 3.2e-8, Boolean chẳng hạn như đúng hoặc sai và chuỗi chẳng hạn như "The rain in Spain"
* Biến - Không cần xác định hoặc gán biến DynaScript cho một kiểu dữ liệu cố định. Một biến phải có một giá trị trước khi bạn sử dụng nó trong một biểu thức; nếu không, một cảnh báo thời gian chạy được tạo ra.
* Biểu thức - Đây là sự kết hợp của các biến, giá trị bằng chữ, toán tử và các biểu thức khác. Vế phải của câu lệnh gán là một biểu thức.
* Toán tử - Chúng hoạt động trên một hoặc nhiều biểu thức được gọi là toán hạng. Đây có thể là bậc ba, nhị phân hoặc đơn nguyên: toán tử bậc ba tác động trên ba biểu thức, toán tử nhị phân tác động trên hai biểu thức và toán tử một ngôi tác động trên một biểu thức.
* Các câu lệnh - Các dòng lệnh điều khiển này, thao tác với các đối tượng và lập trình chung. Nói chung, các câu lệnh này tuân theo cú pháp C và Java tiêu chuẩn. Ví dụ như các vòng lặp if-else, do-while, switch, break, continue, v.v. giống như bất kỳ ngôn ngữ kịch bản nào khác.
* Hàm - Các hàm, giống như bất kỳ ngôn ngữ kịch bản lệnh nào khác, cho phép bạn đóng gói một lần tập hợp các hướng dẫn trong tài liệu dưới dạng một hàm, sau đó sử dụng nó nhiều lần trong toàn bộ tài liệu (bằng cách gọi hàm). DynaScript cũng hỗ trợ các chức năng.
* Đối tượng - DynaScript hướng đối tượng và hỗ trợ `đối tượng` cũng như các khái niệm hướng đối tượng cơ bản về Đóng gói, Đa hình và Kế thừa.

