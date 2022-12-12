{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "phần mở rộng", "tệp", "định dạng", "hệ thống", "tệp TMP", "tài liệu TMP", "tệp TMP", "Tệp tạm thời", "ứng dụng", "chương trình" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Định dạng tệp tạm thời",
  "description":"Tìm hiểu về định dạng tệp TMP và API có thể tạo và mở tệp TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Tệp TMP là gì? ##

Tệp TMP đề cập đến một bản sao lưu, lưu trữ tạm thời hoặc hệ thống tệp khác được tạo bởi một chương trình phần mềm. Đôi khi, nó được tạo dưới dạng một tệp vô hình và thường bị hủy khi thoát khỏi chương trình. Các tệp TMP cũng có thể được sử dụng để lưu trữ thông tin tạm thời trong khi một tệp mới đang được tạo.

## Định dạng tệp TMP ##

Tệp TMP thường được tạo thành từ dữ liệu thô được sử dụng như một giai đoạn trong quá trình chuyển đổi tài liệu từ kiểu này sang kiểu khác. Microsoft Word và Apple Safari là hai ứng dụng có thể tạo và sử dụng định dạng tệp TMP.

Về lý thuyết, các tài liệu TMP được tạo sẽ tự động bị xóa khi đóng chương trình hoặc tắt máy. Trong thực tế, điều này không phải lúc nào cũng đúng. Do đó, trong khi điều hướng qua các tài liệu của chương trình, bạn có thể bắt gặp các tệp tạm thời không được hệ thống hoặc bất kỳ phần mềm nào khác sử dụng tích cực.

### Bộ nhớ phụ ###

Bộ nhớ ảo được sử dụng trong các hệ điều hành, tuy nhiên, các chương trình sử dụng khối lượng thông tin khổng lồ có thể cần tạo các tài liệu tạm thời.

### Giao tiếp giữa các quá trình ###

Hầu hết các hệ điều hành cung cấp các nguyên mẫu để truyền dữ liệu giữa các chương trình, chẳng hạn như đường ống, ổ cắm hoặc bộ nhớ chính, nhưng phương pháp đơn giản nhất là chuyển tệp sang tệp tạm thời và thông báo cho ứng dụng nhận vị trí của tệp tạm thời.


## Đặc điểm kỹ thuật ##

Lấy tên tài liệu tạm thời đặc biệt thường được cung cấp bởi các hệ điều hành và chương trình phần mềm.
Các tệp tạm thời có thể được tạo một cách an toàn trên các hệ thống POSIX bằng các hàm thư viện mkstemp hoặc tmpfile. Một số hệ thống bao gồm ứng dụng mktemp POSIX (đã biến mất) trước đó. Các tệp này thường được tìm thấy trong thư mục tạm thời thông thường trên các nền tảng Unix trong/TMP hoặc %TEMP% (dành riêng cho đăng nhập) trên các máy Windows.

Khi chương trình dừng hoặc tài liệu bị đóng, tệp tạm thời được tạo bằng tmpfile sẽ tự động bị xóa. GetTempFileName (Windows) hoặc tmpnam (POSIX) có thể được sử dụng để tạo một tên tệp tạm thời sẽ tồn tại lâu hơn chương trình đã tạo ra nó.

## Tài liệu tham khảo ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
