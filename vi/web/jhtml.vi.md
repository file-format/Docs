{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","tệp jhtml", "định dạng tệp jhtml", "loại tệp jhtml", "tệp", "loại", "tệp jhtml là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Tệp Java HTML",
  "description":"Tìm hiểu về định dạng tệp JHTML và API có thể tạo và mở tệp JHTML.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Tệp JHTML là gì?

Tệp có phần mở rộng .jhtml là tệp [HTML](/vi/web/html/) có mã [Java](/vi/programming/java/) được thực thi trên máy chủ khi khách hàng yêu cầu trang này trong trình duyệt. Máy chủ xử lý các yêu cầu, thực thi các hàm Java có trong hàm và trả lại trang cho trình duyệt của máy khách. Các đối tượng Java được nhúng trong các trang JHTML chạy trên máy chủ để xử lý các yêu cầu đối với các trang thuộc loại này. Các tệp JHTML cũng có thể truy cập thông tin từ cơ sở dữ liệu bằng kết nối JDBC (Java [Database](/vi/database/) Connectivity). Các tệp JHTML có thể được mở trong bất kỳ trình soạn thảo văn bản nào và được xem trong các trình duyệt web như Google Chrome, Firefox và Safari.

## Định dạng tệp JHTML

JHTML là công nghệ độc quyền của ATG và có thể được tạo bằng Trình chỉnh sửa tài liệu Dynamo ATG (Art Technology Group). Các tệp JHTML được viết ở định dạng tệp văn bản thuần sử dụng mã HTML và Java tiêu chuẩn. Chúng chứa các thẻ HTML tiêu chuẩn ngoài các thẻ độc quyền tham chiếu các đối tượng Java. Khi người dùng yêu cầu một trang như vậy, máy chủ HTTP sẽ chuyển tiếp yêu cầu đến máy chủ ứng dụng Java. Đầu tiên, trang JHTML được chuyển đổi thành tệp .java và được biên dịch để tạo tệp [.class](/vi/programming/class/) được thực thi dưới dạng một servlet. Điều này tạo ra một luồng dữ liệu HTTP và HTML tiêu chuẩn được trả lại cho trình duyệt yêu cầu để hiển thị cho người dùng. Điều này hữu ích để chạy các truy vấn liên quan đến cơ sở dữ liệu trên máy chủ và trả lại kết quả tích lũy cuối cùng cho trình duyệt của khách hàng.

## Người giới thiệu

* [Cấu trúc toàn cục của tài liệu HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

