{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Tệp mẫu email Microsoft Outlook",
  "description":"Tìm hiểu về định dạng tệp OFT và API có thể tạo và mở tệp OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp OFT là gì?

Các tệp có phần mở rộng .oft là các tệp mẫu được tạo bằng Microsoft Outlook. Sau đó, tập hợp bố cục được định dạng trước cho các mẫu thư được sử dụng để gửi email có thông tin chung nhằm tiết kiệm thời gian. Những tệp như vậy có thể được tạo bằng cách tạo một email mới, thêm thông tin cần thiết, sau đó sử dụng trình đơn thả xuống Lưu dưới dạng Mẫu Office (.oft) từ Microsoft Outlook. Người dùng có thể mở tệp OFT bằng cách nhấp đúp vào tệp đó và tệp sẽ mở trong ứng dụng được liên kết trên hệ thống cụ thể đó.

## Cấu trúc tệp OFT ##

Định dạng tệp .OFT sử dụng định dạng tệp [MSG](/vi/email/msg/) làm cơ sở. Điểm khác biệt duy nhất là các tệp OFT có CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) làm lớp lưu trữ (WriteClassStg), trong khi các tệp MSG sử dụng CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}).

Định dạng CFB_3 là cơ sở của tệp MSG. Mô hình dựa trên các khái niệm kho lưu trữ và luồng, khá gần với các thư mục và tệp. Do đó, một sự khác biệt lớn trong cái trước là toàn bộ hệ thống phân cấp, được đóng gói thành một tệp riêng biệt, được gọi là tệp ghép. Các đối tượng tạo thành các tệp thông báo và bao gồm một thuộc tính hoặc các bộ sưu tập của nó. Khả năng này tạo điều kiện cho các ứng dụng lưu trữ dữ liệu có cấu trúc phức tạp trong một tệp duy nhất. Định dạng này cũng chỉ định nhiều kho lưu trữ, mỗi kho lưu trữ đại diện cho đối tượng Tin nhắn như một thành phần chính. Các kho lưu trữ này chứa một số luồng đại diện cho một thuộc tính của thành phần đó. Nesting lưu trữ cũng có thể.

### Thuộc tính OFT

Ở cấp cao nhất của tệp .msg, kho lưu trữ chứa các luồng lưu trữ các thuộc tính trong đó. Các thuộc tính có thể được phân loại như sau:

* Thuộc tính chiều dài cố định
* Thuộc tính độ dài thay đổi
* Thuộc tính đa giá trị

Không phân biệt danh mục, một thuộc tính được gắn thẻ hoặc được đặt tên. Tuy nhiên, thông tin ánh xạ phù hợp là bắt buộc đối với các thuộc tính được đặt tên như được chỉ định bởi bộ lưu trữ ánh xạ của chúng.

### Bộ lưu trữ OFT

Kho lưu trữ cấu thành các thành phần chính của đối tượng Tin nhắn. Định dạng tệp MSG nêu các kho lưu trữ sau:

### Cấu trúc cấp cao nhất

Đối tượng thông báo đại diện cho toàn bộ cấp cao nhất của định dạng tệp tin Msg. Tùy thuộc vào loại, thuộc tính, số lượng đối tượng người nhận và Tệp đính kèm, một đối tượng thông báo có thể có các kho lưu trữ luồng khác nhau trong tệp .MSG tương ứng của nó.

#### Mối quan hệ với các cấu trúc khác

Định dạng tệp MSG/OFT có các mối quan hệ sau với các cấu trúc khác:

* Cơ sở của .msg là Định dạng tệp nhị phân tệp hợp chất.
* Các thuộc tính được sử dụng bởi Giao thức Đối tượng Tin nhắn và Tệp đính kèm được sử dụng bởi định dạng này.

## Người giới thiệu

* [[MS-OXMSG]: Định dạng tệp MSG của Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

