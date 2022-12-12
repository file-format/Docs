{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết tệp XLS là gì và các API có thể tạo và mở chúng.",
  "title" :"Định dạng tệp XLS là gì? Tìm hiểu từ các chuyên gia về định dạng tệp!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Tệp XLS là gì?

Các tệp có phần mở rộng XLS đại diện cho Định dạng tệp nhị phân Excel. Các tệp như vậy có thể được tạo bởi Microsoft Excel cũng như các chương trình bảng tính tương tự khác như OpenOffice Calc hoặc Apple Numbers. Tệp được lưu bởi Excel được gọi là Sổ làm việc trong đó mỗi sổ làm việc có thể có một hoặc nhiều trang tính. Dữ liệu được lưu trữ và hiển thị cho người dùng ở định dạng bảng trong trang tính và có thể bao gồm các giá trị số, dữ liệu văn bản, công thức, kết nối dữ liệu ngoài, hình ảnh và biểu đồ. Các ứng dụng như Microsoft Excel cho phép bạn xuất dữ liệu sổ làm việc sang nhiều định dạng khác nhau bao gồm [PDF](/vi/pdf/), [CSV](/vi/spreadsheet/csv/), [XLSX](/vi/spreadsheet/xlsx/), [TXT](/vi/ xử lý văn bản/txt/), [HTML](/vi/web/html/), [XPS](/vi/page-description-language/xps/), và một số ngôn ngữ khác. Định dạng tệp XLS đã được thay thế bằng định dạng có cấu trúc và mở hơn, XLSX, với việc phát hành Microsoft Excel 2007. Các phiên bản mới nhất vẫn cung cấp hỗ trợ để tạo và đọc các tệp XLS, mặc dù XLSX là lựa chọn sử dụng đầu tiên hiện nay.

## Tóm tắt lịch sử

XLS được tạo bởi Microsoft để sử dụng với Microsoft Excel và còn được gọi là Định dạng tệp trao đổi nhị phân (BIFF). Loại tệp này được giới thiệu lần đầu tiên bằng cách biến nó thành một phần của Excel cho Windows vào năm 1987. Các thông số định dạng tệp XLS được công bố lần đầu tiên vào tháng 6 năm 2008 dưới dạng Bản sửa đổi 1. Sau đó, các thông số kỹ thuật liên tục được cập nhật và có bản sửa đổi mới nhất kể từ tháng 8 năm 2018 được đánh dấu là Bản sửa đổi 8.0. Lịch sử ngắn gọn về các phiên bản khác nhau của định dạng tệp XLS như sau:

* Phiên bản 7.0 (được phát hành cùng với office 95): Phiên bản excel này mạnh nhất và nhanh hơn trong số tất cả các phiên bản và các bản ghi lại luồng nội bộ đã được cập nhật lên 32 bit.
* Phiên bản 8 (phát hành cùng với office 97): VBA được giới thiệu như một ngôn ngữ tiêu chuẩn và lần đầu tiên các nhãn ngôn ngữ tự nhiên bị loại bỏ được đưa vào phiên bản này. Nó cũng lần đầu tiên giới thiệu một trợ lý văn phòng kẹp giấy.
* Phiên bản 9 (Được phát hành cùng với office 2000): Chỉ có những thay đổi nhỏ trong Phiên bản 9 trong đó trợ lý văn phòng kẹp giấy có thể giữ đồng thời nhiều đối tượng mà trước đây không thể thực hiện được.
* Phiên bản 10 (Phát hành cùng với office XP): Phiên bản này không có bất kỳ cải tiến đáng chú ý nào.
* Phiên bản 11 (Phát hành cùng với office 2003): Cập nhật chính trong phiên bản 11, excel 2003 là sự ra đời của các bảng mới.

## Thông số kỹ thuật định dạng tệp XLS ##

Dữ liệu được sắp xếp trong tệp XLS dưới dạng luồng nhị phân ở dạng tệp ghép như được mô tả trong [MS-CFB]. Dữ liệu được lưu trữ trong tệp phức hợp bằng cách sử dụng kho lưu trữ, luồng và luồng con chứa thông tin về nội dung và cấu trúc của sổ làm việc, bao gồm dữ liệu sổ làm việc chẳng hạn như định nghĩa trang tính. Mỗi luồng hoặc luồng con chứa một loạt các bản ghi nhị phân. Mỗi bản ghi nhị phân chứa 0 hoặc nhiều trường có cấu trúc chứa dữ liệu sổ làm việc. Phần này cung cấp tổng quan ngắn gọn về Cấu trúc tệp XLS, nhưng để biết thông số kỹ thuật định dạng tệp chi tiết, người ta phải tham khảo [Thông số kỹ thuật tạo tệp XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) tài liệu của Microsoft.

#### Luồng và Luồng phụ ####

Sổ làm việc được đại diện bởi luồng sổ làm việc. Mỗi trang tính trong một sổ làm việc được đại diện bởi Dòng con. Ngoài ra, nó có Luồng phụ của Trang biểu đồ, Luồng phụ của Trang macro hoặc Luồng phụ của Trang hộp thoại theo sau Luồng phụ chung. Mỗi luồng nhị phân hoặc luồng con chứa dữ liệu sổ làm việc PHẢI được ghi dưới dạng một chuỗi bản ghi nhị phân.

#### Ghi lại ####

Thông tin về các tính năng trong sổ làm việc được lưu trữ dưới dạng bản ghi là một chuỗi byte có độ dài thay đổi. Một bản ghi nhị phân bao gồm ba thành phần sau:

**Loại bản ghi:** Loại bản ghi là một số nguyên không dấu hai byte chỉ định loại thông tin được bản ghi chỉ định và cách cấu trúc của dữ liệu bản ghi dành riêng cho bản ghi này được sắp xếp và cấu trúc. Giá trị loại bản ghi PHẢI là giá trị từ Bảng liệt kê bản ghi (phần 2.3) hoặc bản ghi PHẢI sử dụng kiến trúc bản ghi trong tương lai (phần 2.1.6).

**Kích thước bản ghi**: Kích thước bản ghi là một số nguyên không dấu hai byte chỉ định số lượng byte chỉ định tổng kích thước của dữ liệu bản ghi. Kích thước bản ghi PHẢI lớn hơn hoặc bằng 0 và PHẢI nhỏ hơn hoặc bằng 8224.

**Dữ liệu bản ghi:** Thành phần dữ liệu bản ghi chứa các trường tương ứng với một loại bản ghi cụ thể và bao gồm phần còn lại của bản ghi. Thứ tự và cấu trúc của các trường cho một loại bản ghi nhất định được chỉ định trong phần tương ứng cho loại bản ghi đó. Kích thước của thành phần dữ liệu bản ghi PHẢI bằng kích thước bản ghi. Các trường trong thành phần dữ liệu bản ghi có thể chứa các giá trị đơn giản, mảng giá trị, cấu trúc của một số trường, mảng trường và mảng cấu trúc.

#### Bảng ô ####

Các ô là các khối cơ bản của sổ làm việc lưu trữ nội dung sổ làm việc như văn bản, công thức và dữ liệu số. Các ô duy trì bản ghi của dữ liệu được lưu trữ thông qua cấu trúc dữ liệu được gọi là Bảng ô. Bản thân Bảng ô được lưu trữ theo trình tự các bản ghi tuân theo các quy tắc CELLTABLE được xác định trong tài liệu thông số kỹ thuật. Nó bao gồm một loạt các khối hàng trong đó các hàng được sắp xếp trong các khối hàng. Mỗi khối hàng chứa các hàng từ hàng đầu tiên chứa dữ liệu đến hàng cuối cùng chứa dữ liệu.

Dữ liệu hoặc định dạng hàng được lưu trong bản ghi Hàng cho mỗi khối hàng. Mỗi ô chứa dữ liệu hoặc định dạng ô riêng lẻ được biểu thị bằng một bản ghi. Định dạng được liên kết với một ô có thể được bắt nguồn từ định dạng ô riêng lẻ, định dạng hàng, định dạng cột hoặc định dạng ô mặc định. Thứ tự ưu tiên để định dạng là định dạng ô riêng lẻ có mức độ ưu tiên cao nhất, tiếp theo là định dạng hàng, sau đó là định dạng cột, rồi đến định dạng ô mặc định. Các ô không chứa dữ liệu và không chứa định dạng riêng lẻ sẽ không được lưu.

#### Công thức ####

Công thức là một chuỗi các giá trị, tham chiếu ô, tên, hàm hoặc toán tử trong một ô cùng nhau tạo ra một giá trị mới. Các công thức được lưu trữ trong một đại diện được mã hóa được gọi là "biểu thức được phân tích cú pháp". Một biểu thức được phân tích cú pháp được chuyển đổi thành một công thức văn bản trong thời gian chạy để hiển thị và người dùng chỉnh sửa. Công thức ô được chỉ định bởi bản ghi Công thức. Công thức mảng được chỉ định bởi bản ghi Array. Các công thức được chia sẻ được chỉ định bởi bản ghi ShrFmla.

#### Biểu đồ ####

Trang tính biểu đồ chỉ định biểu đồ, đồ họa hiển thị dữ liệu hoặc mối quan hệ giữa các bộ dữ liệu ở dạng trực quan và bộ nhớ đệm dữ liệu biểu đồ, bản sao cục bộ của dữ liệu được sử dụng trong dữ liệu biểu đồ bị thiếu hoặc nếu liên kết đến bên ngoài nguồn dữ liệu bị hỏng. Biểu đồ chỉ định các nhóm một hoặc hai trục, một tập hợp các trục mà dữ liệu biểu đồ được vẽ dựa trên đó và tập hợp các chuỗi, đường xu hướng và thanh lỗi được chỉ định trong biểu đồ. Mỗi nhóm trục chỉ định một đến bốn nhóm biểu đồ chỉ định kiểu trực quan hóa được sử dụng để hiển thị dữ liệu. Mỗi chuỗi, đường xu hướng và thanh lỗi chỉ định một nhóm biểu đồ được liên kết với nó.

#### Metadata ####

Siêu dữ liệu là dữ liệu bổ sung được liên kết với một ô cụ thể hoặc nội dung của ô đó. Siêu dữ liệu được ghi lại trong BIFF8 chỉ dành cho mục đích mở rộng trong tương lai.

#### Bảng Pivot ####

PivotTable là một cơ chế tóm tắt dữ liệu nguồn để có cái nhìn tổng quan về việc phân phối dữ liệu đó. Trong PivotTable, các cột có thể áp dụng của dữ liệu nguồn trở thành các trường có thể dùng để tóm tắt dữ liệu. Khi dữ liệu nguồn của PivotTable là dữ liệu nguồn OLAP, hệ thống phân cấp OLAP và một số thực thể OLAP khác sẽ trở thành các trường trong PivotTable.
PivotTable có hai phần chính, PivotCache và dạng xem PivotTable. Có thể có nhiều dạng xem PivotTable dựa trên một PivotCache không phải OLAP.

#### Phong cách ####

Phần tổng quan này mô tả cách chỉ định thông tin định dạng và bảo vệ cho các ô trong trang tính (1). Định dạng ô bao gồm một số bộ thuộc tính:

* Thuộc tính phông chữ (đậm, nghiêng, màu chữ, cỡ chữ, v.v.)
* Thuộc tính tô (màu nền trước, màu nền, mẫu, độ dốc, v.v.)
* Thuộc tính căn chỉnh (căn trái, căn giữa, căn phải, v.v.)
* Thuộc tính đường viền (trái, phải, trên, dưới, dày hay mỏng, màu sắc, v.v.)
* Thuộc tính định dạng số (ngày, giờ, số chữ số thập phân, v.v.)
* Thuộc tính bảo vệ (bị khóa, ẩn, v.v.)

Các thuộc tính này, nói chung, mô tả cách hiển thị và in một ô cụ thể.

## Người giới thiệu ##

* [[MS-XLS] - Cấu trúc định dạng tệp nhị phân Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Định dạng tệp nhị phân tệp hợp chất](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

