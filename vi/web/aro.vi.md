{
  "date" : "2021-12-09",
  "keywords" :[ "aro",".aro file", "aro file format", "an file type", "file", "type", "file .aro là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp ARO - Tệp ứng dụng web SteelArrow",
  "description" :"Tìm hiểu về tệp ARO là gì và các API có thể tạo và mở tệp ARO.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Tệp ARO là gì?

Tệp ARO là tệp trang web phía máy chủ được tạo bằng Ứng dụng web SteelArrow. Nó chứa các thẻ và tập lệnh [HTML](/vi/web/html/) và SteelArrow. Chúng được thực thi trên máy chủ để tạo trang phản hồi hoàn chỉnh trước khi gửi chúng tới trình duyệt của người dùng. Các tệp ARO chứa gần 95% nội dung HTML trong khi phần còn lại bao gồm mã SteelArrow. Để các tệp ARO hoạt động cho bạn, máy chủ Ứng dụng web SteelArrow phải được cài đặt và chạy trên máy chủ web.

## Định dạng tệp ARO

Các tệp ARO được viết bằng tệp ngôn ngữ đánh dấu HTML với mã JavaScript được nhúng và các tiểu dụng Java. [Thẻ SteelArrow](http://www.steelarrow.com/docs/basics1.aro) là các khối xây dựng cơ bản để phát triển các trang web. Mặc dù những thứ này không thay đổi cách hiển thị của trang, nhưng chúng được sử dụng để lấp đầy trang bằng dữ liệu. Ngoài ra, chúng cũng có thể được sử dụng để kiểm soát đầu ra bằng các câu điều kiện.

### Ví dụ về thẻ ARO

Các<SAOUTPUT> Thẻ ARO cho phép nhà phát triển xuất giá trị dữ liệu ở bất kỳ vị trí nào trong tập lệnh. Ví dụ: nó có thể được sử dụng để lấy đầu ra của bảng PARAM với<SAOUTPUT VALUE=PARAM[]> có thể được hiển thị trong HTML<BODY> nhãn.

## Người giới thiệu

* [Thẻ SteelArrow](http://www.steelarrow.com/docs/basics.aro)

