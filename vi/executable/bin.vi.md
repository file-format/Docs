{
"date" :  "2023-07-20",
   "keywords":[
"THÙNG RÁC",
"Tệp BIN",
"tài liệu",
"Phần mở rộng tệp BIN",
"sự mở rộng",
"tài liệu"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"Định dạng tệp BIN - Tệp thực thi Unix",
   "description":"Tìm hiểu về định dạng BIN và các API có thể tạo và mở tệp BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## Tệp BIN là gì?

Tệp BIN là tệp thực thi trên các hệ điều hành dựa trên Unix như Linux hoặc FreeBSD. Nó chứa một chương trình được biên dịch bao gồm mã nhị phân lấy từ mã nguồn, làm cho nó tương thích với kiến trúc hệ thống cơ bản. Các tệp BIN thực thi Unix có thể được so sánh với các tệp Windows .EXE và tệp macOS .APP về vai trò của chúng là các định dạng thực thi.

Trong lĩnh vực phát triển phần mềm cho hệ thống Unix, các tệp BIN thường được các nhà phát triển sử dụng để đóng gói và phân phối chương trình. Họ cung cấp một phương tiện thuận tiện để cung cấp phần mềm cho người dùng, cho phép cài đặt và thực thi dễ dàng. Bên cạnh các tệp BIN, còn tồn tại các loại tệp thực thi Unix khác, bao gồm [.ELF](/vi/executable/elf/), .X86, [.RUN](/vi/executable/run/) và .X86_64, mỗi loại được điều chỉnh cho phù hợp với phần cứng hoặc phần cứng cụ thể. yêu cầu hệ thống.

Khi nói đến cấu trúc bên trong của tệp BIN, nó bao gồm dữ liệu được mã hóa mà hệ điều hành Unix sử dụng để xác định, đọc và thực thi chương trình kèm theo. Hệ thống dựa vào các chữ ký hoặc tiêu đề tệp cụ thể để nhận dạng tệp BIN là tệp thực thi, sau đó là giải thích và thực thi các lệnh nhị phân có trong đó.

Các tệp BIN thường đi kèm với tệp **INSTALL.TXT** đi kèm, tệp này cung cấp hướng dẫn chi tiết về cách cài đặt và thiết lập chương trình đúng cách. Tài liệu này đảm bảo rằng người dùng có thể điều hướng quá trình cài đặt thành công và bắt đầu sử dụng phần mềm mà không gặp rắc rối.

## Làm cách nào để mở tệp BIN?

Các tệp BIN không được thiết kế để mở và xem trực tiếp. Tuy nhiên, bạn có thể thực thi các chương trình hoặc trích xuất dữ liệu chứa trong đó. Để truy cập nội dung của tệp BIN, hãy làm theo các bước sau trên dòng lệnh, giả sử tên của tệp BIN là "sample.bin":

1. **Đảm bảo quyền thực thi:**

Trước khi thực thi tệp BIN, hãy đảm bảo tệp có các quyền cần thiết để chạy dưới dạng tệp thực thi. Sử dụng lệnh:

```
$ chmod +x sample.bin
```

Lệnh này cấp các đặc quyền thực thi cho tập tin.

2. **Thực thi file BIN:**

Sau khi thiết lập quyền thực thi, bạn có thể chạy tệp BIN bằng cách nhập lệnh sau:

```
$ ./sample.bin
```

**Cảnh báo**

_Hãy thận trọng khi xử lý các tệp BIN được tải xuống hoặc gửi qua email vì chúng có thể bị tội phạm mạng sử dụng để phát tán phần mềm độc hại. Chỉ chạy các tệp BIN từ các nguồn đáng tin cậy để giảm thiểu nguy cơ bị các cuộc tấn công thực thi độc hại._

## Các tập tin BIN khác

Dưới đây là các loại tệp khác sử dụng phần mở rộng tệp **.bin**.

- [BIN - Tệp mã hóa MacBinary](/vi/compression/bin/)
- [BIN - Tệp ảnh đĩa nhị phân](/vi/disc-and-media/bin/)
- [BIN - Tệp chính sách CNTT của BlackBerry](/vi/settings/bin/)
- [BIN - ROM trò chơi Sega Genesis](/vi/game/bin/)
- [BIN - Hình ảnh BIOS PSX PlayStation](/vi/game/bin-pcsx/)

## Người giới thiệu

* [Cách thực thi tệp nhị phân trong Linux](https://linuxhint.com/execute-binary-files-in-linux/)


