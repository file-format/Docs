{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "file", "extension", "file format", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết tệp ODS là gì và các API có thể tạo và mở chúng.",
  "title" :"Tệp ODS là gì?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Tệp ODS là gì?

Các tệp có phần mở rộng .ods là viết tắt của định dạng Tài liệu Bảng tính OpenDocument mà người dùng có thể chỉnh sửa. Dữ liệu được lưu trữ bên trong tệp ODF thành các hàng và cột. Đây là định dạng dựa trên XML và là một trong một số kiểu con trong họ Định dạng Tài liệu Mở (ODF). Định dạng được chỉ định như một phần của thông số kỹ thuật ODF 1.2 do OASIS xuất bản và duy trì. Một số ứng dụng trên Windows cũng như các hệ điều hành khác có thể mở tệp ODS để chỉnh sửa và thao tác bao gồm Microsoft Excel, NeoOffice và LibreOffice. Các tệp ODS cũng có thể được chuyển đổi thành các định dạng bảng tính khác như [XLS](/vi/spreadsheet/xls/), [XLSX](/vi/spreadsheet/xlsx/) và các định dạng khác bằng các ứng dụng khác nhau.

## Lược Sử ##

Thông số kỹ thuật định dạng tệp ODS dựa trên tiêu chuẩn được phát triển dưới dạng thông số kỹ thuật ODF. Các thông số kỹ thuật này đã phát triển trong quá khứ dưới dạng ba phiên bản do OASIS phát triển và xuất bản như sau:

`2005`- Phiên bản 1.0 được xuất bản vào tháng 5 năm 2005

`2007` - Phiên bản 1.1 được xuất bản vào tháng 2 năm 2007

`2011` - Phiên bản 1.2 được xuất bản vào tháng 9 năm 2011

Có những thay đổi khá nhỏ trong quá trình chuyển đổi từ phiên bản ODF 1.0 sang 1.1. [Phiên bản ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) là phiên bản mới nhất dành cho các thông số kỹ thuật của ODF và nên được các nhà phát triển tham khảo để phát triển các ứng dụng liên quan đến việc đọc/ghi ODS.

## Định dạng tệp ODS ##

Định dạng OpenDocument hỗ trợ biểu diễn tài liệu dưới dạng một tài liệu XML duy nhất cũng như tập hợp một số tài liệu phụ trong một gói dưới dạng lưu trữ [ZIP](/vi/compression/zip/). Mỗi tệp từ kho lưu trữ ZIP lưu trữ một phần của tài liệu hoàn chỉnh. Mỗi tài liệu con lưu trữ một khía cạnh cụ thể của tài liệu. Ví dụ: một tài liệu con chứa thông tin về kiểu dáng và một tài liệu con khác chứa nội dung của tài liệu. Một tài liệu ODF điển hình có các thành phần sau:

* `content.xml` – Nội dung tài liệu và kiểu tự động được sử dụng trong nội dung.
* `styles.xml` – Các kiểu được sử dụng trong nội dung tài liệu và các kiểu tự động được sử dụng trong chính các kiểu đó.
* `meta.xml` – Thông tin meta tài liệu, chẳng hạn như tác giả hoặc thời gian của hành động lưu cuối cùng.
* `settings.xml` – Cài đặt dành riêng cho ứng dụng, chẳng hạn như kích thước cửa sổ hoặc thông tin máy in.

Ngoài những thứ này, trong gói có thể có nhiều tài liệu phụ khác như hình thu nhỏ của tài liệu, hình ảnh, v.v.

Các tệp tài liệu bảng tính là tập hợp con của các tệp ODF nơi nội dung (trang tính) được lưu trữ trong tài liệu con content.xml.

## Người giới thiệu ##

* [OpenDocument - Bởi Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

