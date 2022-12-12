{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp HDM - Tệp ngôn ngữ đánh dấu thiết bị cầm tay",
  "description":"Tìm hiểu về định dạng tệp HDM và API có thể tạo và mở tệp HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Tệp HDM là gì?

Tệp HDM là tệp trang web ngôn ngữ đánh dấu được tạo bằng Ngôn ngữ đánh dấu thiết bị cầm tay (HDML). Nó chứa các thẻ đánh dấu tương tự như ngôn ngữ [HTML](/vi/web/html/), nhưng được thiết kế cho các thiết bị điện tử cầm tay như điện thoại thông minh và PDA. [Thông số định dạng tệp HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) đã được gửi tới W3C để chuẩn hóa nhưng không thể trở thành tiêu chuẩn. HDM dựa trên thông số kỹ thuật định dạng tệp [HDML](/vi/web/hdml/) có sẵn tại trang web của W3.

## Định dạng tệp HDM - Thông tin khác

Tệp HDM bao gồm các thẻ đánh dấu được hiển thị cho trang web được thiết kế trực quan trên thiết bị cầm tay. Các tệp HDM được sao chép sang thiết bị bằng giao thức HDTP (Giao thức vận chuyển thiết bị cầm tay) thay vì giao thức HTTP được sử dụng cho các trang HTML.

## Phần tử tệp HDML

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

