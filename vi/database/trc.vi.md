{
  "date" : "2021-08-24",
  "keywords" :[ "tệp trc", "định dạng tệp trc", "tệp trc là gì", "tệp", "ví dụ trc", "phần mở rộng tệp trc","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp TRC và các API có thể tạo và mở tệp TRC.",
  "title" :"TRC - Tệp theo dõi máy chủ SQL",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Tệp TRC là gì?
Tệp có phần mở rộng .trc chứa kết quả theo dõi hoạt động của cơ sở dữ liệu máy chủ Miscrosoft SQL. Các tệp này được tạo bởi phần mềm SQL Server Profiler; thường được đóng gói cùng với phần mềm Microsoft SQL Server. Quản trị viên cơ sở dữ liệu có thể phân tích một chuỗi các câu lệnh cơ sở dữ liệu và có thể xem lại nhật ký theo dõi nếu nghi ngờ có một số loại lỗi hoặc cảnh báo. Các tệp này thường nằm trong thư mục LOG điển hình của MSSQL bên trong thư mục Tệp chương trình trên hệ điều hành Windows.

## Định dạng tệp TRC
Định dạng tệp TRC được SQL Server Profiler sử dụng để tự động tạo dấu vết mới của các câu lệnh được thực hiện gần đây bởi máy chủ MS SQL. SQL Server Profiler sử dụng mẫu mặc định cho bất kỳ dấu vết mới nào. Tuy nhiên, phần mềm bao gồm một số mẫu được xác định trước để theo dõi các loại sự kiện nhất định. Ngoài ra, SQL Server Profiler có thể được sử dụng để tạo các mẫu xác định các lớp sự kiện và cột dữ liệu để đưa vào dấu vết.

### Mẫu được xác định trước
Dưới đây là danh sách một số mẫu được xác định trước có trong SQL Server Profiler:
- **SP_Counts**: Nắm bắt hành vi thực hiện thủ tục được lưu trữ theo thời gian.
- **Tiêu chuẩn**: Điểm bắt đầu chung để tạo dấu vết.
- **TSQL**: Ghi lại tất cả các câu lệnh Transact-SQL được khách hàng gửi tới SQL Server và thời gian ban hành.
- **TSQL_Duration**: Ghi lại tất cả các câu lệnh Transact-SQL do máy khách gửi tới SQL Server, thời gian thực hiện và nhóm chúng theo thời lượng.
- **TSQL_Grouped**: Sử dụng để điều tra các truy vấn từ một khách hàng hoặc người dùng cụ thể.
- **TSQL_Locks**: Sử dụng để khắc phục sự cố bế tắc, khóa thời gian chờ và khóa các sự kiện leo thang.
- **TSQL_Replay**: Sử dụng để thực hiện điều chỉnh lặp lại, chẳng hạn như kiểm tra điểm chuẩn.
- **TSQL_SPs**: Sử dụng để phân tích các bước thành phần của thủ tục lưu trữ.
- **Điều chỉnh**: Sử dụng để tạo đầu ra theo dõi mà Trình tư vấn điều chỉnh công cụ cơ sở dữ liệu có thể sử dụng làm khối lượng công việc để điều chỉnh cơ sở dữ liệu.
### Tương quan dấu vết với dữ liệu Nhật ký hiệu suất Windows
SQL Server Profiler có thể được sử dụng để mở nhật ký hiệu suất Microsoft Windows, để chọn bộ đếm tương quan với một dấu vết và hiển thị bộ đếm hiệu suất đã chọn cùng với dấu vết trong GUI MS SQL Server Profiler. Để biểu thị dữ liệu nhật ký hiệu suất tương quan với sự kiện theo dõi đã chọn, một thanh dọc màu đỏ trong ngăn cửa sổ dữ liệu Giám sát hệ thống của SQL Server Profiler.


## Người giới thiệu ##

* [Trình cấu hình máy chủ SQL](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

