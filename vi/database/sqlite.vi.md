{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp SQLITE và API có thể tạo và mở tệp SQLITE.",
  "title" :"Định dạng tệp SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Tệp SQLite là gì?

Tệp có phần mở rộng .sqlite là tệp cơ sở dữ liệu SQL nhẹ được tạo bằng phần mềm [SQLite](https://www.sqlite.org/index.html). Bản thân nó là một cơ sở dữ liệu trong một tệp và triển khai một công cụ cơ sở dữ liệu [SQL](/vi/database/sql/) độc lập, đầy đủ tính năng, có độ tin cậy cao. Các tệp cơ sở dữ liệu SQLite có thể được sử dụng để chia sẻ nội dung phong phú giữa các hệ thống bằng cách trao đổi đơn giản các tệp này qua mạng. Hầu như tất cả điện thoại di động và máy tính đều sử dụng SQLite để lưu trữ và chia sẻ dữ liệu, đồng thời là lựa chọn định dạng tệp cho các ứng dụng đa nền tảng. Do sử dụng nhỏ gọn và khả năng sử dụng dễ dàng, nó đi kèm với các ứng dụng khác. Các liên kết SQLite tồn tại cho các ngôn ngữ lập trình như C, [C#](/vi/programming/cs/), [C++](/vi/programming/cpp/), [Java](/vi/programming/java/), [PHP](/vi/programming/php/ ), và nhiều người khác.

## Định dạng tệp SQLite

SQLite trên thực tế là một thư viện Ngôn ngữ C triển khai RDBMS SQLite bằng định dạng tệp SQLite. Với sự phát triển của các thiết bị mới mỗi ngày, định dạng tệp của nó đã được giữ tương thích ngược để phù hợp với các thiết bị cũ hơn. Định dạng tệp SQLite được coi là định dạng lưu trữ lâu dài cho dữ liệu.

### Tệp cơ sở dữ liệu

Cơ sở dữ liệu SQLite được duy trì đầy đủ thông qua hai tệp.
* Tệp cơ sở dữ liệu chính - Chứa trạng thái hoàn chỉnh của cơ sở dữ liệu SQLite
* Rollback Journal - Lưu trữ thông tin bổ sung trong tệp thứ hai và được sử dụng trong quá trình thực hiện giao dịch. Trong trường hợp SQLite ở chế độ WAL, tệp nhật ký đầu ghi được duy trì.

#### Tệp nhật ký

Tệp này nhằm mục đích giữ tất cả thông tin được duy trì trong trường hợp giao dịch cuối cùng không thể hoàn thành trong các trường hợp chẳng hạn như sự cố máy tính. Tệp này được sử dụng để khôi phục tệp cơ sở dữ liệu về trạng thái nhất quán.

#### Trang

Tệp cơ sở dữ liệu SQLite chính bao gồm một hoặc nhiều trang. Tại bất kỳ thời điểm nào, mọi trang trong cơ sở dữ liệu chính đều có một cách sử dụng duy nhất, đó là một trong những cách sau:

* Trang khóa-byte
* Một trang danh sách tự do
* Một trang trung kế freelist
* Một trang lá freelist
* Một trang b-cây
* Một bảng b-cây trang nội thất
* Một bảng b-trang lá cây
* Một trang bên trong b-cây chỉ mục
* Một trang lá b-cây chỉ mục
* Trang tràn tải trọng
* Một trang bản đồ con trỏ

Kích thước của tệp cơ sở dữ liệu SQLite có thể nằm trong khoảng từ vài kilobyte đến vài gigabyte.

### Tiêu đề SQLite

Tiêu đề cơ sở dữ liệu SQLite nằm trong 100 byte đầu tiên của tệp cơ sở dữ liệu. Mọi tệp cơ sở dữ liệu SQLite hợp lệ đều bắt đầu bằng 16 byte (ở dạng hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Chi tiết về các trường tiêu đề như trong bảng sau.

|Độ lệch|Kích thước|Mô tả|
---|---|---|
|0|16|Chuỗi tiêu đề: "SQLite format 3\000"|
|16|2|Kích thước trang cơ sở dữ liệu tính bằng byte. Phải là lũy thừa của hai trong khoảng từ 512 đến 32768 hoặc giá trị 1 biểu thị kích thước trang là 65536.|
|18|1|Phiên bản ghi định dạng tệp. 1 cho di sản; 2 cho WAL.|
|19|1|Định dạng tệp đọc phiên bản. 1 cho di sản; 2 cho WAL.|
|20|1|byte dung lượng "dành riêng" chưa sử dụng ở cuối mỗi trang. Thường là 0.|
|21|1|Phần tải trọng được nhúng tối đa. Phải là 64.|
|22|1|Phần tải trọng được nhúng tối thiểu. Phải là 32.|
|23|1|Phần tải trọng lá. Phải là 32.|
|24|4|Bộ đếm thay đổi tệp.|
|28|4|Kích thước của tệp cơ sở dữ liệu trong các trang. "Kích thước cơ sở dữ liệu trong tiêu đề".|
|32|4|Số trang của trang trung kế tự do đầu tiên.|
|36|4|Tổng số trang danh sách tự do.|
|40|4|Cookie lược đồ.|
|44|4|Số định dạng lược đồ. Các định dạng lược đồ được hỗ trợ là 1, 2, 3 và 4.|
|48|4|Kích thước bộ nhớ cache của trang mặc định.|
|52|4|Số trang của trang b-tree gốc lớn nhất khi ở chế độ tự động hút chân không hoặc tăng dần chân không, hoặc bằng 0 nếu không.|
|56|4|Mã hóa văn bản cơ sở dữ liệu. Giá trị 1 có nghĩa là UTF-8. Giá trị 2 có nghĩa là UTF-16le. Giá trị 3 có nghĩa là UTF-16be.|
|60|4|"Phiên bản người dùng" do pragma user_version đọc và thiết lập.|
|64|4|True (khác không) cho chế độ chân không gia tăng. Sai (không) ngược lại.|
|68|4|"ID ứng dụng" do PRAGMA application_id đặt.|
|72|20|Dành riêng để mở rộng. Phải bằng không.|
|92|4|Số phiên bản hợp lệ.|
|96|4|SQLITE_VERSION_NUMBER|

## Người giới thiệu ##

* [Định dạng tệp SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://vi.wikipedia.org/wiki/SQLite)
* [Thông số ngôn ngữ SQLite - C](https://www.sqlite.org/c3ref/intro.html)

