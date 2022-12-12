{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Định dạng tệp Apple Mail",
  "description":"Tìm hiểu về định dạng tệp EMLX và các API có thể tạo và mở tệp EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp EMLX là gì?

Định dạng tệp EMLX được Apple triển khai và phát triển. Ứng dụng Apple Mail sử dụng định dạng tệp EMLX để xuất email. Cũng có những ứng dụng khác có thể mở tệp EMLX và chuyển đổi chúng sang các định dạng tệp khác.

## Lịch sử tóm tắt về định dạng tệp EMLX

Hệ điều hành Mac OS X đã sử dụng chương trình email hiện có, NeXTMail, do NeXT tạo ra như một phần của hệ điều hành NeXTSTEP. Apple sau khi mua lại NeXT đã nâng cấp các tính năng của nó và nó trở thành ứng dụng email Apple Mail hiện được sử dụng làm ứng dụng thư khách mặc định. Email được xuất qua Apple Mail được lưu trực tiếp dưới dạng tệp EMLX. Ngoài ra, nó là ứng dụng thư mặc định cho các tệp EMLX khi ai đó mở các tệp này bằng cách nhấp đúp vào Mac OS.

## Định dạng tệp EMLX

Các tệp EMLx là các tệp dựa trên văn bản đơn giản có thể được mở trong bất kỳ trình soạn thảo văn bản nào như Notepad. Cấu trúc tệp EMLX bao gồm ba phần:

* Số byte cho tin nhắn - Độ dài của tin nhắn, được viết bằng ASCII ở dạng thập phân, kết thúc bằng 0x0a
* Bản thân tin nhắn
* Siêu dữ liệu tin nhắn ở dạng XML plist

Những điều này có thể được giải thích rõ hơn với sự trợ giúp của email mẫu sau đây được trích xuất từ Apple Mail dưới dạng EMLX và mở trong trình soạn thảo văn bản.

### Ví dụ EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1] (******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

Trong ví dụ này, 875 hiển thị tổng độ dài của tin nhắn. Siêu dữ liệu tin nhắn được đính kèm trong<plist> thẻ và cờ được mô tả như sau:

|Trường|Mô tả|Giá trị
---|---|---|
|0|đọc|1 << 0
|1|đã xóa|1 << 1
|2|đã trả lời|1 << 2
|3|đã mã hóa|1 << 3
|4|được gắn cờ|1 << 4
|5|gần đây|1 << 5
|6|bản nháp|1 << 6
|7|ban đầu (không còn được sử dụng)|1 << 7
|8|đã chuyển tiếp|1 << 8
|9|được chuyển hướng|1 << 9
|10-15|số tệp đính kèm|3F << 10 (6 bit)
|16-22|mức ưu tiên|7F << 16 (7 bit)
|23|đã ký|1 << 23
|24|là rác|1 << 24
|25|không phải rác|1 << 25
|26-28|cỡ chữ delta|7 << 26 (3 bit)
|29|mức thư rác được ghi lại|1 << 29
|30|tô sáng văn bản trong toc|1 << 30
|31|(không sử dụng)|

## Xem thêm ##

* [EML](/vi/email/eml/)
* [MSG](/vi/email/msg/)

