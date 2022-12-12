{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "phần mở rộng", "tệp dbf", "định dạng tệp dbf", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "tệp dbf là gì", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DBF và các API có thể tạo và mở tệp DBF.",
  "title" :"DBF - Tệp cơ sở dữ liệu dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Tệp DBF là gì?
Tệp có phần mở rộng .dbf là tệp cơ sở dữ liệu được sử dụng bởi ứng dụng hệ thống quản lý cơ sở dữ liệu có tên **dBASE**. Ban đầu, cơ sở dữ liệu dBASE được đặt tên là Project Vulcan; bắt đầu bởi **Wayne Ratliff** vào năm 1978. Loại tệp DBF được giới thiệu với dBASE II vào năm 1983. Nó sắp xếp nhiều bản ghi dữ liệu với các trường kiểu Mảng. Phần mềm cơ sở dữ liệu **xBase** phổ biến vì khả năng tương thích với nhiều định dạng tệp; cũng hỗ trợ các tệp DBF.

## Định dạng tệp DBF
Định dạng tệp DBF thuộc về hệ thống quản lý cơ sở dữ liệu dBASE nhưng nó có thể tương thích với xBase hoặc các phần mềm DBMS khác. Phiên bản ban đầu của tệp dbf bao gồm một bảng đơn giản có thể thêm, sửa đổi, xóa hoặc in dữ liệu bằng cách sử dụng bộ ký tự ASCII. Cùng với thời gian, .dbf đã được cải thiện và các tệp bổ sung đã được thêm vào để tăng các tính năng và khả năng của hệ thống cơ sở dữ liệu.

Trong dBASE hiện đại, tệp DBF bao gồm tiêu đề, bản ghi dữ liệu và điểm đánh dấu EOF (Kết thúc tệp)

- Phần đầu chứa thông tin về tệp, chẳng hạn như số lượng bản ghi và số loại trường được sử dụng trong các bản ghi.
- Các bản ghi chứa dữ liệu thực tế.
- Phần cuối của tệp được đánh dấu bằng một byte đơn, có giá trị 0x1A.

### Tiêu đề tệp
Bố cục của tiêu đề tệp trong dBase được đưa ra trong bảng sau:

| Byte | Nội dung | Ý nghĩa |
---|---|---|
| 0 | 1 byte | dBASE hợp lệ cho tệp DOS; bit 0–2 biểu thị số phiên bản, bit 3 biểu thị sự hiện diện của tệp ghi nhớ dBASE cho DOS, bit 4–6 biểu thị sự hiện diện của bảng SQL, bit 7 biểu thị sự hiện diện của bất kỳ tệp ghi nhớ nào (dBASE m PLUS hoặc dBASE cho hệ điều hành) |
| 1–3 | 3 byte | Ngày cập nhật lần cuối; được định dạng là YYMMDD |
| 4–7 | số 32 bit | Số lượng bản ghi trong tệp cơ sở dữ liệu |
| 8–9 | số 16 bit | Số byte trong tiêu đề |
| 10–11 | số 16 bit | Số byte trong bản ghi |
| 12–13 | 2 byte | Kín đáo; điền số 0 |
| 14 | 1 byte | Cờ cho biết giao dịch chưa hoàn tất[chú ý 1] |
| 15 | 1 byte | Cờ mã hóa[chú thích 2] |
| 16–27 | 12 byte | Dành riêng cho dBASE cho DOS trong môi trường nhiều người dùng |
| 28 | 1 byte | Cờ tệp .mdx sản xuất; 1 nếu có tệp .mdx sản xuất, 0 nếu không |
| 29 | 1 byte | ID trình điều khiển ngôn ngữ |
| 30–31 | 2 byte | Kín đáo; điền số 0 |
| 32–n [chú thích 3][chú thích 4] | 32 byte mỗi | mảng các bộ mô tả trường (xem bên dưới để biết cách bố trí các bộ mô tả) |
| n+1 | 1 byte | 0x0D làm bộ kết thúc mảng bộ mô tả trường |

- Hàm ISMARKEDO kiểm tra cờ này (BEGIN TRANSACTION đặt thành 1, END TRANSACTION và ROLLBACK đặt lại thành 0).
- Nếu cờ này được đặt thành 1, thông báo Cơ sở dữ liệu được mã hóa sẽ xuất hiện.
- Số trường tối đa là 255.
- n có nghĩa là byte cuối cùng trong mảng mô tả trường.

### Mảng mô tả trường
Bố cục của bộ mô tả trường trong dBASE:

| Byte | Nội dung | Ý nghĩa |
---|---|---|
| 0–10 | 11 byte | Tên trường trong ASCII (không điền) |
| 11 | 1 byte | Loại lĩnh vực. Các giá trị được phép: C, D, F, L, M hoặc N (xem bảng tiếp theo để biết ý nghĩa) |
| 12–15 | 4 byte | Dành riêng |
| 16 | 1 byte | Độ dài trường ở dạng nhị phân (tối đa 254 (0xFE)). |
| 17 | 1 byte | Số thập phân của trường ở dạng nhị phân |
| 18–19 | 2 byte | ID khu vực làm việc |
| 20 | 1 byte | Ví dụ |
| 21–30 | 10 byte | Dành riêng |
| 31 | 1 byte | Sản xuất cờ lĩnh vực MDX; 1 nếu trường có thẻ chỉ mục trong tệp MDX sản xuất, 0 nếu không |

### Bản ghi cơ sở dữ liệu
Mỗi bản ghi bắt đầu bằng cờ xóa (1 byte). Các trường được bao bọc trong các bản ghi mà không có dấu tách trường. Tất cả dữ liệu trường là ASCII. Tùy thuộc vào loại trường, ứng dụng áp đặt các hạn chế hơn nữa. Đây là các loại trường trong dBase:

| Loại trường | Ghi nhớ | Những gì nó chấp nhận |
-------|-----|----|
| C | Nhân vật | Bất kỳ văn bản ASCII nào (được đệm bằng khoảng trắng theo chiều dài của trường) |
| D| Ngày | Số và ký tự để phân tách tháng, ngày và năm (được lưu trữ nội bộ dưới dạng 8 chữ số ở định dạng YYYYMMDD) |
| | Dấu chấm động | -, ., 0–9 (căn phải, đệm bằng khoảng trắng) |
| l| hợp lý | Y, y, N, n, T, t, F, f, hay ? (khi chưa khởi tạo) |
| M| Ghi nhớ | Bất kỳ văn bản ASCII nào (được lưu trữ nội bộ dưới dạng 10 chữ số đại diện cho số khối .dbt, căn phải, được đệm bằng khoảng trắng) |
| N| Số | -, ., 0–9 (căn phải, đệm bằng khoảng trắng) |









## Người giới thiệu ##

* [.dbf - Wikipedia](https://vi.wikipedia.org/wiki/.dbf)

