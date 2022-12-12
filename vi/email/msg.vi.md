{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Định dạng email Microsoft Outlook",
  "description":"Tìm hiểu về định dạng tệp bột ngọt và các API có thể tạo và mở tệp bột ngọt.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp MSG là gì?

MSG là định dạng tệp được [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) và Exchange sử dụng để lưu trữ email , liên hệ, cuộc hẹn hoặc các tác vụ khác. Những thư như vậy có thể chứa một hoặc nhiều trường email, với người gửi, người nhận, chủ đề, ngày tháng và nội dung thư hoặc thông tin liên hệ, chi tiết cuộc hẹn và một hoặc nhiều thông số kỹ thuật của tác vụ. Các thuộc tính cấu thành đối tượng Tin nhắn, bao gồm cũng là một phần của tệp MSG. Tệp MSG có tiêu đề, nội dung thư chính và siêu liên kết dưới dạng văn bản ASCII thuần túy. Các tệp MSG cũng phù hợp với các chương trình cần Giao diện lập trình ứng dụng nhắn tin (MAPI) của Microsoft.

## Cấu trúc tệp bột ngọt

Định dạng CFB_3 là cơ sở của tệp MSG. Mô hình dựa trên các khái niệm kho lưu trữ và luồng, khá gần với các thư mục và tệp. Do đó, một sự khác biệt lớn trong cái trước là toàn bộ hệ thống phân cấp, được đóng gói thành một tệp riêng biệt, được gọi là tệp ghép. Các đối tượng tạo thành các tệp thông báo và bao gồm một thuộc tính hoặc các bộ sưu tập của nó. Khả năng này tạo điều kiện cho các ứng dụng lưu trữ dữ liệu có cấu trúc phức tạp trong một tệp duy nhất. Định dạng này cũng chỉ định nhiều kho lưu trữ, mỗi kho lưu trữ đại diện cho đối tượng Tin nhắn như một thành phần chính. Các kho lưu trữ này chứa một số luồng đại diện cho một thuộc tính của thành phần đó. Nesting lưu trữ cũng có thể.

## Thuộc tính Mapi

Ở cấp cao nhất của tệp .msg, kho lưu trữ chứa các luồng lưu trữ các thuộc tính trong đó. Các thuộc tính có thể được phân loại như sau:

* Thuộc tính chiều dài cố định
* Thuộc tính độ dài thay đổi
* Thuộc tính đa giá trị

Bất kể danh mục, một thuộc tính được gắn thẻ hoặc được đặt tên. Tuy nhiên, thông tin ánh xạ phù hợp là bắt buộc đối với các thuộc tính được đặt tên như được chỉ định bởi bộ lưu trữ ánh xạ của chúng.

## Kho lưu trữ

Kho lưu trữ cấu thành các thành phần chính của đối tượng Tin nhắn. Định dạng tệp MSG nêu các kho lưu trữ sau:

## Cấu trúc cấp cao nhất

Đối tượng thông báo đại diện cho toàn bộ cấp cao nhất của định dạng tệp MSG. Tùy thuộc vào loại, thuộc tính, số lượng đối tượng người nhận và Tệp đính kèm, một đối tượng thông báo có thể có các kho lưu trữ luồng khác nhau trong tệp .MSG tương ứng của nó.

### Mối quan hệ với các cấu trúc khác

Định dạng tệp Msg có các mối quan hệ sau với các cấu trúc khác:

* Cơ sở của .msg là Định dạng tệp nhị phân tệp hợp chất.
* Các thuộc tính được sử dụng bởi Giao thức Đối tượng Tin nhắn và Tệp đính kèm được sử dụng bởi định dạng này.

## Các tình huống để tránh các định dạng MSG

Đối tượng tin nhắn có thể được chia sẻ giữa các máy khách hoặc kho lưu trữ tin nhắn sử dụng hệ thống tệp .msg. Có một số trường hợp lưu trữ đối tượng Thư ở định dạng tệp .msg sẽ không phù hợp. Ví dụ:

* Trong trường hợp duy trì một kho lưu trữ độc lập lớn, tốt hơn là sử dụng định dạng đầy đủ tính năng trong đó các chế độ xem có thể được hiển thị chính xác hơn.
* Nếu người nhận không xác định, có thể định dạng không được đầu thu hỗ trợ và có thể được gửi ở chế độ riêng tư hoặc không liên quan.

## Ví dụ về tệp MSG

Để biết tệp MSG trông như thế nào, bạn có thể tải xuống [tệp MSG mẫu](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) và mở trên máy tính để xem nội dung của nó.

## Người giới thiệu

* [[MS-OXMSG]: Định dạng tệp MSG của Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

