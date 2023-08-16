{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - Tệp hộp thư email",
  "description":"Tìm hiểu về định dạng tệp MBOX và API có thể tạo và mở tệp MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp MBOX là gì?

Định dạng tệp MBox là một thuật ngữ chung đại diện cho một vùng chứa để thu thập các thông báo thư điện tử. Các tin nhắn được lưu trữ bên trong vùng chứa cùng với tệp đính kèm của chúng. Các tin nhắn từ toàn bộ thư mục được lưu trong một tệp cơ sở dữ liệu duy nhất và các tin nhắn mới được thêm vào cuối tệp. Nhiều ứng dụng và API cung cấp hỗ trợ cho định dạng tệp MBox như Apple Mail và Mozilla Thunderbird.

## Định dạng tệp MBOX ##

Định dạng tệp MBox vẫn chưa được chuẩn hóa trong một thời gian khá dài cho đến năm 2005 khi ứng dụng/mbox được chuẩn hóa thành [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Tin nhắn, ở định dạng RFC 2822 , lần lượt được nối bên trong định dạng tệp MBox. Mỗi tin nhắn bắt đầu bằng một dòng phân cách xác định người gửi tin nhắn và cũng xác định ngày và giờ mà người nhận cuối cùng nhận được tin nhắn (hoặc hệ thống chặng cuối trong đường truyền hoặc hệ thống đóng vai trò là người nhận cửa hàng thư). Mỗi tin nhắn thường được kết thúc bằng một dòng trống. Phần cuối của cơ sở dữ liệu thường được nhận ra bởi sự vắng mặt của bất kỳ dữ liệu bổ sung nào hoặc bởi sự hiện diện của một điểm đánh dấu cuối tệp rõ ràng.

## Đọc tin nhắn từ tệp MBox ##

Trình đọc quét qua tệp mbox để tìm From_ lines. Bất kỳ dòng From_ nào đánh dấu phần đầu của thư. Người đọc không nên cố gắng lợi dụng thực tế là mọi dòng From_ (sau phần đầu của tệp) đều trống. Khi người đọc tìm thấy một tin nhắn, nó sẽ trích xuất người gửi phong bì (có thể bị hỏng) và ngày gửi ra khỏi dòng From_. Sau đó, nó sẽ đọc cho đến dòng From_ tiếp theo hoặc đến cuối tệp, tùy theo điều kiện nào đến trước. Nó loại bỏ dòng trống cuối cùng và xóa phần trích dẫn của >From_ lines và >>From_ lines, v.v. Kết quả là một thông báo RFC 822.

## Cân nhắc mã hóa ##

Nội dung của tệp MBox có thể bị trộn lẫn không thể đảo ngược khi email nhận được chứa tệp Mbox dưới dạng tệp đính kèm và được lưu trong tệp Mbox khác. Để tránh điều này, các hệ thống nhắn tin phải mã hóa cơ sở dữ liệu mbox bằng mã hóa truyền không trong suốt (chẳng hạn như BASE64 hoặc Có thể in được trích dẫn) bất cứ khi nào một đối tượng như vậy được truyền qua các giao thức nhắn tin. Người triển khai cũng nên sẵn sàng mã hóa cục bộ dữ liệu mbox nếu nhận được dữ liệu không tuân thủ.

## Người giới thiệu ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

