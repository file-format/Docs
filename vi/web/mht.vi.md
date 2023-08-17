{
  "date" : "2019-10-11",
  "keywords" :[ "mht","tệp mht", "định dạng tệp mht", "loại tệp mht", "tệp", "loại", "tệp mht là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - Định dạng tệp MIME HTML",
  "description" :"Tìm hiểu về Định dạng tệp MHT và API để tạo và mở tệp MHT.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Tệp MHT là gì?

Tệp có phần mở rộng .mht là định dạng tệp lưu trữ hỗ trợ MIME chứa các loại dữ liệu khác nhau trong một tệp. Nó có thể lưu trữ dữ liệu như văn bản, hình ảnh, kiểu dáng trang ở dạng tệp [CSS](/vi/web/css/), JavaScript và các tài nguyên khác dưới dạng tài nguyên được nhúng trong đó. Các tệp MHT, có loại tin nhắn MIME/rfc822, đóng gói tất cả nội dung của tệp HTML dưới dạng một tệp lưu trữ duy nhất để lưu trữ khi lưu trữ trên thiết bị lưu trữ. Các ứng dụng phần mềm như Microsoft Word cho phép bạn chuyển đổi tài liệu WORD sang MHT bằng cách xuất dưới dạng tệp MHT. Các tệp MHT có thể được mở bằng các trình duyệt phổ biến như Microsoft Internet Explore và Google Chrome.

## Định dạng tệp MHT

Giống như [MHTML](/vi/web/mhtml/), MHT cũng là một đóng gói MIME của các tài liệu HTML tổng hợp. Nội dung tài liệu bên trong tài liệu MHT, chẳng hạn như ảnh nội tuyến, biểu định kiểu, applet, v.v. được mã hóa MIME trong đó chúng được liên kết với tài nguyên gốc thông qua URI. Các ứng dụng email như Microsoft Outlook lưu trữ email (thường là [EML](/vi/email/eml/)) ở định dạng tệp MHT. Thông số kỹ thuật đầy đủ của định dạng tệp MHT có sẵn trong [RFC 822](https://tools.ietf.org/html/rfc822) và có thể tham khảo để phát triển ứng dụng phần mềm có thể xử lý tệp MHT.

## Sự khác biệt giữa MHT và MHTML

Trong khi lưu một trang trực tuyến, người dùng được yêu cầu chọn loại định dạng tệp mà trang trực tuyến phải được lưu trên hệ thống gốc. Điển hình nhất, người dùng bị nhầm lẫn giữa ngôn ngữ đánh dấu và định dạng tệp MHTML. Họ nhận thấy thật khó khăn khi thấy định dạng tệp đó lành mạnh hơn giữa những định dạng này.

Khi người dùng quyết định tránh lãng phí trang trực tuyến làm ngôn ngữ đánh dấu, thì một thư mục sẽ được hình thành, chứa nhiều tệp cho các nội dung khác nhau của trang, tức là các tệp hoàn toàn khác nhau được tạo cho văn bản, đồ họa, applet, v.v. Mặt khác, tiết kiệm trang trực tuyến dưới dạng MHTML tạo một tệp cho trang trực tuyến hoàn chỉnh. Tất cả các thành phần của trang cùng với đồ họa, liên kết và đơn vị vùng tệp thay thế được nhúng bên trong một tệp.

Đương nhiên, thật dễ dàng để xử lý các tệp MHT hoặc MHTML vì tệp đó có thể được bảo vệ và chia sẻ đơn giản qua e-mail. Tuy nhiên, đơn vị khu vực của tệp ngôn ngữ đánh dấu có nguy cơ bị mất thông tin do mất hoặc xóa dù chỉ một tệp có thể khiến toàn bộ thư mục ngôn ngữ đánh dấu trở nên vô dụng đối với người dùng.

## Người giới thiệu

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

