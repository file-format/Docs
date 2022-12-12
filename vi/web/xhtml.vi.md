{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "html mở rộng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Định dạng tệp ngôn ngữ đánh dấu siêu văn bản có thể mở rộng",
  "description":"Tìm hiểu về định dạng tệp XHTML và các API có thể tạo và mở tệp XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp XHTML là gì?

XHTML là định dạng tệp dựa trên văn bản có đánh dấu trong XML, sử dụng công thức cải tiến của HTML 4.0. Các tệp này rất phù hợp để mở hoặc xem trong trình duyệt web. XHTML được thiết kế để có cấu trúc hơn, ít kịch bản hơn, chung chung hơn; sử dụng tất cả các phương tiện hiện có của XML và nhiều thiết bị độc lập hơn. XHTML cung cấp một tập hợp các phần tử và thuộc tính nói chung đáng giá, với các tùy chọn mở rộng kết hợp với biểu định kiểu. Các thuộc tính được sử dụng từ bộ sưu tập thuộc tính siêu dữ liệu. XHTML cung cấp tính linh hoạt và khả năng truy cập bằng cách sắp xếp tất cả các phần tử trình bày **[HTML](/vi/web/html/)** cho biểu định kiểu. Biểu định kiểu linh hoạt hơn các yếu tố trình bày này. Thông số kỹ thuật cho HTML 4.01, HTML5 và XHTML đang được phát triển động bởi World Wide Web Consortium (W3C).

## Lịch sử tóm tắt về định dạng tệp XHTML

Lịch sử của XHTML bắt đầu với một tài liệu dự thảo được phát hành vào tháng 12 năm 1998 bởi World Wide Web Consortium. Tài liệu này đề cập đến "Định dạng lại HTML trong XML", một đặc tả có tên là XHTML 1.0. Đặc tả mới này định dạng lại HTML trong XML bằng cách sử dụng các phần tử hoặc thuộc tính hiện có. Vào tháng 5 năm 1999, W3 Consortium tuyên bố rằng HTML 4.0 đã được tái tạo thành một ứng dụng XML. tức là XHTML. Vào ngày 26 tháng 1 năm 2000, đặc điểm kỹ thuật đầu tiên xác định XHTML 1.0 đã được phát hành bởi W3C. Hơn nữa vào ngày 31 tháng 5 năm 2001, W3C đã công bố XHTML là một ngôn ngữ độc lập và bắt đầu phát triển HTML 5.0. Tuy nhiên, vào năm 2005, một nhóm làm việc (WHATWG) đã được thành lập nhằm cải thiện HTML thông thường độc lập với XHTML. WHATWG cuối cùng đã bắt đầu hoạt động trên HTML5 song song với XHTML 2.

## Định dạng tệp XHTML

XHTML là một định dạng, là tập hợp các loại tài liệu và mô-đun khác nhau bắt chước, phân loại và mở rộng HTML 4. Các tệp trong XHTML dựa trên XML và nhằm mục đích làm việc với các tác nhân người dùng dựa trên XML. Các tệp XHTML tuân thủ XML. Các công cụ XML tiêu chuẩn được sử dụng để xem, chỉnh sửa và xác thực các tệp XHTML. Các ứng dụng phụ thuộc Mô hình Đối tượng Tài liệu HTML hoặc Mô hình Đối tượng Tài liệu XML [DOM] có thể hoạt động thông qua các tài liệu XHTML. Chọn XHTML ngay hôm nay, các nhà phát triển nội dung có thể tận hưởng tất cả các lợi ích liên quan của XML mà không phải lo lắng về khả năng tương thích tiến hoặc lùi của nội dung của họ.

Một tập hợp các phần tử liên quan xây dựng một mô-đun trong XHTML. Mô-đun biểu mẫu hoặc bảng có thể chứa các thành phần biểu mẫu hoặc bảng khác nhau có thể được hiển thị trên trang web. Việc mô đun hóa nhằm mục đích cô lập các phần tử HTML thành các tập hợp nhiều phần tử được liên kết. Vì vậy, các nhà phát triển nội dung có thể tận dụng lợi thế của việc lựa chọn mô-đun cho các loại thiết bị khác nhau. Hơn nữa, các mô-đun cho phép tác nhân người dùng chọn các thành phần mà không làm mất tính nhất quán với tiêu chuẩn XHTML. Các yêu cầu phân tích cú pháp của XHTML giống như XML trong khi HTML thực hiện các yêu cầu của riêng nó.

### Tuân thủ tài liệu

XHTML2 cung cấp các thông số kỹ thuật phù hợp với các tài liệu XHTML 1.0, sử dụng các thành phần và thuộc tính không gian tên từ XML và XHTML 1.0. Sự phù hợp của tài liệu có hai loại.

Tài liệu tuân thủ nghiêm ngặt dựa trên XML chỉ cần các dịch vụ bắt buộc được xác định trong đặc tả này. Các tiêu chí sau cần được đáp ứng cho các tệp XHTML:

* Tệp phải tuân thủ các ràng buộc được xác định trong DTD và trong Phụ lục B.
* Phần tử cơ sở của tệp phải là html.
* Phần tử cơ sở của tệp phải chứa khai báo cho không gian tên XHTML và phải được định nghĩa là:

```
http://www.w3.org/1999/xhtml.
```

* Phần tử cơ sở có thể được viết là:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Trước phần tử cơ sở, một DOCTYPE phải được khai báo, định danh công khai của nó phải tham chiếu một trong ba định nghĩa loại tài liệu (DTD). Mã định danh hệ thống có thể được sửa đổi để tuân thủ các quy ước hệ thống hiện tại.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

Trong các tài liệu XML, không cần thiết phải chỉ định các khai báo XML trong tất cả các tài liệu; tuy nhiên, các nhà phát triển nội dung bị lôi cuốn sử dụng các khai báo XML trong tất cả các tài liệu XHTML của họ. Những khai báo này là bắt buộc khi mã hóa ký tự của tài liệu khác với UTF-8/16 hoặc không có mã hóa nào được chỉ định bởi một giao thức quản lý. Ví dụ sau về tài liệu XHTML định nghĩa các khai báo XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Một tác nhân người dùng phù hợp phải đáp ứng các quy tắc sau:

* Phân tích cú pháp và đánh giá tài liệu XHTML được thực hiện bởi một tác nhân người dùng để đảm bảo tính nhất quán của nó với Khuyến nghị XML 1.0.
* Trường hợp xác thực tác nhân người dùng phải kiểm tra tính hợp lệ của tài liệu đối với DTD tham chiếu của mình theo XML. Khi tệp XHTML được tác nhân người dùng xử lý dưới dạng XML chung, các tính năng của loại ID sẽ được xác nhận là số nhận dạng phân đoạn.

Nếu một tác nhân người dùng gặp phải một phần tử không được nhận dạng, sau đây là các tiêu chí bắt buộc mà tác nhân đó phải hoàn thành

* xử lý nội dung của phần tử chưa biết đó
* bỏ qua thuộc tính và giá trị của nó
* Sử dụng giá trị của thuộc tính được cung cấp làm mặc định.

Khi tác nhân người dùng bắt gặp một khai báo tham chiếu thực thể chưa được xử lý trước đó thì nó sẽ được xử lý dưới dạng các ký tự (bắt đầu bằng dấu “&” và kết thúc bằng dấu chấm phẩy). Trong quá trình xử lý nội dung, các ký tự hoặc tham chiếu thực thể ký tự mà tác nhân người dùng có thể dự đoán được nhưng không thể kết xuất được có thể sử dụng bất kỳ kết xuất thay thế nào mang lại ý nghĩa tương tự. Trong trường hợp như vậy, tài liệu phải được hiển thị theo cách làm cho người dùng thấy rõ rằng quá trình hiển thị không bình thường. Để xử lý khoảng trắng, tác nhân người dùng cần xem định nghĩa từ các ký tự CSS [CSS2].

## XHTML Khả năng tương thích ngược

Khả năng tương thích phía sau của các tài liệu XHTML 1. rất thành thạo với các tác nhân người dùng HTML 4, nếu các quy tắc thích hợp được tuân theo. XHTML 1.1 hoàn toàn tương thích ngoại trừ các chú thích ruby, mặc dù chúng thường bị các trình duyệt HTML 4 bỏ qua. XHTML 2.0 tương đối kém tương thích hơn, tuy nhiên, vấn đề đã được giải quyết ở một mức độ nào đó thông qua việc sử dụng tập lệnh.

## Người giới thiệu

* [Lịch sử XHTML: Từ những năm 1990 đến nay](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

