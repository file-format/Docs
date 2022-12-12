{
  "date" : "2021-06-24",
  "keywords" :[ "tệp bat", "tệp bat là gì", "tệp", "ví dụ về tệp bat", "phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp BAT và API có thể tạo và mở tệp BAT.",
  "title" :"BAT - Định dạng tệp hàng loạt",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Tệp BAT là gì?
Tệp BAT được gọi là tệp bó chạy với DOS và tất cả các phiên bản Windows, dưới cmd.exe. Nó bao gồm một loạt các dòng lệnh ở dạng văn bản thuần túy được thực thi bởi trình thông dịch dòng lệnh để thực hiện các tác vụ khác nhau, chẳng hạn như chạy các tiện ích bảo trì trong Windows hoặc khởi động các chương trình điển hình. Tệp bó có thể bao gồm bất kỳ lệnh nào có thể được trình thông dịch chấp nhận một cách tương tác và sử dụng cấu trúc mã cho phép phân nhánh và lặp có điều kiện như được viết trong tệp bó.
## Định dạng tệp BAT
Định dạng tệp BAT chỉ đơn giản là một tập lệnh được kết hợp để tự động hóa các chuỗi lệnh có tính chất lặp đi lặp lại. Thuật ngữ "batch" được sử dụng để xử lý hàng loạt, Nó có thể được coi là "thực thi không tương tác". Do đó, một tệp bó có thể không xử lý một loạt nhiều dữ liệu. Trong Hệ điều hành đĩa (DOS) cũ, tệp bó được chạy dưới giao diện dòng lệnh bằng cách nhập tên tệp và phần mở rộng .bat. Hệ điều hành dựa trên giao diện đồ họa trước đó của Microsoft như Microsoft Windows phụ thuộc vào DOS. Người dùng phải sử dụng DOS để thực hiện các hoạt động điển hình như sửa chữa, tối ưu hóa hoặc cài đặt lại Windows. Sau đó, Microsoft đã giới thiệu Windows NT không phụ thuộc vào hệ điều hành DOS. Do đó, các tệp lô có thể được chạy bằng cách sử dụng Dấu nhắc Lệnh hoặc **cmd.exe** trong các hệ điều hành Microsoft hiện đại.
### Tham số tệp hàng loạt
Dấu nhắc lệnh hỗ trợ một số biến đặc biệt, chẳng hạn như **%0, %1 đến %9** để tham chiếu đến tên và đường dẫn của công việc theo lô và chín tham số gọi từ bên trong công việc theo lô. Các tham số không tồn tại được thay thế bằng một chuỗi có độ dài bằng không. Mặc dù, chúng có thể được sử dụng tương tự như các biến môi trường, nhưng không được lưu trong môi trường. Microsoft và IBM coi các biến này là tham số thay thế, trong khi Novell, Digital Research và Caldera giới thiệu thuật ngữ biến thay thế cho chúng.

Dưới đây là một số lệnh tệp hàng loạt hữu ích:
| Lệnh | Mô tả |
------|------------|
| PHIÊN BẢN | Lệnh bó này hiển thị phiên bản MS-DOS bạn đang sử dụng. |
|Hiệp hội| Đây là một lệnh hàng loạt liên kết phần mở rộng với một loại tệp (FTYPE), hiển thị các liên kết hiện có hoặc xóa một liên kết. |
|CD| Lệnh bó này giúp thực hiện các thay đổi đối với một thư mục khác hoặc hiển thị thư mục hiện tại. |
|CLS| Lệnh hàng loạt này xóa màn hình. |
|SAO CHÉP| Lệnh bó này được sử dụng để sao chép tệp từ vị trí này sang vị trí khác. |
|DEL| Lệnh bó này xóa các tệp chứ không phải thư mục. |
|TRỰC TIẾP| Lệnh bó này liệt kê nội dung của một thư mục. |
|NGÀY| Lệnh bó này giúp tìm ngày hệ thống. |
|tiếng vang| Lệnh hàng loạt này hiển thị thông báo hoặc bật hoặc tắt lệnh lặp lại. |
|THOÁT| Lệnh bó này thoát khỏi bảng điều khiển DOS. |
|MD| Lệnh bó này tạo một thư mục mới ở vị trí hiện tại. |
|DI CHUYỂN| Lệnh hàng loạt này di chuyển các tệp hoặc thư mục giữa các thư mục. |
|ĐƯỜNG| Lệnh bó này hiển thị hoặc đặt biến đường dẫn. |
|TẠM DỪNG| Lệnh bó này sẽ nhắc người dùng và đợi một dòng đầu vào được nhập vào. |
|THÚC ĐẨY| Lệnh bó này có thể được sử dụng để thay đổi hoặc đặt lại lời nhắc cmd.exe. |
|RD| Lệnh hàng loạt này sẽ xóa các thư mục, nhưng các thư mục cần phải trống trước khi chúng có thể bị xóa. |
|REN| Đổi tên tập tin và thư mục |
|REM| Lệnh bó này được sử dụng cho nhận xét trong tệp bó, ngăn không cho nội dung của nhận xét được thực thi. |
|BẮT ĐẦU| Lệnh bó này bắt đầu một chương trình trong cửa sổ mới hoặc mở một tài liệu. |
|THỜI GIAN| Lệnh bó này đặt hoặc hiển thị thời gian. |
|LOẠI| Lệnh bó này in nội dung của một tệp hoặc nhiều tệp ra đầu ra. |
|VOL| Lệnh bó này hiển thị các nhãn âm lượng. |
|ATTRIB| Hiển thị hoặc đặt thuộc tính của các tệp trong thư mục hiện tại |
|CHKDSK| Lệnh bó này kiểm tra đĩa xem có vấn đề gì không. |
|LỰA CHỌN| Lệnh bó này cung cấp một danh sách các tùy chọn cho người dùng. |
|CMD| Lệnh bó này gọi một phiên bản khác của dấu nhắc lệnh. |
|COMP| Lệnh bó này so sánh 2 tệp dựa trên kích thước tệp. |
|CHUYỂN ĐỔI| Lệnh bó này chuyển đổi một ổ đĩa từ hệ thống tệp FAT16 hoặc FAT32 sang hệ thống tệp NTFS. |
|LÁI XE| Lệnh bó này hiển thị tất cả trình điều khiển thiết bị đã cài đặt và thuộc tính của chúng. |
|MỞ RỘNG| Lệnh hàng loạt này trích xuất các tệp từ các tệp tủ .cab đã nén. |
|TÌM| Lệnh bó này tìm kiếm một chuỗi trong tệp hoặc đầu vào, xuất ra các dòng phù hợp. |
|ĐỊNH DẠNG| Lệnh hàng loạt này định dạng đĩa để sử dụng hệ thống tệp được Windows hỗ trợ như FAT, FAT32 hoặc NTFS, do đó ghi đè lên nội dung trước đó của đĩa. |
|GIÚP ĐỠ| Lệnh bó này hiển thị danh sách các lệnh do Windows cung cấp. |
|IPCONFIG| Lệnh bó này hiển thị Cấu hình IP của Windows. Hiển thị cấu hình theo kết nối và tên của kết nối đó. |
|NHÃN| Lệnh bó này thêm, đặt hoặc xóa nhãn đĩa. |
|THÊM| Lệnh bó này hiển thị nội dung của một tệp hoặc nhiều tệp, mỗi lần một màn hình. |
|MẠNG| Cung cấp các dịch vụ mạng khác nhau, tùy thuộc vào lệnh được sử dụng. |
|PING| Lệnh bó này sẽ gửi các gói "tiếng vang" ICMP/IP qua mạng đến địa chỉ được chỉ định. |
|TẮT| Lệnh bó này tắt máy tính hoặc đăng xuất người dùng hiện tại. |
|SẮP XẾP| Lệnh bó này lấy đầu vào từ một tệp nguồn và sắp xếp nội dung của nó theo thứ tự bảng chữ cái, từ A đến Z hoặc Z đến A. Nó in đầu ra trên bàn điều khiển. |
|SUBST| Lệnh bó này gán một ký tự ổ đĩa cho một thư mục cục bộ, hiển thị các phép gán hiện tại hoặc xóa một phép gán. |
|THÔNG TIN HỆ THỐNG| Lệnh bó này hiển thị cấu hình của máy tính và hệ điều hành của nó. |
|TASKKILL| Lệnh hàng loạt này kết thúc một hoặc nhiều tác vụ. |
|DANH SÁCH NHIỆM VỤ| Lệnh bó này liệt kê các tác vụ, bao gồm tên tác vụ và id tiến trình (PID). |
|XCOPY| Lệnh hàng loạt này sao chép các tệp và thư mục theo cách nâng cao hơn. |
|CÂY| Lệnh bó này hiển thị một cây gồm tất cả các thư mục con của thư mục hiện tại với bất kỳ mức độ đệ quy hoặc độ sâu nào. |
|FC |Lệnh bó này liệt kê sự khác biệt thực tế giữa hai tệp. |
|DISKPART |Lệnh hàng loạt này hiển thị và định cấu hình các thuộc tính của phân vùng đĩa. |
|TITLE |Lệnh lô này đặt tiêu đề được hiển thị trong cửa sổ bảng điều khiển. |
|BỘ | Hiển thị danh sách các biến môi trường trên hệ thống hiện tại. |

## Ví dụ về tệp BAT
Tập lệnh hàng loạt thường được lưu dưới dạng tệp văn bản đơn giản; chứa các lệnh được thực thi theo trình tự. Các tệp này được lưu với phần mở rộng .bat; được nhận dạng và thực thi bằng cách sử dụng phần mềm **Trình thông dịch lệnh**. Phần mềm này vốn có sẵn trong Microsoft Windows với tên **cmd.exe**.

Đây là Batch Script mẫu xóa tất cả các tệp trong thư mục hiện tại:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Người giới thiệu

* [Tập lệnh hàng loạt - Hướng dẫn nhanh](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Tệp lô - theo Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

