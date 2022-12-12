{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Thư điện tử",
  "description":"Tìm hiểu về định dạng tệp EML và các API có thể tạo và mở tệp EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Tệp EML là gì?

Định dạng tệp EML đại diện cho các email được lưu bằng Outlook và các ứng dụng có liên quan khác. Hầu như tất cả các ứng dụng gửi email đều hỗ trợ định dạng tệp này để tuân thủ Tiêu chuẩn định dạng thư Internet RFC-822. Microsoft Outlook là phần mềm mặc định để mở các loại thư EML. Các tệp EML có thể được sử dụng để lưu vào đĩa cũng như gửi cho người nhận bằng các giao thức liên lạc.

## Tóm tắt lịch sử của EML

Thông số định dạng tệp EML có sẵn theo [RFC 822](http://www.ietf.org/rfc/rfc0822.txt) Định dạng Chuẩn. Trước RFC-822, RFC-733 điều chỉnh các quy tắc trao đổi thông báo mạng cho đến năm 1982, cái trước được tạo ra như một cải tiến cho bên bằng cách thiết lập các tiêu chuẩn ARPA. Đồng thời, Microsoft đã tạo các mô-đun COM của riêng mình để phát triển ứng dụng email khách của riêng mình, tức là Outlook Express. RFC-822 đã đi theo con đường được thiết lập dưới dạng định dạng độc quyền khi Microsoft đi chệch khỏi tiêu chuẩn mở và tạo định dạng tệp [PST](/vi/email/pst/), trong đó các email được lưu ở định dạng cơ sở dữ liệu có cấu trúc cao. Điều này dẫn đến sự cố cho người dùng ứng dụng email khách không phải của Microsoft khi email được chuyển tiếp từ Microsoft Outlook.

Đó là vào năm 2001 khi tiêu chuẩn 822 được nâng cao thành 2822 - Định dạng Thư Internet hiện đang được sử dụng để tạo, đọc và gửi thư EML ở định dạng MIME RFC-822.

## Thông số kỹ thuật định dạng tệp EML

Các tệp EML bao gồm hai phần được phân biệt:

* Tiêu đề - Chứa thông tin về tiêu đề thư
* Nội dung thư - Chứa chuỗi thông tin có thể bao gồm nội dung thư, hình ảnh nhúng và tệp đính kèm

### Thông tin tiêu đề ###

Tệp EML bao gồm thông tin Tiêu đề và nội dung thư tùy chọn. Mỗi dòng tiêu đề trong EML có hai phần được phân tách bằng dấu hai chấm ":". Cái đầu tiên được gọi là Tên tiêu đề và cái sau dấu hai chấm là phần thân tiêu đề. Ví dụ: các tiêu đề như vậy bao gồm:

* Địa chỉ email người gửi
* Địa chỉ email người nhận
* Chủ đề Email
* Dấu thời gian và ngày của tin nhắn

**Tiêu đề ví dụ**

Từ:<John@bmw.eml.light.com>

Đến:<Andy@fileformat.com>

Ngày: Thu, 8 Mar 2018 10:43:37 +0100

Chủ đề: đèn bmw eml

### Nội dung thư ###

Nội dung thư EML chứa thông tin chính của email ở dạng văn bản, siêu liên kết và tệp đính kèm. Nội dung email có thể chứa văn bản có thể đọc được nhưng không cần thiết. Trong trường hợp này, nội dung thư có thể trống hoặc chứa dữ liệu tệp đính kèm được mã hóa.

Nội dung của nội dung thư được mô tả bởi Loại nội dung cho phép các ứng dụng đọc đọc thông tin ở các định dạng tương ứng. Nó thực sự đại diện cho bản chất và định dạng của một tài liệu. Cấu trúc của kiểu MIME hoặc kiểu nội dung rất đơn giản; nó bao gồm một loại và một loại phụ, hai chuỗi, được phân tách bằng '/'. Không có không gian được cho phép. `Loại` đại diện cho danh mục và có thể là loại rời rạc hoặc nhiều phần. `loại phụ` dành riêng cho từng loại. Danh sách các loại, nằm trong danh mục Loại nội dung, dài nhưng một số loại nội dung quan trọng như sau:


|**Loại**|**Mô tả**|**Ví dụ về các loại phụ**
---|---|---|
|text|Thể hiện định dạng mà con người có thể đọc được|text/plain, text/html, text/css, text/javascript
|hình ảnh|Đại diện cho hình ảnh thuộc bất kỳ loại nào ngoại trừ video|hình ảnh/bmp, hình ảnh/png, hình ảnh/jpg, hình ảnh/gif
|audio|Đại diện cho mọi định dạng tệp âm thanh|audio/mdi, audio/wav
|application|Đại diện cho bất kỳ loại dữ liệu nhị phân nào|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Biểu diễn Tệp đính kèm trong Nội dung EML ###

Nội dung EML chứa các ranh giới cho từng loại nội dung mà nó chứa. Tệp đính kèm trong nội dung thư được xác định bởi Loại nội dung và Bố trí nội dung như trong ví dụ sau:

Loại nội dung: văn bản/đồng bằng; bộ ký tự#"windows-1252"; name#"apple app store.txt"
Nội dung-Bố trí: tập tin đính kèm; tên tệp#"apple app store.txt"
Mã hóa chuyển nội dung: base64
Id tệp đính kèm X: f_jkhztmd02

Như có thể thấy, Bố trí nội dung được đặt thành tệp đính kèm cho phép các ứng dụng đọc nhận thông tin tệp đính kèm như tên tệp đính kèm và mã hóa chuyển. Thông tin tiêu đề tệp đính kèm được theo sau bởi nội dung tệp đính kèm được mã hóa sẽ được đọc.

#### Ví dụ về Bảng tính dưới dạng Tệp đính kèm ####

Loại nội dung: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; tên#"english_spodr.xlsx"
Nội dung-Bố trí: tập tin đính kèm; tên tập tin#"english_spodr.xlsx"
Mã hóa chuyển nội dung: base64
Id tệp đính kèm X: f_jkhztmd43

## Người giới thiệu

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

