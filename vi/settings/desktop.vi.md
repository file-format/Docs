{
"ngày": "2023-05-31",
  "keywords": [
"tệp máy tính để bàn",
"tệp máy tính để bàn là gì",
"tệp máy tính để bàn chứa gì",
"ví dụ về tệp máy tính để bàn",
"cách mở tập tin trên máy tính",
"định dạng của tệp máy tính để bàn là gì",
"tài liệu",
"phần mở rộng tập tin máy tính để bàn",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp DESKTOP - Tệp mục nhập trên máy tính để bàn",
  "description":"Tìm hiểu về định dạng DESKTOP và các API có thể tạo và mở tệp DESKTOP.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## Tệp DESKTOP là gì?

Tệp .desktop là tệp cấu hình được môi trường máy tính để bàn Linux sử dụng để xác định các phím tắt và trình khởi chạy ứng dụng. Nó cung cấp siêu dữ liệu về một ứng dụng như tên, biểu tượng, lệnh thực thi và các thuộc tính khác. Các tệp này thường được sử dụng để tạo lối tắt trong menu ứng dụng, trình khởi chạy máy tính để bàn hoặc bảng điều khiển trong các hệ thống dựa trên Linux.

## Tệp DESKTOP chứa gì?

Tệp .desktop tuân theo định dạng cụ thể và chứa một số trường chính:

- **[Desktop Entry]:** Đây là tiêu đề phần chính cho tệp .desktop.
- **Tên:** Chỉ định tên của ứng dụng.
- **Nhận xét:** Cung cấp mô tả hoặc nhận xét ngắn gọn về ứng dụng.
- **Exec:** Xác định lệnh thực thi khi khởi chạy ứng dụng.
- **Biểu tượng:** Chỉ định đường dẫn đến tệp biểu tượng được liên kết với ứng dụng.
- **Terminal:** Chỉ định xem ứng dụng có chạy trong cửa sổ terminal hay không.
- **Loại:** Chỉ định loại mục nhập chẳng hạn như "Ứng dụng" hoặc "Liên kết".
- **Danh mục:** Chỉ định danh mục hoặc nhóm mà ứng dụng sẽ được hiển thị trong menu.
- **StartupNotify:** Chỉ định xem môi trường máy tính để bàn có hiển thị thông báo khởi động cho ứng dụng hay không.
- **NoDisplay:** Chỉ định xem có nên ẩn ứng dụng khỏi menu hay không.
- **Hành động:** Xác định các hành động bổ sung có thể được thực hiện trên ứng dụng, chẳng hạn như mở một tệp cụ thể.

## Ví dụ về tệp DESKTOP

Dưới đây là ví dụ về tệp .desktop dành cho trình soạn thảo văn bản hư cấu có tên "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Trong ví dụ này, tệp .desktop xác định ứng dụng "MyTextEditor" với các thuộc tính liên quan của nó. Nó cũng bao gồm hai hành động bổ sung, "Mở cửa sổ mới" và "Mở tệp hiện có", có thể được truy cập từ menu ngữ cảnh của trình khởi chạy ứng dụng.

Bằng cách đặt tệp .desktop trong các thư mục cụ thể, chẳng hạn như `/usr/share/applications` hoặc `~/.local/share/applications`, môi trường máy tính để bàn sẽ nhận dạng nó và hiển thị ứng dụng tương ứng trong menu hoặc cho phép nó được khởi chạy từ máy tính để bàn.

## Làm cách nào để mở tệp DESKTOP?

Một số chương trình phần mềm có thể mở và xử lý các tệp .desktop. Các chương trình này thường là trình quản lý tệp hoặc môi trường máy tính để bàn trên các hệ thống dựa trên Linux. Dưới đây là một số ví dụ:

- **Nautilus (Tệp):** Trình quản lý tệp mặc định cho môi trường máy tính để bàn Gnome.
- **Nemo:** Trình quản lý tệp cho môi trường máy tính để bàn Cinnamon.
- **Dolphin:** Trình quản lý tệp mặc định cho môi trường máy tính để bàn KDE Plasma.
- **Thunar:** Trình quản lý tệp mặc định cho môi trường máy tính để bàn Xfce.
- **Trình chỉnh sửa menu KDE:** Một công cụ dành riêng cho môi trường máy tính để bàn KDE Plasma cho phép bạn xem và chỉnh sửa các tệp .desktop.

Các trình quản lý tệp và môi trường máy tính để bàn này cung cấp giao diện đồ họa để quản lý các tệp .desktop. Chúng cho phép bạn xem và chỉnh sửa các thuộc tính của tệp .desktop, tạo trình khởi chạy ứng dụng và sắp xếp các phím tắt trong menu ứng dụng hoặc trên màn hình nền.

Các tệp .desktop là các tệp văn bản thuần túy, vì vậy bạn cũng có thể mở và chỉnh sửa chúng bằng trình soạn thảo văn bản mà bạn chọn. Chỉ cần nhấp chuột phải vào tệp .desktop và chọn "Mở bằng" hoặc "Mở bằng ứng dụng khác" để chọn trình soạn thảo văn bản từ danh sách các chương trình đã cài đặt.

## Định dạng của tệp DESKTOP là gì?

Định dạng tệp .desktop tuân theo cấu trúc và định dạng cụ thể. Nó là một tệp văn bản đơn giản với một tập hợp các cặp khóa-giá trị được sắp xếp thành các phần. Dưới đây là tổng quan về định dạng:

- **Tiêu đề phần:** Mỗi phần bắt đầu bằng tiêu đề được đặt trong dấu ngoặc vuông ([]). Phần chính thường được đặt tên là [Mục nhập trên màn hình], chứa siêu dữ liệu chính cho ứng dụng hoặc trình khởi chạy.
- **Cặp khóa-giá trị:** Trong mỗi phần, bạn xác định thuộc tính bằng cặp khóa-giá trị. Định dạng là "Khóa = Giá trị". Khóa xác định thuộc tính và giá trị cung cấp dữ liệu tương ứng.
- **Cú pháp thuộc tính:** Các giá trị thuộc tính có thể thuộc nhiều loại khác nhau bao gồm chuỗi, giá trị boolean, đường dẫn tệp hoặc danh sách. Định dạng cho mỗi giá trị thuộc tính phụ thuộc vào loại của nó.
- **Nhận xét:** Bạn có thể đưa nhận xét vào tệp .desktop bằng ký hiệu '#'. Bất cứ điều gì theo sau '#' trên mạng đều được coi là nhận xét và bị bỏ qua.

## Người giới thiệu
* [Tệp mục nhập trên máy tính để bàn](https://www.baeldung.com/linux/desktop-entry-files)

