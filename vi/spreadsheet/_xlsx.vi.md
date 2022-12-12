{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết tệp _XLSX là gì và các API có thể tạo và mở tệp _XLSX.",
  "title" :"Tệp _XLSX là gì?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Tệp _XLSX là gì?

Tệp có phần mở rộng .\_xlsx thực chất là tệp [XLSX](/vi/spreadsheet/xlsx/) được đổi tên bởi một số ứng dụng khác. Điều này có thể xảy ra trong một số trường hợp khi tên tệp chứa phần mở rộng . ở cuối tên tệp. Các tệp \_XLSX có thể được mở trong Microsoft Excel tương tự như các tệp XLSX bằng cách đổi tên lại các tệp này thành phần mở rộng .xlsx.

## Định dạng tệp _XLSX - Thông tin khác

Tệp _XLSX không khác gì tệp XLSX và sử dụng tiêu chuẩn Open XML được Microsoft áp dụng từ năm 2000. Trước XLSX, [XLS](/vi/spreadsheet/xls/) là định dạng tệp chính được sử dụng để làm việc với bảng tính Excel nhằm lưu tài liệu ở định dạng nhị phân. Định dạng tệp dựa trên XML mới này có các ưu điểm như kích thước tệp nhỏ, khả năng chống hỏng tệp và biểu diễn hình ảnh có định dạng tốt. Định dạng tệp dựa trên XML mới này đã trở thành một phần của Office 2007 và cũng được thực hiện trong các phiên bản mới của Microsoft.

## Thông số định dạng tệp \_XLSX

Vì tệp \_XLSX là tệp XLSX được đổi tên nên tệp này có cùng thông số kỹ thuật với tệp gốc. Nó chỉ là một tệp lưu trữ dựa trên định dạng tệp lưu trữ [ZIP](/vi/compression/zip/). Nếu bạn muốn xem nội dung của kho lưu trữ này, chỉ cần đổi tên tệp thành phần mở rộng .zip và giải nén nó để xem các tệp cấu thành của sổ làm việc Excel này. Một sổ làm việc trống, khi được giải nén vào các tệp của nó, có các tệp và thư mục cấu thành sau đây.

### [Content_Types].xml

Đây là tệp duy nhất được tìm thấy ở cấp độ cơ sở khi giải nén zip. Nó liệt kê các loại nội dung cho các phần trong gói. Tất cả các tham chiếu đến các tệp XML có trong gói đều được tham chiếu trong tệp XML này.

### \_rels (Thư mục)

Đây là thư mục Mối quan hệ chứa một tệp XML duy nhất lưu trữ các mối quan hệ ở cấp độ gói. Liên kết đến các phần chính của tệp Xlsx được chứa trong tệp này dưới dạng URI. Các URI này xác định loại mối quan hệ của từng phần chính với gói. Điều này bao gồm mối quan hệ với tài liệu văn phòng chính nằm ở dạng xl/workbook.xml và các phần khác trong docProps dưới dạng thuộc tính cốt lõi và mở rộng.

### docProps

Thư mục này chứa các thuộc tính tài liệu tổng thể. Chúng bao gồm một tập hợp các thuộc tính cốt lõi, một tập hợp các thuộc tính mở rộng hoặc dành riêng cho ứng dụng và bản xem trước hình thu nhỏ của tài liệu. Sổ làm việc trống có hai tệp trong thư mục này là app.xml và core.xml. Core.xml chứa thông tin như tác giả, ngày tạo, lưu và sửa đổi. App.xml chứa thông tin về nội dung của tệp.

### xl (Thư mục)

Đây là thư mục chính chứa tất cả các chi tiết về nội dung của sổ làm việc. Theo mặc định, nó có các thư mục sau:

* \_rels
* chủ đề
* bảng tính

và các tệp xml sau:

* style.xml
* sổ làm việc.xml

## Người giới thiệu

* [Định dạng tệp MS-XLSX - .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

