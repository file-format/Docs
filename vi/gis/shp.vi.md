{
  "date" : "2019-10-11",
  "keywords" :[ "tệp shp", "định dạng tệp shp", "tệp shp là gì", "tệp", "ví dụ shp", "phần mở rộng tệp shp","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - Tệp hình dạng ESRI",
  "description":"Tìm hiểu về định dạng tệp SHP và API có thể tạo và mở tệp SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp SHP là gì?

SHP là phần mở rộng tệp cho một trong các loại tệp chính được sử dụng để biểu diễn ESRI Shapefile. Nó đại diện cho thông tin Không gian địa lý ở dạng dữ liệu vectơ được sử dụng bởi các ứng dụng Hệ thống Thông tin Địa lý (GIS). Định dạng đã được phát triển dưới dạng thông số kỹ thuật mở để tạo điều kiện thuận lợi cho khả năng tương tác giữa ESRI và các sản phẩm phần mềm khác.

## Sự miêu tả dữ liệu

Như đã đề cập, định dạng shapefile mô tả thông tin không gian địa lý của tập dữ liệu dưới dạng các đối tượng vectơ. Các tính năng vectơ này bao gồm:

* điểm
* dòng
* đa giác

Các tính năng này kết hợp có thể đại diện cho hầu hết mọi loại hình dạng như giếng nước, ranh giới quốc gia, điểm không gian, dòng chảy của sông, hồ, v.v. Mỗi tính năng vectơ có thể có các thuộc tính thực sự xác định mục đích của tính năng đó. Ví dụ: một tệp hình dạng chứa các thành phố của Los Angeles có thể có tên thành phố và nhiệt độ làm thuộc tính mang lại biểu diễn có ý nghĩa cho dữ liệu không gian.

## Tệp liên kết

Một tệp shp độc lập không thể được sử dụng bởi các ứng dụng phần mềm để hiểu ý nghĩa của dữ liệu chứa trong đó. Để hiểu được thông tin chứa trong một tệp như vậy, một shapefile sử dụng các tệp bắt buộc bổ sung sau đây.

* tệp shx - tệp chỉ mục
* tệp dbf - tệp dBASE lưu trữ tất cả các thuộc tính của hình dạng trong tệp chính
* tệp prj - lưu trữ thông tin dự án của tệp

Cũng có thể có các tệp tùy chọn khác có cùng tên với tệp chính.

## Thông số kỹ thuật định dạng tệp SHP

Thông số kỹ thuật mở của shapefile có sẵn trực tuyến từ ESRI dưới dạng [Mô tả kỹ thuật](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) và giải thích chi tiết cấu trúc tổng thể của tệp. Thông tin trong tệp .shp chính bao gồm các tiêu đề và bản ghi. Tiêu đề tệp có độ dài cố định được theo sau bởi các bản ghi có độ dài thay đổi trong đó mọi bản ghi được tạo thành từ một tiêu đề bản ghi có độ dài cố định, theo sau là nội dung bản ghi có độ dài thay đổi.

### Tiêu đề tệp SHP chính

Tiêu đề tệp chính bắt đầu từ đầu tệp và có độ dài 100 byte. Tổ chức của tiêu đề tệp chính này cùng với vị trí byte, giá trị, loại và thứ tự byte được hiển thị trong bảng sau.


|Byte|Trường|Giá trị|Loại|Thứ tự byte
---|---|---|---|---|
|0-3|Mã tệp|9994|Số nguyên|Dấu cuối lớn
|4-23|Không sử dụng|0|Số nguyên|Dấu cuối lớn
|24-27|Độ dài tệp|Độ dài tệp|Số nguyên|Dấu cuối lớn
|28-31|Phiên bản|1000|Số nguyên|Little Endian
|32-35|Kiểu hình|Kiểu hình|Số nguyên|Little Endian
|36-67|Hình chữ nhật giới hạn tối thiểu|Xmin, Ymin, Xmax và Ymax|đôi|Little Endian
|68-83|Hộp giới hạn|Zmin, Zmax|đôi|Little Endian
|84-99|Hộp giới hạn|Mmin, Mmax|đôi|

Cần lưu ý rằng giá trị của độ dài tệp là tổng độ dài của tệp tính bằng các từ 16 bit, bao gồm cả 50 từ 16 bit tạo nên tiêu đề.

#### Các loại hình dạng

Các giá trị của trường loại hình dạng trong bảng trên như sau:


|Giá trị|Loại hình
---|---|
|0|Hình dạng Null
|1|Điểm
|3|Đa tuyến
|5|Đa giác
|8|Đa điểm
|11|ĐiểmZ
|13|Đa tuyếnZ
|15|Đa giácZ
|18|Đa điểmZ
|21|ĐiểmM
|23|Đa tuyếnM
|25|Đa giácM
|28|Đa điểmM
|31|MultiPatch

### Bản ghi dữ liệu ###

Tiêu đề tệp chính được theo sau bởi các bản ghi có độ dài thay đổi trong đó mỗi bản ghi bao gồm một tiêu đề bản ghi có độ dài cố định, theo sau là nội dung bản ghi có độ dài thay đổi.

#### Tiêu đề Bản ghi ####

Tiêu đề bản ghi chứa thông tin về số bản ghi và độ dài nội dung của bản ghi trong một độ dài cố định là 8 byte. Việc tổ chức tiêu đề bản ghi như sau:


|Byte|Trường|Giá trị|Loại|Thứ tự byte
---|---|---|---|---|
|0-3|Số bản ghi|Số bản ghi|Số nguyên|Lớn
|4-7|Độ dài bản ghi|Độ dài bản ghi|Số nguyên|Lớn

#### Nội dung ghi ####

Nội dung bản ghi shapefile bao gồm một loại hình theo sau là dữ liệu hình học cho hình dạng đó. Loại hình dạng 0 đại diện cho một hình dạng null không có dữ liệu hình học cho hình dạng. Độ dài của nội dung bản ghi là sự phản ánh của các phần và đỉnh của hình dạng. Hãy lấy một ví dụ về loại Hình dạng Điểm để giải thích cách một bản ghi chứa thông tin về loại hình dạng đó.

Một điểm đại diện cho một vị trí địa lý nhất định theo thứ tự X, Y trong đó mỗi tọa độ được biểu thị bằng một giá trị có độ chính xác kép. Bảng sau đây cho thấy sự sắp xếp của một loại hình dạng Điểm.


|Byte|Loại Hình dạng|Giá trị|Loại|Số|Thứ tự Byte
---|---|---|---|---|---|
|0-3|Loại hình|1|Số nguyên|1|Little
|4-11|X|X|đôi|1|Ít
|12-19|Y|Y|đôi|1|Ít

Ví dụ về các loại hình dạng khác có thể được tìm thấy trong tài liệu mô tả kỹ thuật ESRI.

## Người giới thiệu ##

* [Mô tả kỹ thuật ESRI Shapefile](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) của ESRI

