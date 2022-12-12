{
  "date" : "2019-10-11",
  "keywords" :[ "tệp aba", "định dạng tệp aba", "tệp aba là gì", "tệp", "ví dụ aba", "phần mở rộng tệp aba","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - Định dạng tệp CemText",
  "description":"Tìm hiểu về định dạng tệp ABA và các API có thể tạo và mở tệp ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Tệp ABA là gì?

Tệp có phần mở rộng .aba là định dạng tệp của Hiệp hội Ngân hàng Úc (ABA) hoặc [Cemtext](https://www.cemtexaba.com/) được các ngân hàng sử dụng cho các giao dịch theo lô. Nó được hầu hết các Ngân hàng sử dụng để lưu giữ hồ sơ tài chính. Còn được gọi là tệp Nhập trực tiếp, định dạng tệp ABA đã được hầu hết các ngân hàng Úc áp dụng làm định dạng mặc định cho các giao dịch hàng loạt. Nó vẫn chưa được công nhận là định dạng Chuẩn mặc dù nó đã được sử dụng bởi Ngân hàng Queensland, NAB và Westpac. Các tệp ABA có thể được mở bằng bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Notepad ++.


## Định dạng tệp ABA

Tệp ABA sử dụng định dạng ASCII để lưu trữ dữ liệu để chuyển tiếp hoặc tải vào hệ thống ngân hàng. Định dạng đã được giữ đơn giản để giúp dễ dàng tích hợp vào hệ thống tài chính của chính công ty để xử lý các lô giao dịch. Ví dụ: trong hệ thống tính lương, một lô giao dịch có thể được tải lên để xử lý trong một lần truy cập. Thông số định dạng tệp ABA có sẵn dưới dạng bản ghi đầy đủ trên trang web [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) và có thể được giới thiệu để nhà phát triển tham khảo .

Tệp ABA bao gồm nhiều dòng trong đó mỗi dòng được gọi là `bản ghi`. Có ba bản ghi chính trong tệp ABA:

* Hồ sơ mô tả
* Bản ghi chi tiết
* Tệp Tổng số bản ghi

### Bản ghi mô tả

`Bản ghi Mô tả` chứa thông tin như Số thứ tự Cuộn phim, Tên Tổ chức Tài chính của Người dùng, Tệp cung cấp Tên Sử dụng và các thông tin khác.

### Bản ghi chi tiết

Loại `Bản ghi chi tiết` bao gồm các thông tin như Số ngân hàng/bang/chi nhánh, số tài khoản được ghi có/ghi nợ, chỉ báo, mã giao dịch, số tiền và các thông tin khác.

### Tệp Tổng số Bản ghi

Loại "Bản ghi tổng tệp" bao gồm Loại bản ghi 7, Trình điền định dạng BSB, Tổng số tiền ròng của tệp (người dùng), Tổng số tiền ghi có tệp (người dùng), Tổng số tiền ghi nợ tệp (người dùng) và các thông tin khác.

### Mã giao dịch

Danh sách các mã giao dịch hợp lệ như sau. Hầu hết thời gian, mã "53 - Thanh toán" được sử dụng trong các tệp ABA. Các mã giao dịch này kéo dài các khoản ghi nợ, tín dụng và thuế khấu trừ.

|Mã số|Mô tả giao dịch|
---|---|
|13|Các khoản mục ghi nợ bên ngoài|
|50|Các hạng mục tín dụng được khởi xướng bên ngoài ngoại trừ những hạng mục có Mã giao dịch|
|51|Lợi ích an ninh của chính phủ Úc|
|52|Trợ cấp gia đình|
|53|Trả|
|54|Hưu trí|
|55|Phân bổ|
|56|Cổ tức|
|57|Trái phiếu/Lãi trái phiếu|

## Ví dụ về tệp ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Người giới thiệu

* [Cemtext ABA](https://www.cemtexaba.com/)

