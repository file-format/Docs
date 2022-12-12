{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "phần mở rộng", "tệp cdb", "định dạng tệp cdb", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "tệp cdb là gì" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp CDB và API có thể tạo và mở tệp CDB.",
  "title" :"CDB - Tệp cơ sở dữ liệu không đổi",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Tệp CDB là gì?
Các tệp CDB được sử dụng trong các ứng dụng quan trọng như email. CDB là viết tắt của "cơ sở dữ liệu không đổi", một gói nhanh chóng, đáng tin cậy và đơn giản để tạo hoặc đọc cơ sở dữ liệu không đổi. Thay thế cơ sở dữ liệu là an toàn chống lại sự cố hệ thống. Người dùng không phải tạm dừng trong khi viết lại. CDB hoạt động như một mảng kết hợp (trên đĩa), ánh xạ các khóa tới các giá trị và cho phép lưu trữ nhiều giá trị trong một khóa.

## Định dạng tệp CDB
Định dạng tệp CDB lưu trữ các số, độ lệch, độ dài và giá trị băm ở định dạng endian nhỏ dưới dạng số nguyên 32 bit không dấu. Các khóa và dữ liệu được cho là các chuỗi byte mờ không có cách xử lý đặc biệt. Khi bắt đầu cơ sở dữ liệu, tiêu đề có kích thước cố định đại diện cho 256 bảng băm bằng cách liệt kê vị trí của chúng trong tệp và độ dài của chúng trong các vị trí. Thông thường dữ liệu được lưu trữ dưới dạng một dãy các bản ghi, mỗi bản ghi lưu trữ độ dài khóa, độ dài dữ liệu, khóa và dữ liệu. Không có quy tắc sắp xếp hoặc căn chỉnh. Các bản ghi được theo sau bởi một tập hợp gồm 256 bảng băm có độ dài khác nhau. Vì 0 là độ dài hợp lệ nên có thể có ít hơn 256 bảng băm được lưu trữ vật lý trong cơ sở dữ liệu, nhưng không có bảng nào được coi là 256 bảng. Các bảng băm bao gồm một loạt các vị trí, mỗi vị trí chứa một giá trị băm và phần bù bản ghi. "Các vị trí trống" có độ lệch bằng 0.

### Kết cấu
Cơ sở dữ liệu CDB bao gồm toàn bộ tập dữ liệu trong một tệp máy tính. Nó bao gồm ba phần:
- Tiêu đề có kích thước cố định
- Dữ liệu
- Một bộ bảng băm.

Tra cứu chỉ có sẵn cho các khóa chính xác. Hoạt động tra cứu sử dụng thuật toán sau:

- Băm khóa.
- Xác định vị trí của bảng băm và vị trí của bản ghi này.
- Kiểm tra vị trí được chỉ định trong bảng băm.

Để tra cứu các khóa có nhiều hơn một giá trị, có thể tìm thấy các giá trị bổ sung bằng cách tiếp tục tìm kiếm ở vị trí tiếp theo.

#### Đặc trưng

Cấu trúc cơ sở dữ liệu CDB cung cấp một số tính năng:

##### Tra cứu nhanh
Một lần tra cứu thành công trong một cơ sở dữ liệu khổng lồ thường chỉ cần hai lần truy cập đĩa và một lần tra cứu không thành công chỉ cần một lần.
##### Chi phí thấp
Cơ sở dữ liệu sử dụng 2048 byte, 24 byte cho mỗi bản ghi và không gian cho khóa và dữ liệu.
##### Không giới hạn ngẫu nhiên
CDB có thể quản lý bất kỳ cơ sở dữ liệu nào lên tới 4 gigabyte. Vì không có hạn chế nào khác, các bản ghi thậm chí không cần phải vừa với bộ nhớ. Cơ sở dữ liệu được lưu trữ ở định dạng độc lập với máy.
##### Thay thế cơ sở dữ liệu nguyên tử nhanh
Lệnh **cdbmake** có thể ghi lại toàn bộ cơ sở dữ liệu thành hai bậc độ lớn, nhanh hơn các gói băm khác.
##### Kết xuất cơ sở dữ liệu nhanh
**cdbdump** có thể in nội dung của cơ sở dữ liệu ở định dạng tương thích với cdbmake.


## Người giới thiệu ##

* [cdb (phần mềm) - Wikipedia](https://vi.wikipedia.org/wiki/Cdb_(phần mềm))
* [Đặc tả CDB](http://cr.yp.to/cdb.html)

