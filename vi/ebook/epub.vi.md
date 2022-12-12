{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "file", "extension", "format", "E-Book", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp EPUB và các API có thể tạo và mở tệp EPUB.",
  "title" :"Tệp EPUB là gì?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Tệp EPUB là gì?

Các tệp có phần mở rộng .epub là định dạng tệp sách điện tử cung cấp định dạng xuất bản kỹ thuật số tiêu chuẩn cho nhà xuất bản và người tiêu dùng. Định dạng này đã trở nên phổ biến đến mức nó được hỗ trợ bởi nhiều trình đọc sách điện tử và ứng dụng phần mềm. Ví dụ: trên Mac OS, phần mềm **Sách** được cài đặt sẵn cung cấp hỗ trợ để mở các tệp như vậy. Ngoài ra, có rất nhiều phần mềm tương thích dành cho điện thoại thông minh, máy tính bảng và máy tính. Tiêu chuẩn tệp EPUB được duy trì bởi [Diễn đàn xuất bản kỹ thuật số quốc tế ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). Phiên bản EPUB 3 cũng được xác nhận bởi Book Industry Study Group (BISG), một hiệp hội thương mại sách hàng đầu về các phương pháp hay nhất được tiêu chuẩn hóa, nghiên cứu, thông tin và sự kiện để đóng gói nội dung.

## Sơ lược về lịch sử định dạng tệp EPUB

* **Tháng 10 năm 2007** - EPUB 2.0 đã được phê duyệt
* **Tháng 9 năm 2010** - Bản cập nhật bảo trì đã được phát hành
* **Tháng 10 năm 2011** - Thông số kỹ thuật EPUB 3.0 có hiệu lực
* **Tháng 6 năm 2014** - Bản cập nhật bảo trì nhỏ đã được phát hành để thay thế phiên bản 3.0
* **Tháng 1 năm 2017** - EPUB 3.1 bắt đầu có hiệu lực

## Định dạng tệp EPUB

Định dạng tệp EPUB là một tệp lưu trữ có thể được đổi tên thành tiện ích mở rộng [ZIP](/vi/compression/zip/) và có thể xem nội dung của nó bằng cách giải nén tệp lưu trữ bằng bất kỳ trình giải nén tệp lưu trữ nào. Nó là một định dạng dựa trên XML mở và bao gồm các tệp HTML, hình ảnh, biểu định kiểu CSS và các phần tử khác. Nó cũng có thể được chuyển đổi thành PDF, Mobi và một số định dạng tệp khác thông qua một số ứng dụng phần mềm và API.

{{< figure src="../epub.png" alt="Định dạng tệp EPUB" >}}

**Sách điện tử EPUB được mở bằng Ứng dụng Sách Mac OS**

Định dạng tệp EPUB dựa trên ba tiêu chuẩn mở sau đây.

### Cấu trúc công khai mở (OPS) ###

Tệp EPUB 2.0 sử dụng XHTML 1.1 để xây dựng nội dung của ấn phẩm. Về bản chất, điều này có nghĩa là tệp EPUB bao gồm một hoặc nhiều trang web. Mặc dù bạn có thể bao gồm toàn bộ nội dung của một cuốn sách hoặc tờ báo trong một trang, tốt hơn hết là tệp đó không vượt quá 300K, cả vì lý do hiệu suất và khả năng tương thích. Cũng giống như các trang web thông thường, kiểu dáng và bố cục được xác định bằng biểu định kiểu xếp tầng (CSS). Trong các tệp EPUB, cần sử dụng một tập hợp con (chuỗi lệnh giới hạn) của CSS2. Nhiều tính năng mới của CSS3, chẳng hạn như hộp tròn hoặc bóng đổ, vẫn chưa khả dụng. Để tương thích ngược, người sáng tạo cũng có thể sử dụng DTBook thay vì XHTML để mã hóa nội dung.

### Mở Định dạng Đóng gói (OPF) ###

Phần này của thông số kỹ thuật liên quan đến thông tin cấu trúc, chẳng hạn như siêu dữ liệu (tác giả và nhà xuất bản là ai, tiêu đề là gì,..), tệp kê khai (danh sách tất cả các tệp bên trong tệp epub) và mục lục. Những dữ liệu này đều được nhúng bằng XML.

### Định dạng vùng chứa mở (OCF) ###

Như các mô tả ở trên đã làm rõ, tài liệu EPUB bao gồm một loạt tệp. Thông số kỹ thuật OCF xác định cách tất cả các tệp đó được đóng gói trong một tệp vùng chứa duy nhất. Nén ZIP được sử dụng cho việc này.

## Định dạng tệp hình ảnh được hỗ trợ ##

Định dạng tệp EPUB hỗ trợ các định dạng tệp hình ảnh sau.

* [GIF](/vi/image/gif/)
* [JPG](/vi/image/jpeg/)
* [PNG](/vi/image/png/)
* [SVG](/vi/page-description-language/svg/)

## Người giới thiệu ##

* [EPUB - Theo Wikipedia](https://vi.wikipedia.org/wiki/EPUB)

