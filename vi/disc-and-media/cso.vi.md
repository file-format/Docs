{
  "date" : "2021-08-09",
  "keywords" :[ "tệp cso", "định dạng tệp cso", "tệp cso là gì", "tệp", "ví dụ cso", "phần mở rộng tệp cso","tiện ích mở rộng", "định dạng", "iso", "Nén DAX " ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp CSO và các API có thể tạo và mở tệp CSO.",
  "title" :"CSO - Ảnh đĩa ISO được nén",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Tệp CSO là gì?

Tệp có phần mở rộng .cso là tệp ảnh ISO được nén. CSO là một giải pháp thay thế cho phương pháp nén DAX; còn được gọi là CISO; là phương pháp đầu tiên để nén các tệp [ISO](/vi/compression/iso/) và thường là phương pháp ưa thích để lưu trữ nội dung PlayStation Portable. Định dạng này sử dụng nén Deflate, có thể bao gồm tối đa chín lớp nén. Phần mềm như Prometheus và YACC được sử dụng để tạo hình ảnh.

## Định dạng tệp CSO

Định dạng tệp CSO là phương pháp nén đầu tiên cho ISO để tiết kiệm thêm dung lượng bộ nhớ. Các cải tiến được thực hiện theo thời gian để nén tốt hơn. CSO đang sử dụng nén Deflate có chín cấp độ cài đặt trước, thông thường, mỗi cấp độ có thể xử lý 2 khối KiB riêng lẻ. Mặc dù các mức nén cao nhất có thể làm chậm và kéo dài thời gian tải trong phần mềm phụ thuộc nhiều vào truyền phát đĩa, nhưng các mức thấp hơn cũng có thể thực hiện nén đáng kể.

### Cấu trúc tệp CSO

Định dạng tệp CSO chứa tiêu đề 24 byte, khối dữ liệu và bảng chỉ mục. Little-endian được giả định cho các trường lớn hơn một byte. Độ bền kiến trúc của PlayStation Portable được đưa ra dưới đây.

#### Tiêu đề

| Độ lệch (byte) | Tên | Kích thước (byte) | Mục đích |
----------|----------|--------------|---------|
| 0x0 | Phép thuật | 4 | Luôn là CISO hoặc 0x4F534943 khi được đọc dưới dạng số nguyên 32 bit. Trường này được sử dụng để xác định tệp CSO. Lưu ý rằng trường này có thể khác đối với các dẫn xuất khác của CSO, ví dụ: ZSO đã sử dụng mã ma thuật ZISO. |
| 0x4 | Kích thước tiêu đề | 4 | Đối với định dạng tệp CSO "v1" ban đầu, trường này bị bỏ qua và do đó không bắt buộc phải chính xác. Tuy nhiên, định dạng "v2" và ZSO yêu cầu trường này luôn là 0x18 (24 byte). |
| 0x8 | Kích thước không nén | 8 | Kích thước của ISO không nén ban đầu tính bằng byte. |
| 0x10 | Kích thước khối | 4 | Kích thước của mỗi khối dữ liệu tính bằng byte trước khi nén. Thông thường là 2048 byte, giống như kích thước của từng cung theo tiêu chuẩn ISO 9660. |
| 0x14 | Phiên bản | 1 | Phiên bản của định dạng tệp đang sử dụng. Đối với định dạng "v1", giá trị có thể là 0 hoặc 1. Đối với định dạng "v2", giá trị này phải là 2. Ngoài ra, định dạng ZSO yêu cầu giá trị này phải là 1. |
| 0x15 | Căn chỉnh chỉ mục | 1 | Căn chỉnh của mỗi mục nhập chỉ mục, được chỉ định bằng bit. |
| 0x16 | Dành riêng | 2 | Trường này không được sử dụng. Ở định dạng "v1", trường này bị bỏ qua và có thể chứa các giá trị tùy ý. Ở định dạng "v2", trường này phải bằng không. |

#### Bảng chỉ mục

Bảng chỉ mục chứa một số mục 4 byte, cho biết vị trí của từng khối dữ liệu và một mục bổ sung, cuối cùng trỏ đến cuối tệp.
Nội dung từng entry như sau:
| Chút | Chiều dài | Mặt nạ | Tên | Mục đích |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Vị trí | Trường này, khi được dịch chuyển sang trái bởi căn chỉnh chỉ mục được cung cấp trong tiêu đề, sẽ đưa ra vị trí bắt đầu khối dữ liệu. |
| 31 | 1 | 0x80000000 | Loại nén | Định dạng ZSO có ngữ nghĩa tương tự, chỉ có điều 0 đại diện cho LZ4 thay vì Deflate. Ở định dạng "v2". Khối được coi là không nén nếu kích thước khối bằng hoặc lớn hơn kích thước khối được chỉ định trong tiêu đề tệp. |

#### Khối dữ liệu

Các khối dữ liệu bao gồm dữ liệu không nén hoặc nén. Kích thước của một khối được tính bằng cách lấy vị trí của nó, sau đó trừ nó khỏi vị trí của khối tiếp theo. Nếu căn chỉnh chỉ mục lớn hơn 0, có khả năng kích thước khối lớn hơn dữ liệu mà nó chứa.


## Người giới thiệu

* [CSO - theo Wikipedia](https://en.wikipedia.org/wiki/.CSO)


