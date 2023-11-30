{
"ngày": "2023-05-16",
  "keywords": [
"tập tin sami",
"tập tin sami là gì",
"ví dụ về tập tin sami",
"tài liệu",
"phần mở rộng tập tin sami",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp SAMI - Tệp trao đổi phụ đề và siêu dữ liệu",
  "description":"Tìm hiểu về định dạng SAMI và các API có thể tạo và mở tệp SAMI.",
"linktitle":"SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"lastmod": "2023-05-16"
}

## Tập tin SAMI là gì?

Tệp có phần mở rộng ".sami" thường đề cập đến tệp Trao đổi phụ đề và siêu dữ liệu (SAMI). SAMI là định dạng phụ đề được sử dụng để hiển thị phụ đề hoặc chú thích chi tiết trong video. Ban đầu nó được Microsoft phát triển cho Windows Media Player của họ.

Tệp SAMI chứa thông tin về thời gian và nội dung văn bản cho phụ đề, cho phép chúng được đồng bộ hóa với quá trình phát lại video. Định dạng này hỗ trợ các tùy chọn định dạng cơ bản như kiểu phông chữ, màu sắc và vị trí của phụ đề trên màn hình.

Tệp SAMI thường là tệp văn bản thuần túy và có thể được mở và chỉnh sửa bằng trình chỉnh sửa văn bản. Nội dung của tệp SAMI thường bao gồm phần tiêu đề cung cấp thông tin về tệp, theo sau là các mục phụ đề riêng lẻ kèm theo thời gian và văn bản tương ứng.

Sau đây là ví dụ về hình thức của tệp SAMI:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

Các tệp SAMI thường được sử dụng cùng với trình phát video hoặc trình phát phương tiện hỗ trợ hiển thị phụ đề, chẳng hạn như Windows Media Player hoặc VLC Media Player. Trình phát đọc tệp SAMI và đồng bộ hóa phụ đề với nội dung video, cho phép người xem đọc chú thích trong khi xem video.

## Thẻ HTML được hỗ trợ

Các tệp SAMI (Trao đổi phụ đề và siêu dữ liệu) hỗ trợ một bộ thẻ giống HTML có giới hạn để định dạng và tạo kiểu cho phụ đề. Dưới đây là một số thẻ thường được sử dụng bởi SAMI:

- ``<SAMI> :`` Phần tử gốc đóng gói toàn bộ tệp SAMI.
- ``<HEAD> :`` Chứa thông tin tiêu đề cho tệp SAMI.
<html>- ``<TITLE> :`` Chỉ định tiêu đề của tệp SAMI. </html>
- ``<BODY> :`` Bao gồm các mục phụ đề và thông tin thời gian của chúng.
- ``<SYNC> :`` Biểu thị điểm đồng bộ hóa cho mục nhập phụ đề. Nó chỉ định thời gian mà phụ đề sẽ được hiển thị.
- ``<P> :`` Bao gồm nội dung văn bản thực tế của phụ đề. Nó thường được sử dụng trong một<SYNC> khối.
<html>- `` <FONT>:`` Xác định thuộc tính phông chữ cho văn bản kèm theo. Các thuộc tính như Màu sắc, Khuôn mặt, Kích thước và Kiểu có thể được sử dụng để sửa đổi giao diện phông chữ.</font>
- ``<BR> :`` Chèn ngắt dòng trong phụ đề.
<html>- `` <B>:`` Hiển thị văn bản kèm theo ở dạng in đậm.</b>
<html>- `` <I>:`` Hiển thị văn bản kèm theo ở dạng in nghiêng.</i>
<html>- `` <U>:`` Hiển thị gạch chân văn bản kèm theo.</u>
- ``<C> :`` Chỉ định vị trí hoặc căn chỉnh của văn bản phụ đề trên màn hình. Nó hỗ trợ các thuộc tính như Center, Middle, Left, Right, Top, Bottom và sự kết hợp của chúng.
- ``<LANG> :`` Chỉ định mã ngôn ngữ cho văn bản phụ đề. Nó giúp xác định ngôn ngữ của phụ đề.

Đây là một số thẻ cơ bản được tệp SAMI hỗ trợ. Điều quan trọng cần lưu ý là SAMI không hỗ trợ đầy đủ các thẻ và thuộc tính HTML. Các thẻ được hỗ trợ chủ yếu tập trung vào việc tạo kiểu và định vị phụ đề thay vì cung cấp cấu trúc hoặc tính tương tác tài liệu mở rộng.

## Người giới thiệu
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

