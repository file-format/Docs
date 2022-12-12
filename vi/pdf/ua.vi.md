{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PDF/UA",
  "description":"Tìm hiểu về định dạng tệp PDF/UA và các API có thể tạo và mở tệp PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Tập tin PDF/UA là gì? #

PDF/UA đã được xuất bản dưới dạng [Tiêu chuẩn ISO 14289-1](https://en.wikipedia.org/wiki/ISO_14289) vào tháng 8 năm 2012 và cho đến nay là định nghĩa hoàn chỉnh đầu tiên về tập hợp các yêu cầu đối với tài liệu PDF có thể truy cập toàn cầu. Thuật ngữ "có thể truy cập toàn cầu" đề cập đến cách hiểu rằng thông tin có trong tài liệu [PDF](/vi/pdf/) phải được mọi người nói chung và người khuyết tật nói riêng có thể truy cập bình đẳng và độc lập. Việc giới thiệu tiêu chuẩn PDF/UA có thể được coi là một bước quan trọng để tạo ra các công cụ và ứng dụng nhằm tạo và đọc nội dung PDF.

## Yêu cầu định dạng tệp ##

PDF/UA có một số yêu cầu xác định tại cơ sở đóng vai trò là bản chất của tiêu chuẩn này. Về cơ bản, những điều này dựa trên việc gắn thẻ các tệp PDF, nghĩa là tất cả các tài liệu PDF/UA phải được gắn thẻ đúng cách. Nó cũng yêu cầu các thẻ phải phù hợp về mặt ngữ nghĩa và theo thứ tự logic. Điều này đảm bảo rằng tài liệu cuối cùng được tạo bằng thông số kỹ thuật PDF/UA đáng tin cậy và dễ truy cập hơn. Điều này có thể khiến các tác giả PDF đặt câu hỏi liệu họ có cần biết mọi thứ về tất cả các yêu cầu như vậy không? May mắn thay, không phải như vậy vì các công cụ tuân thủ PDF/UA chịu trách nhiệm thêm và duy trì khả năng truy cập của PDF.

Các yêu cầu về định dạng tệp cho PDF/UA như sau.

* Nội dung được phân loại theo một trong hai cách: nội dung có ý nghĩa và đồ tạo tác như các phần tử trang trí. Tất cả nội dung có ý nghĩa phải được gắn thẻ và tích hợp vào cây cấu trúc của tất cả các thẻ trong tài liệu. Mặt khác, đồ tạo tác chỉ cần được đánh dấu như vậy.
* Nội dung có ý nghĩa phải được đánh dấu bằng các thẻ và cùng với các thẻ khác trong tài liệu, tạo thành một cây cấu trúc hoàn chỉnh.
* Nội dung có ý nghĩa phải được đánh dấu bằng các thẻ ngữ nghĩa thích hợp.
* Cây cấu trúc được tạo bởi các thẻ tài liệu phải phản ánh thứ tự đọc hợp lý của tài liệu.
* Chỉ có thể sử dụng các thẻ tiêu chuẩn được xác định trong PDF 1.7; nếu bất kỳ thẻ nào khác được sử dụng, mục nhập gán vai trò phải ghi lại thẻ tiêu chuẩn mà mỗi thẻ đại diện.
* Thông tin có thể không được truyền tải chỉ bằng các phương tiện trực quan (ví dụ: độ tương phản, màu sắc hoặc vị trí trên trang).
* Không cho phép nội dung nhấp nháy, nhấp nháy hoặc nhấp nháy, dù là hiệu ứng do JavaScript kiểm soát hay là một phần của bất kỳ video nào được nhúng trong PDF.
* Tiêu đề tài liệu phải được cung cấp và tài liệu phải được thiết lập sao cho tiêu đề (chứ không phải tên tệp) xuất hiện trong tiêu đề cửa sổ.
* Ngôn ngữ của tất cả nội dung phải được ghi chú và những thay đổi về ngôn ngữ phải được đánh dấu rõ ràng như vậy.

## Tuân thủ PDF/UA ##

Tiêu chuẩn PDF/UA xác định thông số kỹ thuật cho nội dung, trình đọc và công nghệ hỗ trợ. Ba khía cạnh này được liên kết với nhau dựa trên nội dung của tài liệu. Các yêu cầu tuân thủ cho từng trong số này như được đề cập dưới đây.

## Tập tin phù hợp ##

Các tệp tuân theo tiêu chuẩn PDF/UA phải chứa các tính năng hợp lệ theo [thông số kỹ thuật PDF 1.7](http://www.adobe.com/go/pdfreference). Tuy nhiên, nên loại trừ các tính năng bị cấm cụ thể bởi PDF/UA.

## Người đọc phù hợp ##

Trình đọc phù hợp phải tuân theo các quy tắc được đánh vần bởi thông số kỹ thuật của PDF 1.7. Cụ thể, nó sẽ hỗ trợ:

* tất cả các thẻ, thuộc tính và giá trị khóa được chỉ định cho khả năng truy cập. Nó cũng phải có khả năng xử lý và thể hiện chữ ký số, chú thích và Nội dung tùy chọn.
* xử lý và thể hiện chữ ký số, chú thích và Nội dung tùy chọn
* điều hướng tài liệu bằng nhiều cách khác nhau

## Tuân thủ Công nghệ Hỗ trợ ##

Một công nghệ hỗ trợ phù hợp bị ràng buộc để hỗ trợ các tính năng PDF/UA. Chúng bao gồm, ví dụ, các tính năng của nội dung và trình đọc, đồng thời phải cho phép điều hướng theo nhãn trang, cấu trúc tài liệu hoặc dàn bài. Nó cũng sẽ cho phép người dùng ghi đè thu phóng điều hướng mặc định.

## Người giới thiệu ##

* [PDF/UA - Theo Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [Tóm tắt PDF/UA](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

