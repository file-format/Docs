{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Tệp ngôn ngữ định nghĩa báo cáo",
  "keywords" :[ "rdl", "ngôn ngữ định nghĩa báo cáo", "XmlTextWriter", "XSD", "phần tử RDL"],
  "description":"Tìm hiểu về định dạng tệp RDL là biểu diễn XML của định nghĩa báo cáo Dịch vụ báo cáo máy chủ SQL.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Tệp RDL là gì? ##

RDL (Ngôn ngữ định nghĩa báo cáo) là tiêu chuẩn do Microsoft thiết lập để xác định báo cáo. Một tệp RDL bao gồm một hoặc nhiều Phần tử RDL. Trong khi đó, một phần tử RDL bao gồm kiểu dữ liệu và lực lượng của nó. Một phần tử có thể đơn giản hoặc phức tạp. Phần tử đơn giản không có bất kỳ phần tử hoặc thuộc tính con nào, trong khi phần tử phức tạp có các thuộc tính con và tùy chọn.

## Định nghĩa lược đồ XML RDL
Tệp Định nghĩa lược đồ XML (XSD) xác thực tệp RDL. Lược đồ xác định các quy tắc về vị trí các phần tử RDL có thể xuất hiện trong tệp .rdl. Một phần tử RDL có thể đơn giản hoặc phức tạp. Một phần tử đơn giản không có các phần tử hoặc thuộc tính con và một phần tử phức hợp có các thuộc tính con và tùy chọn.

## Tạo RDL
Vì RDL về bản chất là mở và có thể mở rộng, nhiều ứng dụng và công cụ có thể được xây dựng để tạo các tệp RDL dựa trên lược đồ XML của nó. Một trong những cách đơn giản nhất để tạo RDL từ một ứng dụng là sử dụng các lớp Microsoft .NET Framework của không gian tên **System.Xml** và không gian tên System.Linq. Đặc biệt, lớp **XmlTextWriter** có thể được sử dụng để viết RDL. Bạn có thể tạo định nghĩa báo cáo hoàn chỉnh từ đầu đến cuối trong bất kỳ ứng dụng .NET Framework nào bằng cách sử dụng **XmlTextWriter**. Các nhà phát triển cũng có thể thêm các mục báo cáo tùy chỉnh với các thuộc tính tùy chỉnh để mở rộng RDL.

## Các loại RDL
Bảng sau đây liệt kê các loại và thuộc tính được sử dụng trong các phần tử RDL.

|Loại|Mô tả|
---|---|
|Nhị phân |Một thuộc tính có giá trị nhị phân được mã hóa theo cơ số 64.|
|Boolean| Thuộc tính có true hoặc false làm giá trị của đối tượng. Trừ khi được chỉ định khác, giá trị của một đối tượng Boolean tùy chọn bị bỏ qua là Sai.|
|Date |Một thuộc tính có giá trị ngày tháng hoặc thời gian được chỉ định đầy đủ được chỉ định ở định dạng ngày tháng theo tiêu chuẩn ISO8601: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Một thuộc tính có giá trị văn bản chuỗi phải là một trong danh sách các giá trị được chỉ định.|
|Float |Một thuộc tính có giá trị float. Dấu chấm (.) được sử dụng làm dấu tách thập phân tùy chọn.|
|Số nguyên |Một thuộc tính có giá trị số nguyên (int32).|
|Ngôn ngữ |Một thuộc tính có giá trị văn bản chứa mã ngôn ngữ và văn hóa, chẳng hạn như "en-us" cho tiếng Anh Mỹ. Giá trị phải là ngôn ngữ cụ thể hoặc ngôn ngữ trung lập mà ngôn ngữ mặc định được xác định trong Microsoft .NET Framework.|
|Tên |Một thuộc tính có giá trị văn bản chuỗi. Tên phải là duy nhất trong không gian tên của mục. Nếu không được chỉ định, không gian tên cho một mục là đối tượng chứa trong cùng có tên.|
|NormalizedString |Một thuộc tính có giá trị văn bản chuỗi đã được chuẩn hóa.|
|Kích thước |Một phần tử kích thước phải chứa một số (với ký tự dấu chấm được sử dụng làm dấu tách thập phân tùy chọn). Số phải được theo sau bởi một ký tự chỉ định cho một đơn vị độ dài CSS, chẳng hạn như cm, mm, in, pt hoặc pc. Khoảng cách giữa số và ký hiệu là tùy chọn. Để biết thêm thông tin về các ký hiệu chỉ định kích thước, hãy xem Giá trị CSS và tham chiếu đơn vị. Trong RDL, giá trị tối đa cho Kích thước là 160 inch. Kích thước tối thiểu là 0 inch.|
|Chuỗi |Một thuộc tính có giá trị văn bản chuỗi.|
|UnsignedInt |Một thuộc tính có giá trị số nguyên không dấu (uint32).|
|Biến thể |Một thuộc tính với bất kỳ loại XML đơn giản nào.|

## Các kiểu dữ liệu RDL
Trong RDL, DataType Enumeration xác định kiểu dữ liệu của một thuộc tính, biểu thức hoặc tham số. Bảng sau đây cho biết cách các kiểu dữ liệu CLR tương ứng với các kiểu dữ liệu RDL.

|(Các) Loại CLR |Loại Dữ liệu Tương ứng|
---|---|
|Boolean| Boolean|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Số nguyên|
|Đơn, đôi |Trôi nổi|
|Chuỗi, Char, GUID, Khoảng thời gian |Chuỗi|


## Người giới thiệu ##

- [Ngôn ngữ Định nghĩa Báo cáo (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Ngôn ngữ Định nghĩa Báo cáo (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

