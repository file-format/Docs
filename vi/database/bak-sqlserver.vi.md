{
"ngày": "2023-06-12",
  "keywords": [
"bak",
"tập tin bak",
"Sao lưu cơ sở dữ liệu Microsoft SQL Server",
"tập tin bak là gì",
"cách mở tập tin bak",
"tài liệu",
"phần mở rộng tập tin bak",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp BAK - Sao lưu cơ sở dữ liệu Microsoft SQL Server",
  "description":"Tìm hiểu về định dạng BAK SQL Server Backup và các API có thể tạo và mở tệp BAK.",
"linktitle":"Máy chủ SQL BAK",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Tập tin BAK là gì?

Tệp ".bak", trong ngữ cảnh của Microsoft SQL Server, là định dạng tệp sao lưu được sử dụng để lưu trữ các bản sao của cơ sở dữ liệu SQL Server. Các tệp này chứa ảnh chụp nhanh của cơ sở dữ liệu tại một thời điểm cụ thể, bao gồm lược đồ, dữ liệu và thông tin liên quan khác. Chúng được tạo bằng chức năng sao lưu và khôi phục tích hợp của SQL Server và phục vụ một số mục đích quan trọng:

1. **Phục hồi dữ liệu:** Tệp .bak cung cấp phương tiện để khôi phục cơ sở dữ liệu trong trường hợp mất dữ liệu, hỏng hoặc các vấn đề khác. Bằng cách khôi phục cơ sở dữ liệu từ tệp .bak, bạn có thể hoàn nguyên cơ sở dữ liệu về trạng thái trước đó, giảm thiểu thời gian ngừng hoạt động và mất dữ liệu.

2. **Di chuyển và nhân bản:** Tệp sao lưu thường được sử dụng để di chuyển cơ sở dữ liệu giữa các máy chủ hoặc tạo bản sao cơ sở dữ liệu cho mục đích thử nghiệm, phát triển hoặc báo cáo. Họ cung cấp một cách nhất quán và hiệu quả để di chuyển cơ sở dữ liệu giữa các môi trường.

3. **Khôi phục tại thời điểm:** SQL Server cho phép bạn thực hiện khôi phục tại thời điểm bằng cách sử dụng tệp .bak. Điều này có nghĩa là bạn có thể khôi phục cơ sở dữ liệu vào một thời điểm cụ thể, điều này có thể rất quan trọng đối với việc tuân thủ quy định hoặc kiểm tra dữ liệu.

4. **Khôi phục sau thảm họa:** Tệp .bak là một phần quan trọng trong kế hoạch khắc phục thảm họa. Chúng đảm bảo rằng dữ liệu của bạn được an toàn và có thể được khôi phục nhanh chóng trong trường hợp xảy ra lỗi phần cứng, thiên tai hoặc các sự kiện thảm khốc khác.

## Tạo tệp .BAK trong SQL Server

Để tạo tệp .bak trong SQL Server, bạn thường sử dụng các lệnh SQL Server Management Studio (SSMS) hoặc Transact-SQL (T-SQL) như BACKUP DATABASE hoặc BACKUP LOG. Dưới đây là ví dụ đơn giản về cách bạn có thể tạo bản sao lưu cơ sở dữ liệu bằng T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Khôi phục tệp .BAK trong SQL Server

Để khôi phục cơ sở dữ liệu từ tệp .bak, bạn có thể sử dụng lệnh RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Làm cách nào để mở tệp BAK trong SQL Server?

Để mở và truy cập dữ liệu được lưu trữ trong tệp ".bak", bạn thường cần khôi phục dữ liệu đó về phiên bản Microsoft SQL Server. Dưới đây là các bước chung để mở tệp ".bak" bằng SQL Server Management Studio (SSMS):

1. **Khởi chạy SQL Server Management Studio**: Mở SSMS trên máy tính của bạn. Bạn thường có thể tìm thấy nó trong Menu Bắt đầu hoặc bằng cách tìm kiếm "SQL Server Management Studio".

2. **Kết nối với phiên bản SQL Server**: Trong SSMS, kết nối với phiên bản SQL Server mà bạn muốn khôi phục cơ sở dữ liệu. Bạn sẽ cần có các quyền cần thiết để thực hiện thao tác này.

3. **Khôi phục cơ sở dữ liệu**:

Một. Trong ngăn Object Explorer ở phía bên trái, hãy mở rộng phiên bản SQL Server.

b. Mở rộng nút "Cơ sở dữ liệu".

c. Nhấp chuột phải vào "Cơ sở dữ liệu" và chọn "Khôi phục cơ sở dữ liệu".

4. **Chỉ định nguồn và đích**:

Một. Trong trang "Chung" của hộp thoại "Khôi phục cơ sở dữ liệu", nhập tên cho cơ sở dữ liệu mới vào trường "Tới cơ sở dữ liệu". Đây sẽ là tên của cơ sở dữ liệu được khôi phục.

b. Trong phần "Nguồn", chọn "Thiết bị" làm loại phương tiện sao lưu.

c. Nhấp vào nút "..." bên cạnh trường "Thiết bị" để duyệt tìm tệp ".bak" bạn muốn khôi phục.

d. Chọn tệp ".bak" bạn muốn mở và nhấp vào "OK."

5. **Tùy chọn khôi phục**: Xem lại và định cấu hình các tùy chọn khôi phục nếu cần. Bạn có thể chỉ định có ghi đè cơ sở dữ liệu hiện có hay không, đặt tùy chọn khôi phục, v.v. Đảm bảo đặt các tùy chọn này theo yêu cầu của bạn.

6. **Bắt đầu Khôi phục**: Sau khi bạn đã định cấu hình các tùy chọn khôi phục, hãy nhấp vào nút "OK" trong hộp thoại "Khôi phục cơ sở dữ liệu". SQL Server sẽ bắt đầu quá trình khôi phục.

7. **Truy cập cơ sở dữ liệu đã khôi phục**: Sau khi khôi phục thành công, bạn có thể truy cập cơ sở dữ liệu đã khôi phục trong SQL Server Management Studio giống như bất kỳ cơ sở dữ liệu nào khác. Bạn có thể chạy truy vấn, xem bảng và làm việc với dữ liệu trong cơ sở dữ liệu.

## Các tập tin BAK khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.bak**.

**Cơ sở dữ liệu**
- [BAK - Tệp sao lưu cơ sở dữ liệu](/vi/database/bak/)
- [BAK - Đạo luật Swiftpage! Sao lưu cơ sở dữ liệu](/vi/database/bak-act/)

**Trò chơi**
- [BAK - Thế giới Terraria hoặc Sao lưu người chơi](/vi/game/bak-terraria/)

**Khác**
- [BAK - Tệp sao lưu](/vi/misc/bak-backup/)
- [BAK - Sao lưu dấu trang Chrome](/vi/misc/bak-chromium/)
- [BAK - Sao lưu điểm chung kết 2012](/vi/misc/bak-finale/)
- [BAK - Sao lưu MobileTrans](/vi/misc/bak-mobiletrans/)
- [BAK - Sao lưu dự án video VEGAS](/vi/misc/bak-vegas/)

**Cài đặt**
- [BAK - Sao lưu trình khởi chạy Holo](/vi/settings/bak-holo/)

## Người giới thiệu
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
