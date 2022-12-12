{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "tệp", "phần mở rộng", "định dạng tệp", "Tệp bảng tính nhị phân Excel" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết tệp XLSB là gì và các API có thể tạo và mở chúng.",
  "title" :"Tệp XLSB là gì?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Tệp XLSB là gì?

Định dạng tệp XLSB chỉ định Định dạng tệp nhị phân Excel, là tập hợp các bản ghi và cấu trúc chỉ định nội dung sổ làm việc Excel. Nội dung có thể bao gồm các bảng số, văn bản hoặc cả số và văn bản, công thức, kết nối dữ liệu bên ngoài, biểu đồ và hình ảnh không có cấu trúc hoặc bán cấu trúc. Không giống như [XLSX](/vi/spreadsheet/xlsx/) (dựa trên định dạng tệp Open XML), XLSB đại diện cho tệp sổ làm việc Excel nhị phân. Các tệp XLSB có thể được đọc và ghi nhanh hơn, điều này giúp chúng hữu ích khi làm việc với các tệp lớn. XLSB hiếm khi được sử dụng để lưu trữ sổ làm việc vì XLSX (và trước đây [XLS](/vi/spreadsheet/xls/)) là định dạng tệp phổ biến nhất do người dùng chọn để lưu sổ làm việc. Nó có thể được mở bằng Microsoft Office 2007 trở lên.

## Thông số kỹ thuật định dạng tệp XLSB ##

Thông số kỹ thuật định dạng tệp cho định dạng tệp XLSB đã được công khai trở lại vào năm 2008 dưới dạng phiên bản 1.0. Kể từ đó, thông số kỹ thuật đã được sửa đổi nhiều lần và phiên bản mới nhất của thông số kỹ thuật (v 10.0) đã được xuất bản vào tháng 4 năm 2018. Thông số kỹ thuật được Microsoft công khai dưới dạng [[MS-XLSB] - Thông số định dạng tệp nhị phân Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) và nên được bất kỳ ai tư vấn về cách đọc hoặc ghi tệp ở định dạng tệp XLSB.

## Cấu trúc tệp XLSB ##

Tệp XLSB là một gói bao gồm một tập hợp các phần. Các phần này chứa thông tin về nội dung của sổ làm việc, bao gồm dữ liệu sổ làm việc và cấu trúc của gói. Một số phần chứa thông tin được lưu trữ bằng bản ghi nhị phân, một số dưới dạng XML, trong khi những phần khác chứa thông tin được lưu trữ dưới dạng luồng byte nhị phân. Mỗi bản ghi nhị phân chứa 0 hoặc nhiều trường có cấu trúc chứa dữ liệu sổ làm việc.

#### Bưu kiện ####

Gói XLSB là một kho lưu trữ [ZIP](/vi/compression/zip/) phải chứa chính xác một phần sổ làm việc. Phần này phải là mục tiêu của một mối quan hệ trong phần mối quan hệ gói này. Phần sổ làm việc là phần bắt đầu trong tài liệu XLSB.

#### Phần ####

Một phần là một luồng byte có loại nội dung được liên kết chỉ định bản chất và loại nội dung được lưu trữ trong phần đó. Một số phần lưu trữ thông tin ở định dạng nhị phân trong khi những phần khác lưu trữ thông tin dưới dạng XML. Phần [liệt kê bộ phận](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) của tài liệu thông số kỹ thuật liệt kê các bộ phận hợp lệ, loại nội dung và mối quan hệ bắt buộc/tùy chọn giữa tất cả các bộ phận trong một gói.

#### Mối quan hệ ####

Một nguồn và một tài nguyên đích được kết nối bởi một mối quan hệ. Một mối quan hệ có thể là:

**Mối quan hệ gói:** trong đó mục tiêu là một phần và nguồn là toàn bộ gói

**Mối quan hệ giữa các bộ phận:** trong đó đích là một bộ phận và nguồn là một bộ phận trong gói

**Mối quan hệ rõ ràng:** trong đó tài nguyên được tham chiếu từ nội dung của phần nguồn bằng cách tham chiếu giá trị thuộc tính ID của phần tử mối quan hệ

**mối quan hệ ngầm** là mối quan hệ không rõ ràng

**Mối quan hệ nội bộ:** trong đó mục tiêu là một phần trong gói

**Mối quan hệ bên ngoài:** trong đó mục tiêu là tài nguyên bên ngoài không có trong gói

#### Ghi lại ####

Bản ghi là khối dựng cơ bản được sử dụng để lưu trữ thông tin về các tính năng trong sổ làm việc. Mỗi bản ghi nhị phân là một chuỗi byte có độ dài thay đổi. Một bản ghi nhị phân bao gồm ba thành phần:

* một loại bản ghi
* một kích thước kỷ lục, và
* dữ liệu bản ghi dành riêng cho loại bản ghi đó.

**Loại bản ghi:** Loại bản ghi hiển thị loại bản ghi được chỉ định bởi bản ghi. Nó cũng chỉ định cấu trúc của dữ liệu bản ghi dành riêng cho bản ghi này. Các loại bản ghi hợp lệ được liệt kê trong phần [Liệt kê bản ghi](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) của tài liệu thông số kỹ thuật. Loại bản ghi phải là một hoặc hai byte và phải lớn hơn hoặc bằng 128 và nhỏ hơn 16384.

**Kích thước bản ghi:** Kích thước bản ghi chỉ định số lượng byte chỉ định tổng kích thước của dữ liệu bản ghi. Giá trị này PHẢI từ một đến bốn byte. Giá trị này PHẢI là một byte nếu bit cao trong byte thấp bằng 0; mặt khác, giá trị này PHẢI lớn hơn một byte. Nếu số lượng byte lớn hơn một byte, thì bit cao trong mỗi byte kế tiếp sẽ chỉ định xem một byte bổ sung có được sử dụng hay không. Nếu bit cao của byte thứ hai bằng 1, thì giá trị này PHẢI sử dụng thêm một byte thứ ba. Nếu bit cao của byte thứ ba bằng 1, thì giá trị này PHẢI sử dụng một byte thứ tư bổ sung. Bit cao của byte thứ tư PHẢI được bỏ qua. Giá trị bao gồm bảy bit thấp của mỗi byte được kết hợp. Các bit thấp, ít quan trọng nhất được chứa trong byte đầu tiên và mỗi byte kế tiếp chứa các bit có thứ tự cao hơn byte trước đó.

**Dữ liệu bản ghi:** Thành phần dữ liệu bản ghi chứa các trường tương ứng với một loại bản ghi cụ thể và bao gồm phần còn lại của bản ghi. Thứ tự và cấu trúc của các trường cho một loại bản ghi nhất định được liệt kê trong Liệt kê Bản ghi được chỉ định trong phần tương ứng cho loại bản ghi đó trong Bản ghi. Tổng kích thước của thành phần dữ liệu bản ghi PHẢI bằng kích thước bản ghi. Các trường trong thành phần dữ liệu bản ghi có thể chứa các giá trị đơn giản, mảng giá trị, cấu trúc của một số trường, mảng trường và mảng cấu trúc.

#### Ví dụ Bản ghi XLSB ####

Loại bản ghi và kích thước bản ghi sau đây chỉ định bản ghi **BrtCommentText** với kích thước 200 byte:

11111101 00000100 11001000 00000001 [Trường ghi]

Byte đầu tiên là 11111101, chỉ định giá trị thấp là 125 và loại bản ghi yêu cầu byte thứ hai. Byte thứ hai là 00000100, chỉ định giá trị cao là 4 * 128, bằng 512. Giá trị loại bản ghi là 125 + 512 hoặc 637, tương ứng với loại bản ghi **BrtCommentText**. Byte tiếp theo là 11001000, chỉ định giá trị thấp là 72 và kích thước bản ghi yêu cầu byte thứ hai. Byte thứ hai là 00000001, chỉ định giá trị cao hơn là 1 * 128 và kích thước bản ghi không yêu cầu byte bổ sung. Kích thước bản ghi là 72 + 128 hoặc 200, chỉ định tổng kích thước, tính bằng byte, của thành phần dữ liệu bản ghi. Các trường trong thành phần dữ liệu bản ghi được chỉ định bởi **BrtCommentText**.

## Người giới thiệu ##

* [[MS-XLSB] - Định dạng tệp nhị phân Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

