{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp AHK và các API có thể tạo và mở tệp AHK.",
  "title" :"Định dạng tệp AHK- Tệp tập lệnh AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Tệp AHK là gì?

Tệp AHK là tệp tập lệnh được tạo bằng ứng dụng phần mềm AutoHotkey được sử dụng để tự động hóa các tác vụ trong Microsoft Windows. Nó chứa các hướng dẫn để tự động hóa các tác vụ bằng các phím tắt có thể được sử dụng để thực hiện các hành động tức thì. Tệp được thực thi bởi AutoHotkey và tất cả các hành động được thực hiện tuần tự. Các tệp AHK đủ mạnh để thực hiện các tác vụ phức tạp bằng cách sử dụng các phím nóng được xác định bằng các phím nóng. Các tệp AHK có thể được mở bằng các trình soạn thảo văn bản như Microsoft Notepad và Notepad ++.

## Định dạng tệp AHK

Các tệp AHK được lưu vào đĩa dưới dạng tệp văn bản thuần túy và chứa các dòng mã có thể được thực thi bởi AutoHotkey. AutoHotkey là ngôn ngữ kịch bản mã nguồn mở, miễn phí và cho phép người dùng tạo các tập lệnh từ đơn giản đến phức tạp để thực hiện các hành động như điền biểu mẫu, tự động nhấp, thực thi macro, v.v. Một tệp AHK ở mức tối thiểu có thể thực hiện một hành động rồi thoát .

Có sẵn các công cụ có thể được sử dụng để chuyển đổi AHK thành tệp [Exe](/vi/executable/exe/).

### Ví dụ AHK

Ví dụ sau sử dụng phím Win+Z để chạy Microsoft Notepad hoặc đưa nó lên phía trước nếu nó đang chạy.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Làm cách nào để tạo tệp AHK?

Các bước sau đây có thể được sử dụng để tạo tệp AHK. Chúng giả định rằng AutoHotkey đã được cài đặt trên máy.

* Nhấp chuột phải vào màn hình nền của bạn.
* Tìm "Mới" trong menu.
* Nhấp vào "AutoHotkey Script" bên trong menu "Mới".
* Đặt tên mới cho kịch bản.
* Tìm tệp vừa tạo trên màn hình của bạn và nhấp chuột phải vào tệp đó.
* Nhấp vào "Chỉnh sửa tập lệnh".
* Một cửa sổ sẽ bật lên, có thể là Notepad.
* Lưu các tập tin.

## Người giới thiệu

* [AutoHotkey](https://www.autohotkey.com/)
* [Tệp lô - theo Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

