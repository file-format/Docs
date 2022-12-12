{
  "date" : "2019-10-11",
  "keywords" :[ "asp","tệp asp", "định dạng tệp asp", "loại tệp asp", "tệp", "loại", "tệp asp là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Định dạng tệp trang máy chủ hoạt động",
  "description" :"Tìm hiểu về tệp ASP là gì và các API có thể tạo và mở chúng.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp ASP là gì?

ASP là viết tắt của Active Server Pages, là một khung phát triển để tạo các trang web. Nó cho phép mã máy tính được thực thi bởi một máy chủ nội bộ để phục vụ các yêu cầu web. Khi yêu cầu được tạo cho tệp ASP bởi trình duyệt web, máy chủ sẽ đọc tệp và thực thi bất kỳ mã/tập lệnh nào bên trong tệp để tạo kết quả **[HTML](/vi/web/html/)** được trả về cho trình duyệt để hiển thị.

Không giống như các trang HTML, là các trang tĩnh do máy chủ phục vụ, các tệp ASP tạo nội dung động trong thời gian chạy có thể liên quan đến các yêu cầu dữ liệu từ cơ sở dữ liệu. Các trang ASP thường sử dụng phần mở rộng .asp thay vì .html. Vì mã/tập lệnh bên trong tệp ASP được thực thi ở phía máy chủ nên trình duyệt yêu cầu không thể thấy mã được sử dụng để tạo trang được cung cấp. Tất cả các trình duyệt hiện đại đều có khả năng hiển thị các trang được tạo ra. Được xây dựng trên công nghệ của Microsoft, các trang được xây dựng bằng ASP được lưu trữ trên các máy chủ Dịch vụ Thông tin Internet (IIS) của Microsoft.

## Lịch sử tóm tắt về định dạng tệp ASP
ASP đã trải qua một vài sửa đổi cho đến khi nó được thay thế bởi ASP.NET, một cách hiện đại hơn và hiệu quả hơn để phát triển và quản lý các trang phía máy chủ. Hỗ trợ cho ASP được bao gồm theo mặc định cùng với Dịch vụ Thông tin Internet (IIS). ASP đã được xuất bản trong ba phiên bản khác nhau với những cải tiến trong từng phiên bản.

* ASP 1.0 được phát hành vào tháng 12 năm 1996 như một phần của IIS 3.0
* ASP 2.0 được phát hành vào tháng 9 năm 1997 như một phần của IIS 4.0
* ASP 3.0 được phát hành vào tháng 11 năm 2000 như một phần của IIS 5.0

## Đối tượng chức năng ASP

Các tệp ASP sử dụng các đối tượng phía máy chủ để xử lý các yêu cầu của người dùng và tạo các trang đầu ra để phục vụ cho người dùng. Mỗi đối tượng có một tập hợp các bộ sưu tập, thuộc tính và phương thức để xử lý các yêu cầu và phản hồi. Những đối tượng này bao gồm:

### Đối tượng yêu cầu

Khi trình duyệt yêu cầu một trang từ máy chủ, nó được gọi là yêu cầu. Đối tượng Request được sử dụng để lấy thông tin từ khách truy cập.

### Đối tượng phản hồi

Đối tượng Phản hồi ASP được sử dụng để gửi đầu ra cho người dùng từ máy chủ.

### Đối tượng máy chủ

Đối tượng ASP Server được sử dụng để truy cập các thuộc tính và phương thức trên máy chủ. Nó cho phép kết nối với cơ sở dữ liệu (ADO), hệ thống tệp và sử dụng các thành phần được cài đặt trên máy chủ.

### Đối tượng phiên

Một đối tượng phiên giống như một liên kết giữa trình duyệt của người dùng yêu cầu một trang từ máy chủ và chính máy chủ. Điều này đạt được nhờ một cookie được tạo bởi ASP và được gửi đến máy tính của người dùng. Đối tượng Phiên lưu trữ thông tin về hoặc thay đổi cài đặt cho phiên người dùng. Thông tin được lưu trữ trong một đối tượng Phiên được chia sẻ trên tất cả các trang của ứng dụng. Thông tin phổ biến được lưu trữ trong các biến phiên là tên, id và tùy chọn. Máy chủ tạo một đối tượng Phiên mới cho mỗi người dùng mới và hủy đối tượng Phiên khi phiên hết hạn.

### Đối tượng ứng dụng

Đối tượng Ứng dụng chứa thông tin sẽ được sử dụng bởi nhiều trang trong ứng dụng (như thông tin kết nối cơ sở dữ liệu). Thông tin có thể được truy cập từ bất kỳ trang nào. Thông tin cũng có thể được thay đổi ở một nơi và các thay đổi sẽ tự động được phản ánh trên tất cả các trang. Đối tượng Ứng dụng được sử dụng để lưu trữ và truy cập các biến từ bất kỳ trang nào, giống như đối tượng Phiên.

### Đối tượng ASPError

Đối tượng ASPError được triển khai trong ASP 3.0 và có sẵn trong IIS5 trở lên. Đối tượng ASPError được sử dụng để hiển thị thông tin chi tiết về bất kỳ lỗi nào xảy ra trong tập lệnh trong trang ASP.

**Lưu ý:** Đối tượng ASPError được tạo khi Server.GetLastError được gọi, vì vậy chỉ có thể truy cập thông tin lỗi bằng cách sử dụng phương thức Server.GetLastError.

## Người giới thiệu

* [ASP - Bởi W3C](https://www.w3schools.com/asp/default.asp)
* [Tạo trang ASP đơn giản](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

