{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "tệp", "phần mở rộng", "định dạng tệp", "Excel", "Bảng tính" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về tệp XLSX là gì và các API có thể tạo và mở tệp XLSX.",
  "title" :"Định dạng tệp XLSX - Tệp XLSX là gì?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Tệp XLSX là gì?

**XLSX** là định dạng nổi tiếng dành cho các tài liệu Microsoft Excel được Microsoft giới thiệu cùng với việc phát hành Microsoft Office 2007. Dựa trên cấu trúc được tổ chức theo Quy ước Đóng gói Mở như đã nêu trong [Phần 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) của tiêu chuẩn OOXML ECMA-376, định dạng mới là một gói zip chứa một số tệp XML. Cấu trúc cơ bản và các tệp có thể được kiểm tra bằng cách giải nén tệp .xlsx.

## Lịch sử tóm tắt về định dạng tệp XLSX

Định dạng tệp XLSX được giới thiệu vào năm 2007 và sử dụng tiêu chuẩn Open XML được Microsoft điều chỉnh từ năm 2000. Trước XLSX, định dạng tệp phổ biến được sử dụng là [XLS](/vi/spreadsheet/xls/) là định dạng tệp nhị phân thuần túy. Loại tệp mới có thêm lợi thế về kích thước tệp nhỏ, ít thay đổi về lỗi và biểu diễn hình ảnh được định dạng tốt. Đó là vào đầu năm 2000 khi Microsoft quyết định thực hiện thay đổi để phù hợp với tiêu chuẩn cho **Office Open XML**. Đến năm 2007, định dạng tệp mới này đã trở thành một phần của Office 2007 và cũng được đưa vào các phiên bản mới của Microsoft Office.

## Định dạng tệp XLSX Thông số kỹ thuật

[Thông số định dạng tệp XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) chính thức có sẵn trực tuyến từ Microsoft. Để xem nội dung bên trong tệp XLSX, chỉ cần đổi tên tệp thành tệp [ZIP](/vi/compression/zip/) bằng cách thay đổi phần mở rộng của tệp rồi giải nén tệp để xem các tệp cấu thành của sổ làm việc Excel này. Một sổ làm việc trống, khi được giải nén vào các tệp của nó, có các tệp và thư mục cấu thành sau đây.

### [Content_Types].xml ###

Đây là tệp duy nhất được tìm thấy ở cấp độ cơ sở khi giải nén zip. Nó liệt kê các loại nội dung cho các phần trong gói. Tất cả các tham chiếu đến các tệp XML có trong gói đều được tham chiếu trong tệp XML này.

### \_rels (Thư mục) ###

Đây là thư mục Mối quan hệ chứa một tệp XML duy nhất lưu trữ các mối quan hệ ở cấp độ gói. Liên kết đến các phần chính của tệp Xlsx được chứa trong tệp này dưới dạng URI. Các URI này xác định loại mối quan hệ của từng phần chính với gói. Điều này bao gồm mối quan hệ với tài liệu văn phòng chính nằm ở dạng xl/workbook.xml và các phần khác trong docProps dưới dạng thuộc tính cốt lõi và mở rộng.

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

## Ví dụ về định dạng XLSX ##


Đối với mỗi trang tính Excel có trong sổ làm việc, có một tệp XML. Bạn có thể tìm thấy các tệp XML này trong thư mục xl/worksheets. Tất cả thông tin chứa trong một trang tính được tổ chức thành các phần khác nhau trong tệp XML. Hãy xem xét một trang tính mẫu từ một sổ làm việc được hiển thị trong hình ảnh sau đây.

{{< figure src="../XLSX file format.png" alt="Định dạng tệp XLSX" >}}

Có thể thấy, trang tính này chứa nội dung trong các ô từ A1 đến B2 và một hình ảnh. Ngoài ra, ô G13 hiện là ô hiện hoạt trong trang tính. Bây giờ, hãy kiểm tra tệp xl/worksheets/sheet1.xml để xem cách thông tin này được trình bày trong tệp XML. Nội dung của tệp XML này như hình bên dưới.

{{< figure src="../XLSX File Format Details.png" alt="Định dạng tệp XPS" >}}

1. Tab được áp dụng màu chủ đề. Nó được đề cập trong tệp XML có thẻ<tabColor> theo id chủ đề.
1. Giá trị tabSelected được đặt thành 1 cho biết đây là trang tính đã chọn
1. Như có thể thấy trong hình đầu tiên ở trên, ô G13 trong trang tính là ô đang hoạt động cũng được đề cập trong tệp XML.
1. Tab sheetData đại diện cho dữ liệu chứa trong trang tính. Tuy nhiên, bạn có thể thấy rằng nội dung ban đầu của trang tính không có trong phần này. Điều này là do văn bản được gọi gián tiếp từ trang XML "sharedStrings". Liên kết này đảm bảo rằng mỗi văn bản chỉ được lưu một lần và có thể được tham chiếu lại để tiết kiệm dung lượng.
1. Hình ảnh có thể nhìn thấy được tham chiếu bởi id tham chiếu "rId2"

## Đóng góp

Phải chia sẻ điều gì đó về định dạng tệp XLSX hoặc Bảng tính? Bạn có thể đăng phát hiện của mình trong phần [Tin tức về định dạng tệp bảng tính](https://news.fileformat.com/t/Spreadsheet).

## Người giới thiệu

* [[MS-XLSX] - Định dạng tệp XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

