{
  "date" : "2021-09-08",
  "keywords" :[ "tệp rel", "định dạng tệp rel", "tệp rel là gì", "tệp", "ví dụ rel", "phần mở rộng tệp rel","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp REL và API có thể tạo và mở tệp REL.",
  "title" :"REL - Tệp mô-đun có thể định vị lại",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Tập tin REL là gì?
Một tệp có phần mở rộng .rel có thể được sử dụng cho nhiều mục đích. Do đó, về mặt phân loại trò chơi, nó được gọi là tệp mô-đun có thể định vị lại được sử dụng bởi một số trò chơi Nintendo Wii, chẳng hạn như Brawl, Super Smash Bros và Mario Kart Wii. Nó bao gồm dữ liệu chơi trò chơi, bao gồm cả mô hình nhân vật và giai đoạn. Các tệp REL hoạt động tương tự như các tệp .DLL được sử dụng bởi Microsoft Windows.

## Định dạng tệp REL
Ở định dạng tệp REL, tệp được chia thành nhiều phần, được nhóm theo quyền truy cập như nhau, ví dụ: chỉ đọc dữ liệu trong một phần, tất cả mã thực thi được đặt trong một phần khác, v.v. Tệp bắt đầu bằng phần tiêu đề, tiếp theo là:
- Bảng chứa thông tin phần.
- Các dữ liệu mặt cắt.
- Thông tin di dời.

### Tiêu đề tệp
Tệp bắt đầu với tiêu đề tối đa 0x4C byte:
| Bù đắp | Kích thước | Tên trường | Mô tả |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Số nhận dạng tùy ý. Phải là duy nhất trong số tất cả các REL được trò chơi sử dụng. Không được bằng 0. |
| 0x04 | 4 | tiếp theo | Con trỏ tới mô-đun tiếp theo, được điền vào thời gian chạy. |
| 0x08 | 4 | trước | Con trỏ tới mô-đun trước đó, được điền vào thời gian chạy. |
| 0x0c | 4 | numSections | Số phần trong tệp. |
| 0x10 | 4 | phầnInfoOffset | Offset đến đầu bảng phần. |
| 0x14 | 4 | tênOffset | Offset thành chuỗi ASCII chứa tên của mô-đun. Có thể là NULL. Liên quan đến phần đầu của tệp REL. |
| 0x18 | 4 | tênKích thước | Kích thước của tên mô-đun tính bằng byte. |
| 0x1c | 4 | phiên bản | Số phiên bản của định dạng tệp REL. |
| 0x20 | 4 | bsSize | Kích thước của phần '.bss'. |
| 0x24 | 4 | relOffset | Offset vào bảng di chuyển. |
| 0x28 | 4 | impOffset | Offset vào bảng imp. |
| 0x2c | 4 | kích thước nhỏ | Kích thước của bảng imp tính bằng byte. |
| 0x30 | 1 | prologSection | Lập chỉ mục vào bảng phần mà prolog có liên quan. Bỏ qua nếu trường này là 0. |
| 0x31 | 1 | phần kết | Lập chỉ mục vào bảng phần mà phần kết có liên quan đến. Bỏ qua nếu trường này là 0. |
| 0x32 | 1 | phần chưa được giải quyết | Chỉ mục vào bảng phần chưa được giải quyết có liên quan đến. Bỏ qua nếu trường này là 0. |
| 0x33 | 1 | bssSection | Lập chỉ mục vào bảng phần mà bss có liên quan. Đã điền vào thời gian chạy! |
| 0x34 | 4 | mở đầu | Offset vào phần được chỉ định của hàm _prolog. |
| 0x38 | 4 | phần kết | Offset vào phần được chỉ định của hàm _epilog. |
| 0x3c | 4 | chưa giải quyết | Offset vào phần được chỉ định của hàm _unresolved. |
| 0x40 | 4 | căn chỉnh | Phiên bản ≥ 2 thôi. Ràng buộc căn chỉnh trên tất cả các phần, được biểu thị bằng lũy thừa của 2. |
| 0x44 | 4 | bssAlign | Phiên bản ≥ 2 thôi. Ràng buộc căn chỉnh trên tất cả phần '.bss', được biểu thị bằng lũy thừa của 2. |
| 0x48 | 4 | fixSize | Phiên bản ≥ 3 thôi. Nếu REL được liên kết với OSLinkFixed (thay vì OSLink), khoảng trống sau địa chỉ này có thể được sử dụng cho các mục đích khác (như BSS). |

### Bảng thông tin phần
Bảng thông tin phần chứa các mục nhập **numSections** với mỗi mục dài 0x8 byte:
| Bù đắp | Kích thước | Mô tả |
-------|------------|-------------|
| 0x0 | 30 bit | Offset từ đầu REL đến phần. Nếu giá trị này bằng 0, phần này là phần chưa được khởi tạo (tức là .bss). |
| 0x3.6 | 1 chút | Không xác định. |
| 0x3.7 | 1 chút | Cờ thi hành; nếu đây là 1 thì phần này có thể thực thi được. |
| 0x4 | 4 | Độ dài tính bằng byte của phần. Nếu giá trị này bằng 0, mục nhập này sẽ bị bỏ qua. |
| 0x8 | Mục tiếp theo | Mục tiếp theo |

### Dữ liệu di dời
Dữ liệu di chuyển là một hoặc nhiều danh sách cấu trúc byte 0x8. Cuối mỗi danh sách được đánh dấu bằng mã loại đặc biệt 203:
| Bù đắp | Tên | Kích thước | Mô tả |
-------|------------|------------|-----|
| 0x0 | bù đắp | 2 | Bù đắp theo byte từ lần di chuyển trước sang lần di chuyển này. Nếu đây là lần di chuyển đầu tiên trong phần, điều này có liên quan đến phần bắt đầu. |
| 0x2 | loại | 1 | Loại tái định cư. Được mô tả dưới đây. |
| 0x3 | phần | 1 | Phần của biểu tượng để di chuyển chống lại. Đối với loại di chuyển đặc biệt 202, thay vào đó, đây là số của phần trong tệp này áp dụng cho các mục nhập di chuyển sau. |
| 0x4 | thêm vào | 4 | Độ lệch theo byte của biểu tượng để định vị lại, so với phần đầu của phần của nó. Đây là một địa chỉ tuyệt đối thay vì di dời đối với main.dol. |
| 0x8 | Mục tiếp theo | Mục tiếp theo | Mục tiếp theo |


 




## Người giới thiệu


* [Định dạng mô-đun đối tượng có thể định vị lại](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


