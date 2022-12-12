{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "tệp", "phần mở rộng", "định dạng tệp", "Giá trị được phân tách bằng dấu phẩy", "Bảng tính" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp CSV và các API có thể tạo và mở tệp CSV.",
  "title" :"Định dạng tệp CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Tệp CSV là gì?

Các tệp có phần mở rộng .csv (Các giá trị được phân tách bằng dấu phẩy) đại diện cho các tệp văn bản thuần túy chứa các bản ghi dữ liệu có các giá trị được phân tách bằng dấu phẩy. Mỗi dòng trong tệp CSV là một bản ghi mới từ tập hợp các bản ghi có trong tệp. Các tệp như vậy được tạo khi dự định truyền dữ liệu từ hệ thống lưu trữ này sang hệ thống lưu trữ khác. Vì tất cả các ứng dụng có thể nhận dạng các bản ghi được phân tách bằng dấu phẩy nên việc nhập các tệp dữ liệu đó vào cơ sở dữ liệu được thực hiện rất thuận tiện. Hầu như tất cả các ứng dụng bảng tính như Microsoft Excel hoặc OpenOffice Calc đều có thể nhập CSV mà không cần nỗ lực nhiều. Dữ liệu được nhập từ các tệp đó được sắp xếp trong các ô của bảng tính để trình bày cho người dùng.

## Lược Sử ##

Sau đây là một số thông tin nhanh về nguồn gốc và lịch sử của định dạng tệp CSV.

* 1972 - Trình biên dịch IBM Fortran (mức H mở rộng) hỗ trợ chúng trong OS/360

* 1978 - FORTRAN 77 hỗ trợ đầu vào/đầu ra theo hướng danh sách sử dụng dấu phẩy và dấu cách cho các dấu phân cách

* 2005 - CSV được chuẩn hóa với [RFC4180](https://tools.ietf.org/html/rfc4180) làm Loại nội dung MIME.

* 2013 - Các thiếu sót của RFC4180 đã được xử lý theo khuyến nghị của W3C

* 2015 - W3C đã đưa ra các bản dự thảo đề xuất đầu tiên cho các tiêu chuẩn siêu dữ liệu CSV, bắt đầu dưới dạng đề xuất vào tháng 12 năm 2015

## Chuyển đổi tệp CSV ##

Các tệp CSV có thể được chuyển đổi sang một số định dạng tệp khác nhau bằng các ứng dụng có thể mở các tệp này. Ví dụ: Microsoft Excel có thể nhập dữ liệu từ định dạng tệp CSV và lưu vào XLS, [XLSX](/vi/spreadsheet/xlsx/), [PDF](/vi/pdf/), [TXT](/vi/word-processing/txt/) định dạng tệp , XML và [HTML](/vi/web/html/). Tương tự, các dịch vụ trực tuyến cũng như máy tính để bàn khác cung cấp khả năng xuất tệp CSV sang HTML, ODS và [RTF](/vi/word-processing/rtf/).

## Định dạng tệp CSV ##

Định dạng tệp CSV được biết là được chỉ định trong [RFC4180](https://tools.ietf.org/html/rfc4180). Nó xác định bất kỳ tệp nào tuân thủ CSV nếu:

* Mỗi bản ghi nằm trên một dòng riêng biệt, được phân định bằng dấu ngắt dòng (CRLF). Ví dụ:
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* Bản ghi cuối cùng trong tệp có thể có hoặc không có dấu ngắt dòng kết thúc. Ví dụ:
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx
* Có thể có một dòng tiêu đề tùy chọn xuất hiện dưới dạng dòng đầu tiên của tệp với định dạng giống như các dòng ghi thông thường. Tiêu đề này sẽ chứa các tên tương ứng với các trường trong tệp và phải chứa cùng số trường như các bản ghi trong phần còn lại của tệp (sự hiện diện hay vắng mặt của dòng tiêu đề phải được chỉ định thông qua tham số "tiêu đề" tùy chọn của phần này loại MIME). Ví dụ:
* tên_trường,tên_trường,tên_trường CRLF
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿Trong tiêu đề và mỗi bản ghi, có thể có một hoặc nhiều trường, được phân tách bằng dấu phẩy. Mỗi dòng phải chứa cùng một số trường trong toàn bộ tệp. Khoảng trắng được coi là một phần của trường và không nên bỏ qua. Trường cuối cùng trong bản ghi không được theo sau bởi dấu phẩy. Ví dụ:
* aa, bbb, ccc
* Mỗi trường có thể có hoặc không được đặt trong dấu ngoặc kép (tuy nhiên một số chương trình, chẳng hạn như Microsoft Excel, hoàn toàn không sử dụng dấu ngoặc kép). Nếu các trường không được đặt trong dấu ngoặc kép thì dấu ngoặc kép có thể không xuất hiện bên trong các trường. Ví dụ:\
* "aaa","bbb","ccc" CRLF
* zzz,yyy,xxx
* Các trường chứa dấu ngắt dòng (CRLF), dấu ngoặc kép và dấu phẩy phải được đặt trong dấu ngoặc kép. Ví dụ:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* Nếu dấu ngoặc kép được sử dụng để bao quanh các trường, thì dấu ngoặc kép xuất hiện bên trong trường phải được thoát ra bằng cách đặt trước nó bằng một dấu ngoặc kép khác. Ví dụ:
* "aaa","b""bb","ccc"

Tuy nhiên, theo cách sử dụng hiện đại, dấu phân cách không chỉ giới hạn ở dấu phẩy và có thể là dấu chấm phẩy, tab hoặc dấu cách. Các ứng dụng như Microsoft Excel cung cấp tùy chọn chỉ định ký tự phân cách để nhập bản ghi từ tệp CSV.

## Người giới thiệu

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

