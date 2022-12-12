{
  "date" : "2019-10-11",
  "keywords" :[ "tệp md", "định dạng tệp md", "tệp md là gì", "tệp", "ví dụ md", "phần mở rộng tệp md","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - Tệp ngôn ngữ MarkDown",
  "description":"Tìm hiểu về định dạng tệp MD và API có thể tạo và mở tệp MD.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp MD là gì?

Các tệp văn bản được tạo bằng phương ngữ ngôn ngữ Markdown được lưu với phần mở rộng tệp **.md** hoặc **.MARKDOWN**. Các tệp MD được lưu ở định dạng văn bản thuần túy sử dụng ngôn ngữ Markdown, ngôn ngữ này cũng bao gồm các ký hiệu văn bản nội tuyến, xác định cách định dạng văn bản, chẳng hạn như thụt lề, định dạng bảng, phông chữ và tiêu đề. Các tệp MD có thể được chuyển đổi thành HTML bằng chương trình có tên Markdown. Ngôn ngữ Markdown được phát hành bởi John Gruber.

Các tệp MD cũng có thể được phân loại là tệp dành cho nhà phát triển, phần lớn được Markdown sử dụng để chuyển đổi tệp văn bản sang phiên bản HTML để người dùng có thể tạo tệp dễ đọc và viết. Sau đây là các ứng dụng có thể mở tệp .md:

* Sổ tay Microsoft
* Sổ tay2
* Chỉnh sửa văn bản của Apple
*Microsoft WordPad

Một lời cảnh báo là không đổi tên phần mở rộng của tệp .md. Nếu vậy, điều này sẽ không thay đổi loại tệp vì có sẵn phần mềm chuyển đổi đặc biệt để thay đổi tệp từ loại này sang loại khác. Như đã thảo luận ở trên. Các tệp .MD là phần mở rộng của các tệp được tạo bằng phần mềm ngôn ngữ Markdown. **Markdown** là một [ngôn ngữ đánh dấu nhẹ](https://en.wikipedia.org/wiki/Lightweight_markup_language) dành cho một mục đích, dùng để định dạng văn bản trên web bằng cú pháp định dạng văn bản thuần túy. Hãy làm rõ rằng Markdown không phải là sự thay thế cho HTML vì cú pháp của nó rất nhỏ, chứa một tập hợp con rất nhỏ các thẻ HTML. Lý do đằng sau Markdown là để dễ đọc, viết và chỉnh sửa văn xuôi. Nói cách khác, chúng ta có thể nói rằng HTML là định dạng xuất bản trong khi Markdown là định dạng viết.

Markdown hiện là một trong những ngôn ngữ đánh dấu phổ biến nhất thế giới. Trong khi sử dụng Microsoft Word, việc định dạng các từ và cụm từ thông qua việc nhấp vào nút và các thay đổi sẽ hiển thị ngay lập tức. Nhưng Markdown không như vậy. Khi tệp định dạng Markdown được tạo, cú pháp Markdown được thêm vào văn bản để cho biết những từ và cụm từ nào có thể trông khác. Ví dụ: để hiển thị một tiêu đề, một ký hiệu số được thêm vào trước nó (ví dụ: # Heading One). Để tạo một câu in đậm, hai dấu hoa thị được thêm vào trước và sau nó (ví dụ: **văn bản này được in đậm**). Cú pháp đánh dấu có thể được nhìn thấy sau khi trong văn bản.

## Tóm tắt lịch sử

John Gruber và Aaron Swartz vào năm 2004 đã tạo ra ngôn ngữ Markdown với ý tưởng cho phép mọi người “viết bằng cách sử dụng định dạng văn bản thuần túy dễ đọc và dễ viết cùng với tùy chọn chuyển đổi sang XHTML hoặc HTML. Mục tiêu đằng sau thiết kế của nó là khả năng đọc – ngôn ngữ có thể đọc được mà không có vẻ như nó đã được gắn thẻ hoặc thêm các hướng dẫn định dạng như được thực hiện trong các ngôn ngữ đánh dấu như RTF hoặc HTML, nơi các thẻ và hướng dẫn định dạng là rõ ràng. Cảm hứng cơ bản là sử dụng các quy ước hiện có để đánh dấu văn bản thuần túy trong email.

Kể từ đó, Markdown đã được những người khác triển khai lại giống như trong [mô-đun] Perl(https://en.wikipedia.org/wiki/Modular_programming) có sẵn trên [CPAN](https://en.wikipedia.org/ wiki/CPAN) và bằng nhiều ngôn ngữ lập trình khác. Nó được phân phối theo [giấy phép kiểu BSD](https://en.wikipedia.org/wiki/BSD_license) và được bao gồm hoặc có sẵn dưới dạng plugin cho một số [hệ thống quản lý nội dung](https:// en.wikipedia.org/wiki/Content_manager_system).

## Thông số kỹ thuật

Khi một cái gì đó được viết bằng Markdown, trước tiên, văn bản được lưu trữ trong tệp văn bản gốc có phần mở rộng là .md hoặc .markdown, sau đó ứng dụng đánh dấu như Dillinger được sử dụng để xử lý tệp Markdown để chuyển văn bản có định dạng Markdown sang HTML để hiển thị trên web trình duyệt. Các ứng dụng Markdown sử dụng //bộ xử lý Markdown// (còn thường được gọi là "trình phân tích cú pháp" hoặc "triển khai") để lấy văn bản có định dạng Markdown và xuất nó sang định dạng HTML. Sơ đồ luồng của quy trình như sau:

Nói tóm lại, đó là một quy trình gồm bốn bước như sau:

1. Đầu tiên, tạo tệp Markdown bằng trình soạn thảo văn bản hoặc ứng dụng Markdown có phần mở rộng là .md hoặc .markdown.
1. Tệp Markdown sau đó được mở trong ứng dụng Markdown.
1. Ứng dụng Markdown được sử dụng để chuyển đổi tệp Markdown thành tài liệu HTML.
1. Tệp HTML sau đó được xem trong trình duyệt web hoặc ứng dụng Markdown được sử dụng để chuyển đổi tệp đó sang định dạng tệp khác, chẳng hạn như PDF.

Markdown nhanh chóng và dễ dàng để ghi chú, viết nội dung cho trang web, tạo tài liệu in sẵn, để xuất bản sách, tạo bản trình bày và tạo tài liệu.

Một số phiên bản trong markdown có tác động đáng kể đến các phiên bản khác đến mức người ta thường thấy chúng được trích dẫn như một phần của các phiên bản khác. Ví dụ: các thư viện đề cập đến hỗ trợ CommonMark (GFM). Chúng ta hãy có một cái nhìn ngắn gọn về những người.

### GFM
Markdown rất phổ biến với các nhà phát triển vì nền tảng chia sẻ mã nguồn mở Github đã chấp nhận và mở rộng ngôn ngữ này với một phiên bản có tên Github Flavored Markup (GFM) bao gồm các khối mã có hàng rào, liên kết tự động URL, gạch ngang, bảng và tạo việc cần làm.

### Dấu chung
Các nhà phát triển Markdown gần đây đã cố gắng chuẩn hóa markdown, họ đã cùng nhau tạo ra một phiên bản, các bài kiểm tra và tài liệu cho ngôn ngữ mạnh mẽ hơn và được gọi là CommonMark. Định dạng này hơi mới và không hỗ trợ nhiều tính năng, nhưng nhiều tính năng MultiMarkdown sẽ sớm được thêm vào.

### Đa Markdown
Multi-Markdown đã thêm nhiều tính năng khác nhau vào ngôn ngữ được các phiên bản khác hỗ trợ. Ban đầu nó được viết bằng Perl, nhưng sau đó được chuyển sang C. Nó hỗ trợ các khối mã có hàng rào, đánh dấu cú pháp, bảng, siêu dữ liệu, các đoạn/liên kết tham chiếu chéo, chú thích cuối trang, gạch ngang, danh sách định nghĩa, toán học.

## Người giới thiệu

* [Làm chủ MarkDown](https://guides.github.com/features/mastering-markdown/)

