{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Tìm hiểu về định dạng tệp TNEF và các API có thể tạo và mở tệp TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp TNEF là gì?

Định dạng đóng gói trung tính vận chuyển (TNEF) là tài sản độc quyền của Microsoft, để đóng gói các tệp đính kèm email dựa trên Giao diện lập trình ứng dụng nhắn tin (**MAPI**). Microsoft Outlook và Microsoft Exchange Server, hoàn toàn hỗ trợ TNEF trong khi sau đó giải mã TNEF thành MAPI và hiển thị các thư được định dạng. Tệp đính kèm email có mã hóa TNEF có loại MIME là MS-TNEF và lưu trữ dưới dạng winmail/win.dat. Tệp đính kèm trong winmail .dat bao gồm các thông tin sau:


|Tin nhắn|Đối tượng OLE|Các tính năng của Outlook
---|---|---|
|<ul><li> Tệp đính kèm thư gốc</li><li> Phiên bản định dạng gốc</li><li> phông chữ, kích thước văn bản và màu văn bản</li></ul> |<ul><li> hình ảnh nhúng</li><li> nhúng tài liệu Office</li></ul> |<ul><li> hình thức tùy chỉnh</li><li> nút biểu quyết</li><li> yêu cầu họp</li></ul>


Các dịch vụ email khác không hỗ trợ TNEF, hiển thị văn bản thuần túy cho các thư có định dạng TNEF. Outlook nhúng định dạng phong phú của thư trong tệp TNEF (OLE) hoặc các tính năng cụ thể của Outlook (biểu mẫu, nút bỏ phiếu và yêu cầu hội nghị). Tuy nhiên, việc xử phạt mã hóa TNEF rõ ràng trong ứng dụng email khách Outlook là không thể, tuy nhiên, Chọn định dạng RTF để gửi e-mail hoàn toàn tạo điều kiện thuận lợi cho mã hóa TNEF.

## Định dạng tệp TNEF

Thuật toán dữ liệu TNEF thiết lập cấu trúc phẳng từ các thuộc tính thông báo phân cấp phong phú. Sau đó, các cấu trúc phẳng này được sử dụng để biểu diễn luồng dữ liệu nối tiếp bao gồm các thuộc tính cụ thể.

Trong một số trường hợp, khi các thuộc tính xuất hiện theo nhóm hoặc có nhiều giá trị, luồng có thể bao gồm số lượng và phần đệm để thực thi cách sắp xếp dữ liệu cụ thể. Một tình huống đặc biệt mà việc sử dụng thuật toán này có lợi là trong môi trường nhắn tin không hỗ trợ. Trong những môi trường như vậy, thuộc tính thông báo phong phú được mã hóa thành luồng dữ liệu nối tiếp bởi Trình ghi TNEF. Hơn nữa, các thuộc tính không thuộc TNEF cơ bản có thể được đóng gói trong quá trình truyền. Các thuộc tính được đóng gói này sau đó được cung cấp bằng cách giải mã thông qua TNEF để đảm bảo tính khả dụng của tất cả các thuộc tính của thông báo gốc cho ứng dụng khách.

Trong TNEF, tất cả các kiểu dữ liệu số đều là little-endian và kích thước của chúng lớn hơn một byte. Việc xử lý các giá trị số này trên các nền tảng không phải là little-endian yêu cầu thực hiện các phép biến đổi thích hợp để nhận được các giá trị chính xác. Giá trị chuỗi được thể hiện ở định dạng Augmented Backus-Naur Form (ABNF) theo thông số kỹ thuật của [RFC5234]. Khi chuỗi kết thúc bằng ký tự null, nó cũng được bao gồm; ví dụ: "worker@specimen.com" %x00.

{{< figure src="../TNEF.png" alt="Định dạng tệp TNEF" >}}

## Thuộc tính TNEF và quy tắc xử lý ##

Luồng dữ liệu trong TNEF bắt đầu bằng số phiên bản kế thừa, chữ ký, giá trị khóa nguyên thủy và trang mã đại diện cho thuộc tính. Trang mã này được tạo khi bộ mã hóa ghi lại các thuộc tính và thuộc tính ANSI. Sau đó, luồng trở thành một loạt các thuộc tính, trong đó các thuộc tính thông báo được xếp trước và sau đó là các thuộc tính tệp đính kèm. Các đặc điểm của thông báo và tệp đính kèm khác nhau được chứa trong các thuộc tính đặc biệt như attMsgProps, attAttachment và attRecipTable. Các thuộc tính xuất hiện trong luồng TNEF chứa cấu trúc, thuộc tính thông báo và chuyển đổi cần thiết để thu hút họ bằng các thuộc tính thông báo. Mỗi thuộc tính bao gồm ID, kích thước và dữ liệu của thuộc tính, tổng kiểm tra và cấp độ theo ứng dụng của nó.

## Mối quan hệ với các giao thức và thuật toán khác ##

Các hệ thống có cơ chế kém để hiển thị định dạng thông báo phong phú vốn cần thuật toán dữ liệu TNEF để truyền tải. Sử dụng loại phương tiện ms-TNEF, đầu ra của thuật toán bao gồm một tệp đính kèm (winmail.dat) và một phần nội dung của MIME được chỉ định trong [RFC2045]. Nội dung tin nhắn văn bản thuần túy được truyền bằng cách sử dụng UUENCODE theo thông số [MSDN-UAF] và nội dung tin nhắn này hoặc phương thức tương đương được giải mã ở đầu người nhận. Hơn nữa, TNEF có thể truyền dữ liệu tin nhắn bằng các giao thức internet khác nhau như SMTP, POP3, IMAP4 và các giao thức tích hợp MIME theo tiêu chuẩn RFC2045.

## Tuyên bố về khả năng áp dụng ##

Ngoài việc truyền thông báo đơn giản, ứng dụng ban đầu của TNEF đã được tạo để sử dụng các lớp thông báo và hỗ trợ các tính năng bổ sung không có hỗ trợ ban đầu trong giao thức truyền tải. Ứng dụng này đã được tinh chỉnh thêm để truyền các thuộc tính tin nhắn phong phú và các thuộc tính được đặt tên mà các ứng dụng nhắn tin hiện đại sử dụng ngày nay. Để phù hợp với triển khai ban đầu, cú pháp thuộc tính ban đầu được duy trì và một thuộc tính đặc biệt giữ các thuộc tính thông báo mới một cách riêng biệt.

## Người giới thiệu

* [Định dạng đóng gói trung lập vận chuyển](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Địa chỉ email và sổ địa chỉ trong Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Thuật toán dữ liệu định dạng đóng gói trung tính vận chuyển (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

