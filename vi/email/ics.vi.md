{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - Định dạng tệp iCalendar",
  "description":"Tìm hiểu về định dạng tệp ICS và API có thể tạo và mở tệp ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp ICS là gì?

Đặc tả đối tượng lõi lập lịch và lập lịch trên Internet (iCalendar) là một tiêu chuẩn internet (RFC 2445) để trao đổi và triển khai các sự kiện và lên lịch lập lịch. Định dạng iCalendar có thể tương tác với nhau, do đó đảm bảo việc trao đổi thông tin lịch giữa những người dùng có các ứng dụng email khác nhau. iCalendar định dạng dữ liệu đầu vào dưới dạng Phần mở rộng Thư Internet Đa năng (MIME) và tạo điều kiện thuận lợi cho đối tượng được trao đổi qua các giao thức truyền tải khác nhau. Các giao thức vận chuyển này có thể là SMTP, HTTP, giao tiếp không đồng bộ điểm-điểm và vận chuyển mạng dựa trên phương tiện vật lý.

iCalendar cho phép người dùng chia sẻ các sự kiện, công việc phụ thuộc vào ngày/giờ và thông tin rảnh/bận qua email tới những người dùng khác có thể phản hồi lại. Các tệp iCalendar lưu trữ bằng các hậu tố ".ics" ".iCalendar" hoặc ".ifb" với loại MIME là "văn bản/lịch". iCalendar được duy trì để tự chủ mà không phụ thuộc vào giao thức truyền tải. Các máy chủ web (với giao thức HTTP) có thể vận chuyển thông tin iCalendar và các trang web có thể chứa dữ liệu iCalendar ở dạng nhúng bằng cách sử dụng iCalendar.

## Lịch sử tóm tắt về định dạng tệp ICS

Năm 1998, Lực lượng Đặc nhiệm Kỹ thuật Internet (IETF) đã xác định iCalendar là một tiêu chuẩn (RFC 2445). Tiêu chuẩn được tài liệu hóa bởi Frank Dawson (Lotus Notes Corporation) và Derik Stenerson (Microsoft). Vào năm 2009, tiêu chuẩn đã được tinh chỉnh lại bởi Bernard Desruisseaux (Oracle) với tên gọi RFC 5545. Lần này, một số tính năng mới đã được thêm vào và một số tính năng lỗi thời không được dùng nữa. Vào năm 2016, RFC 7986 đã được phát hành và bổ sung cho iCalendar RFC ban đầu. RFC 7986 đã thêm các đặc điểm mới vào đối tượng VCALENDAR chính và các tính năng hỗ trợ mới cũng được giới thiệu cho các hệ thống hội nghị.

## Định dạng tệp ICS ##

Loại MIME được dữ liệu của iCalendar sử dụng là “văn bản/lịch”. Bộ ký tự mặc định cho iCalendar là UTF-8, tuy nhiên, bằng cách cung cấp các tham số trong MIME, bạn có thể sử dụng một bộ ký tự khác. Tệp iCalendar chứa các phần, trong số các phần này "VCALENDAR", là phần chung bao gồm tất cả các phần khác. Phần VEVENT xác định các sự kiện, VTODO liệt kê tất cả các mục công việc, VJOURNAL chứa các mục nhật ký và VTIMEZONE chỉ định thông tin về múi giờ. nhiều phần của danh mục tương tự được cho phép. Đối với nhiều sự kiện, nhiều phần VEVENT có thể xuất hiện trong tệp iCalendar.

### Dòng nội dung ###

Các đối tượng iCalendar được sắp xếp thành các dòng văn bản riêng biệt “dòng nội dung”. Ở định dạng tệp này, chuỗi CRLF kết thúc một dòng trong khi độ dài của dòng được giới hạn ở 75 octet không bao gồm ngắt dòng. Một mục dữ liệu dài có thể được kéo dài thành nhiều dòng.

### Dấu tách danh sách và trường ###

Các thuộc tính và tham số chỉ định danh sách các giá trị được phân tách bằng ký tự COMMA. Chuỗi trích dẫn được sử dụng cho các giá trị tham số dựa trên URI. Danh sách các tham số có thể được xây dựng theo giá trị thuộc tính. Mỗi tham số thuộc tính trong danh sách này phải được phân tách bằng Dấu chấm phẩy.

Trong một danh sách giá trị, một SEMICOLON cô lập các tham số thuộc tính và một COMMA các giá trị thuộc tính riêng biệt. Ví dụ được đưa ra dưới đây:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Nhiều giá trị

Một số thuộc tính có thể có nhiều giá trị. Chỉ cần tạo một dòng nội dung mới với tên thuộc tính là quy tắc cơ bản cho các thuộc tính đa giá trị. Tuy nhiên, đối với một giá trị có nhiều biến thể ngôn ngữ không được sử dụng các thuộc tính đa giá trị.

### Nội dung nhị phân

Trong đối tượng iCalendar, giá trị thuộc tính có thể tham chiếu dữ liệu nội dung nhị phân được đặt trong thực thể MIME bên ngoài bằng URI. Nội dung nhị phân nội tuyến có thể được sử dụng trong các tình huống đặc biệt với tham số "ENCODING", trong đó ứng dụng cần thể hiện một đối tượng iCalendar dưới dạng một thực thể duy nhất. Ví dụ sau giải thích thuộc tính "ATTACH" bằng tham chiếu URI:

ĐÍNH KÈM: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Bộ ký tự

Mặc dù lược đồ bộ ký tự mặc định cho iCalendar là UTF-8 nhưng không có tham số thuộc tính nào được chỉ định để xác định bộ ký tự của giá trị thuộc tính. trong MIME chuyển tham số "bộ ký tự" PHẢI được sử dụng cho bộ ký tự hiện có.

## Người giới thiệu

* [Đặc tả đối tượng lõi lập lịch và lập lịch trên Internet](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalWiki#History_and_design)

