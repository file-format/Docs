{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "tệp", "phần mở rộng", "định dạng tệp", "Excel Open XML", "Bảng tính" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết tệp XLTX là gì và các API có thể tạo và mở chúng.",
  "title" :"Tệp XLTX là gì?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Tệp XLTX là gì?

Các tệp có phần mở rộng .xltx đại diện cho các tệp Mẫu Microsoft Excel dựa trên các đặc tả định dạng tệp Office OpenXML. Nó được sử dụng để tạo một tệp mẫu tiêu chuẩn có thể được sử dụng để tạo các tệp [XLSX](/vi/spreadsheet/xlsx/) thể hiện các cài đặt giống như được chỉ định trong tệp XLTX.

## Tóm tắt lịch sử

Đó là vào đầu năm 2000 khi Microsoft quyết định thực hiện thay đổi để phù hợp với tiêu chuẩn cho **Office Open XML**. Các tài liệu, thuộc các loại khác nhau, theo Tiêu chuẩn mới này được xác định bằng cách thêm "X" vào phần mở rộng của chúng, trong đó "X" là XML. Đến năm 2007, định dạng tệp mới này đã trở thành một phần của Office 2007 và cũng được đưa vào các phiên bản mới của Microsoft Office. Loại tệp mới có thêm lợi thế về kích thước tệp nhỏ, ít thay đổi về hỏng hóc hơn và thể hiện hình ảnh được định dạng tốt.

## Thông số kỹ thuật định dạng tệp XLTX

Các tệp XLTX dựa trên định dạng tệp Office OpenXML và sử dụng XML và [ZIP](/vi/compression/zip/) để giảm kích thước tệp. Nó được tạo ra cùng với việc phát hành Microsoft Office 2007 để thay thế định dạng tệp XLT nhị phân. Tương tự như XLTX, định dạng tệp XLT có thể được sử dụng để tạo tệp [XLS](/vi/spreadsheet/xls/) bằng Microsoft Excel 2003 và 2007. Có thể mở các tệp này bằng Microsoft Excel bằng cách nhấp đúp vào tệp. Có thể quan sát tổ chức tệp ở định dạng tệp XLTX bằng cách đổi tên tệp thành ZIP và sau đó giải nén nội dung của nó vào đĩa.

### [Content_Types].xml ###

Đây là tệp duy nhất được tìm thấy ở cấp độ cơ sở khi giải nén zip. Nó liệt kê các loại nội dung cho các phần trong gói. Tất cả các tham chiếu đến các tệp XML có trong gói đều được tham chiếu trong tệp XML này.

### \_rels (Thư mục) ###

Đây là thư mục Mối quan hệ chứa một tệp XML duy nhất lưu trữ các mối quan hệ ở cấp độ gói. Liên kết đến các phần chính của tệp Xltx được chứa trong tệp này dưới dạng URI. Các URI này xác định loại mối quan hệ của từng phần chính với gói. Điều này bao gồm mối quan hệ với tài liệu văn phòng chính được đặt dưới dạng xl/workbook.xml và các phần khác trong docProps dưới dạng các thuộc tính mở rộng và cốt lõi.

### docProps ###

Thư mục này chứa các thuộc tính tài liệu tổng thể. Chúng bao gồm một tập hợp các thuộc tính cốt lõi, một tập hợp các thuộc tính mở rộng hoặc dành riêng cho ứng dụng và bản xem trước hình thu nhỏ của tài liệu. Sổ làm việc trống có hai tệp trong thư mục này là app.xml và core.xml. Core.xml chứa thông tin như tác giả, ngày tạo và lưu cũng như sửa đổi. App.xml chứa thông tin về nội dung của tệp.

### xl (Thư mục) ###

Đây là thư mục chính chứa tất cả các chi tiết về nội dung của sổ làm việc. Theo mặc định, nó có các thư mục sau:

* \_rels
* chủ đề
* bảng tính

và các tệp xml sau:

* style.xml
* sổ làm việc.xml

## Người giới thiệu ##

* [[MS-XLSX] - Định dạng tệp .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

