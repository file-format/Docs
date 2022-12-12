{
  "date" : "2021-06-30",
  "keywords" :[ "tệp exe", "định dạng tệp exe", "tệp exe là gì", "tệp", "ví dụ exe", "phần mở rộng tệp exe","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tệp .exe là tệp Microsoft Executable chạy trên HĐH Windows. Tìm hiểu thêm về định dạng tệp EXE.",
  "title" :"Tệp EXE có thể thực thi là gì?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Tệp EXE là gì?

Từ EXE là viết tắt của **executable**. Tệp .exe là một chương trình có thể được thực thi trên hệ điều hành Microsoft Windows. Các nhà phát triển ứng dụng chủ yếu xuất bản các chương trình của họ cho HĐH Windows ở định dạng thực thi dưới dạng tệp exe. Đây là định dạng tệp tiêu chuẩn để chạy các ứng dụng trên Windows. **Setup.exe**, **Install.exe** và **cmd.exe** là một số tên phổ biến và quen thuộc của các tệp EXE.

## Định dạng tệp EXE

Trình biên dịch MS-DOS được giới thiệu với các kiểu bộ nhớ có giới hạn bộ nhớ 64K. Khái niệm chung là đặt các thanh ghi phân đoạn khác nhau trong CPU x86 (CS, DS, ES, SS) để trỏ đến các phân đoạn khác nhau hoặc giống nhau, do đó cho phép các mức độ truy cập bộ nhớ khác nhau. Một số mô hình bộ nhớ cụ thể là:

- **Tiny**: Tất cả truy cập bộ nhớ là 16 bit (thanh ghi phân đoạn không thay đổi). Tạo tệp .COM thay vì tệp .EXE.
- **Small**: Tất cả truy cập bộ nhớ là 16-bit (thanh ghi phân đoạn không thay đổi).
- **Compact**: Địa chỉ dữ liệu bao gồm cả phân đoạn và độ lệch, tải lại các thanh ghi DS hoặc ES khi truy cập và cho phép tối đa 1M dữ liệu. Truy cập mã không thay đổi thanh ghi CS, cho phép 64K mã.
- **Trung bình**: Địa chỉ mã bao gồm địa chỉ phân đoạn, tải lại CS khi truy cập và cho phép tối đa 1M mã. Truy cập dữ liệu không thay đổi thanh ghi DS và ES, cho phép 64K dữ liệu.
- **Large**: Cả địa chỉ mã và dữ liệu đều là cặp (phân đoạn, độ lệch), luôn tải lại các địa chỉ phân đoạn. Toàn bộ không gian bộ nhớ 1M byte có sẵn cho cả mã và dữ liệu.
- **Lớn**: Giống như mô hình lớn, với phép toán bổ sung được tạo bởi trình biên dịch để cho phép truy cập vào các mảng lớn hơn 64K.

Các nhà phát triển phải quyết định nên chọn mô hình nào trong khi tạo tệp exe.

### Định dạng tệp EXE di động

Định dạng tệp thực thi di động (PE) chứa một số tiêu đề thông tin, sau đây là danh sách các tiêu đề:

- **Tiêu đề DOS**: Tiêu đề MS-DOS đảm bảo khả năng tương thích ngược hoặc từ chối nhẹ nhàng các loại tệp mới.
- **PE Header**: Tại offset 60 (0x3C) tính từ đầu DOS header là một con trỏ tới PE File header
- **Tiêu đề COFF**: Tiêu đề COFF có một số thông tin hữu ích cho tệp thực thi và một số thông tin hữu ích hơn cho tệp đối tượng.
- **Tiêu đề tùy chọn PE**: Tiêu đề tùy chọn PE xuất hiện ngay sau tiêu đề COFF và một số nguồn thậm chí còn hiển thị hai tiêu đề là một phần của cùng một cấu trúc.
- **Bảng phần**: Ngay sau Tiêu đề tùy chọn PE, chúng tôi tìm thấy một bảng phần. Bảng phần bao gồm một mảng cấu trúc IMAGE_SECTION_HEADER.
- **Phần có thể ánh xạ**: Có thể tiết kiệm dung lượng trong bộ nhớ bằng cách ánh xạ mã của thư viện vào nhiều quy trình.

## Bạn có thể chạy tệp EXE trên máy Mac không?

Các tệp exe không được sử dụng làm tệp thực thi trên Mac OS. Tuy nhiên, nếu bạn muốn chạy tệp exe trên Mac OS, có thể sử dụng các phương pháp sau.

1. **Wine** - Wine là giải pháp hoàn hảo cho những người muốn sử dụng ứng dụng PC của họ trên hệ thống Mac. Đó là từ viết tắt của "Wine Is Not A Emulator", có nghĩa là. Wine tạo môi trường thư mục giống như môi trường được Microsoft sử dụng để bạn có thể chạy ứng dụng Windows của mình bằng cách sử dụng nó.
2. **Máy ảo** - Tạo Máy ảo Windows bằng Parallel Desktop hoặc VM Virtual Box và chạy ứng dụng của bạn bên trong máy ảo.
3. **Boot Camp** - Cài đặt và định cấu hình Windows Boot Camp trên Mac OS cho phép bạn chạy Windows OS trên máy Mac.

## Người giới thiệu

* [.exe- của Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [X86 Disassembly/Tệp thực thi Windows](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

