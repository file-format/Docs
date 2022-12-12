{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp ngôn ngữ đánh dấu thiết bị cầm tay",
  "description":"Tìm hiểu về định dạng tệp HDML và API có thể tạo và mở tệp HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Tệp HDML là gì?

Tệp có phần mở rộng .hdml (Ngôn ngữ đánh dấu thiết bị cầm tay) là ngôn ngữ đánh dấu để tạo trang web cho các thiết bị điện tử cầm tay như máy tính cầm tay, điện thoại thông minh và thiết bị hiển thị thông tin. HDML được cho là phần mở rộng của ngôn ngữ [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML tương tự như HTML nhưng dành cho các thiết bị cầm tay và không dây có màn hình nhỏ như PDA, điện thoại di động, v.v. Nó đã được thay thế bằng WML mà nó đóng vai trò là một ảnh hưởng quan trọng.

## Định dạng tệp HDML - Thông tin khác

HDML là ngôn ngữ đánh dấu cho các thiết bị cầm tay dựa trên các thẻ đánh dấu tương tự như HTML. HDML đã được gửi tới W3C để chuẩn hóa nhưng nó chưa bao giờ trở thành tiêu chuẩn. Tuy nhiên, thông số định dạng tệp của nó có sẵn trên [trang web của W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) để tham khảo. [Cú pháp cho ngôn ngữ HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) có sẵn để nhà phát triển tham khảo và có thể được sử dụng để phát triển ứng dụng mẫu.

## Phần tử HDML

Sau đây là một loạt các phần tử cung cấp môi trường thời gian chạy cho HDML và được gọi là tác nhân người dùng.

|Phần tử|Mô tả|
---|---|
|Thẻ|Đây là khối xây dựng cơ bản của HDML, đồng thời hiển thị và cho phép người dùng tương tác với các thẻ thông tin. |
|Bộ bài|Thẻ HDML được nhóm lại với nhau thành bộ bài. Sàn HDML tương tự như trang HTML ở chỗ nó được xác định bằng URL [RFC1738] và là đơn vị nội dung được yêu cầu từ máy chủ và được lưu vào bộ đệm bởi tác nhân người dùng.|
|Actions|Actions có thể thuộc loại PREV, SOFT1-SOFT8 và HELP. Đây là những bản tóm tắt và được hỗ trợ trong giao diện người dùng theo cách cụ thể của tác nhân người dùng.|
|Hoạt động|Một hoạt động giống như một nhóm các thẻ có liên quan thực hiện một chức năng logic. Chúng có thể kéo dài một hoặc nhiều bộ bài. Mô hình trạng thái và điều hướng HDML được cấu trúc xung quanh các hoạt động.|
|Điều hướng dựa trên lịch sử|Tác nhân người dùng duy trì lịch sử của các thẻ được hiển thị cho người dùng. Mỗi thẻ được truy cập sẽ được thêm vào lịch sử thẻ. Tác nhân người dùng cho phép người dùng dễ dàng điều hướng trở lại thẻ trước đó trong lịch sử.|

## Người giới thiệu

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Thông số kỹ thuật HDML - Trường W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

