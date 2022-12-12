{
  "date" : "2021-04-08",
  "keywords" :[ "tệp pkg", "định dạng tệp pkg", "tệp pkg là gì", "tệp", "ví dụ pkg", "phần mở rộng tệp pkg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Định dạng tệp lưu trữ có thể mở rộng",
  "description":"Tìm hiểu về định dạng tệp PKG và các API có thể tạo và mở tệp PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Tệp PKG là gì?

Tệp có phần mở rộng .pkg là tệp gói trình cài đặt được sử dụng để cài đặt phần mềm trên macOS. Ngoài máy tính Macintosh, nó cũng được sử dụng trên iPhone. Ứng dụng cài đặt sẵn của Apple có thể được sử dụng để cài đặt nội dung của tệp PKG. Tệp PKG tương tự như tệp MSI được sử dụng trên Hệ điều hành Windows để cài đặt phần mềm. Trong quá trình cài đặt, các tệp gói này có thể ghi lại các thông báo cho bạn ý tưởng về những thứ bổ sung được cài đặt bởi gói này.

## Định dạng tệp PKG

PKR là các tệp nhị phân được nén để giảm kích thước tệp tổng thể. Kể từ OSX 10.5, các gói phẳng với các tệp trình cài đặt duy nhất đã được Apple giới thiệu. Những định dạng này khác với các định dạng đóng gói trước đây xuất hiện dưới dạng gói thay vì tệp đơn lẻ. Các gói đi kèm này chứa một hệ thống phân cấp thư mục có cấu trúc lưu trữ các tệp theo cách tạo điều kiện thuận lợi cho việc truy xuất chúng thông qua một số tệp chỉ mục. Định dạng tệp PKG phẳng thực sự là một kho lưu trữ [XAR](/vi/compression/xar/) có:

* Tiêu đề - Xác định kích thước, tổng kiểm tra và thông tin phiên bản
* Mục lục - Một tài liệu XML (và phải) được mã hóa dưới dạng UTF-8 và được lưu trữ ở phần đầu của tệp, giúp dễ dàng quét qua kho lưu trữ để giải nén từng tệp
* Heap - đống dữ liệu phi cấu trúc được tham chiếu bởi TOC

## Người giới thiệu

* [Định dạng tệp gói phẳng](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

