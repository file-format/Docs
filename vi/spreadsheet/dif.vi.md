{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "tệp", "phần mở rộng", "định dạng tệp", "Tệp trao đổi dữ liệu", "Bảng tính" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Hướng dẫn định dạng tệp của bạn để biết phần mở rộng tệp DIF là gì và các API có thể tạo và mở tệp DIF.",
  "title" :"DIF - Định dạng tệp trao đổi dữ liệu",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Tệp DIF là gì?

DIF là viết tắt của Định dạng trao đổi dữ liệu được sử dụng để nhập/xuất dữ liệu bảng tính giữa các ứng dụng khác nhau. Chúng bao gồm Microsoft Excel, OpenOffice Calc, StarCalc và nhiều thứ khác. Nó lưu trữ dữ liệu trong một bảng tính duy nhất, đây là hạn chế duy nhất của định dạng tệp này.

## Lịch sử tóm tắt về định dạng tệp DIF ##

Định dạng tệp DIF được phát triển bởi Software Arts, Inc. vào đầu những năm 1980. Các thông số định dạng tệp cho DIF đã được đưa vào VisiCalc, đây là chương trình bảng tính đầu tiên dành cho máy tính cá nhân. Các thông số kỹ thuật này đã được đăng ký bản quyền vào năm 1981 và là nhãn hiệu đã đăng ký của Software Arts Products Corp.

## Định dạng tệp DIF ##

DIF lưu trữ nội dung bảng tính trong tệp văn bản ASCII cho phép xem và chỉnh sửa nó bằng trình soạn thảo văn bản. Định dạng sở hữu vị trí của nó trong danh sách định dạng tuần tự hóa dữ liệu vì các đặc tính trao đổi dữ liệu của nó. Tệp DIF bao gồm 2 phần; một tiêu đề và dữ liệu.

Mọi thứ trong DIF được thể hiện bằng một đoạn 2 hoặc 3 dòng. Tiêu đề có một đoạn 3 dòng; dữ liệu, 2.

* Các đoạn tiêu đề bắt đầu bằng một mã định danh văn bản viết hoa toàn bộ, chỉ các ký tự chữ cái và ít hơn 32 chữ cái. Dòng tiếp theo phải là một cặp số và dòng thứ ba phải là một chuỗi được trích dẫn.
* Các khối dữ liệu bắt đầu bằng một cặp số và dòng tiếp theo là một chuỗi được trích dẫn hoặc một từ khóa.

### Giá trị ###

Một giá trị chiếm hai dòng, dòng đầu tiên là một cặp số và dòng thứ hai là một chuỗi hoặc một từ khóa. Số đầu tiên của cặp cho biết loại:

* −1 – loại chỉ thị, số thứ hai bị bỏ qua, dòng sau là một trong những từ khóa sau:
** BOT – bắt đầu tuple (bắt đầu hàng)
** EOD – kết thúc dữ liệu
* 0 – kiểu số, giá trị là số thứ hai, dòng sau là một trong các từ khóa sau:
** V – hợp lệ
** NA – không có sẵn
** LỖI – lỗi
** TRUE – giá trị boolean thực
** FALSE – giá trị boolean sai
* 1 – kiểu chuỗi, bỏ qua số thứ 2, dòng sau là chuỗi trong ngoặc kép

### Đoạn tiêu đề DIF ###

Đoạn tiêu đề của tệp DIF bao gồm một dòng định danh theo sau là hai dòng giá trị. Các giá trị số trong các đoạn tiêu đề chỉ sử dụng một chuỗi trống thay vì các từ khóa hợp lệ. Chi tiết của các đoạn tiêu đề này như sau.

* BẢNG - một giá trị số theo sau phiên bản, dòng thứ hai không được sử dụng của giá trị chứa nhận xét của trình tạo
* VECTOR - số cột theo sau là một giá trị số
* TUPLES - số hàng theo sau dưới dạng giá trị số
* DỮ LIỆU - sau một giá trị số 0 giả, dữ liệu cho bảng theo sau, mỗi hàng trước một giá trị BOT, toàn bộ bảng bị kết thúc bởi một giá trị EOD

### Ví dụ DIF ###

Ví dụ sau hiển thị nội dung của một trang tính đơn giản và biểu diễn DIF tương đương của nó.


|Tên|Tuổi
---|---|
|Bob|34
|Tờ giấy|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Người giới thiệu ##

* [ DIF - Theo Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

