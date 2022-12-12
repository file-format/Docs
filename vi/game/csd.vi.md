{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về API và định dạng tệp sao lưu dữ liệu trò chơi CSD Steam.",
  "title" :"Định dạng tệp CSD - Tệp sao lưu dữ liệu trò chơi Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Tệp CSD là gì?

Tệp CSD là tệp sao lưu trò chơi được tạo bởi dịch vụ trò chơi **Steam** cho phép người dùng tải xuống và quản lý các trò chơi **Valve**. Nó chứa dữ liệu sao lưu liên quan đến trò chơi có thể được sử dụng để khôi phục trò chơi đã xóa. Steam chỉ có thể khôi phục trò chơi từ tệp CSD nếu trò chơi đã được tải xuống, cài đặt và vá lỗi hoàn tất thông qua Steam. Để khôi phục trò chơi từ tệp CSD, hãy sử dụng tùy chọn Steam → Backup and Restore Gamesteam và chọn tệp.

## Định dạng tệp CSD - Thông tin khác

Cấu trúc bên trong của định dạng tệp CSD không có sẵn công khai và thông số kỹ thuật định dạng tệp của nó không có sẵn để nhà phát triển tham khảo. Các tệp CSD được kèm theo các tệp CSM và ISS cũng là định dạng tệp trò chơi Steam.

### Tìm tập tin sao lưu Steam ở đâu?

Toàn bộ tệp sao lưu Steam có thể được tìm thấy tại các vị trí sau:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Cấu hình tùy chỉnh và tập lệnh cấu hình
* \downloads\ - Nội dung tùy chỉnh cho trò chơi nhiều người chơi
* \maps\ - Bản đồ tùy chỉnh đã được cài đặt hoặc tải xuống trong trò chơi nhiều người chơi
* \materials\ - Kết cấu và giao diện tùy chỉnh
* \SAVE\ - Trò chơi đã lưu một người chơi

Tuy nhiên, vị trí của các trò chơi do bên thứ ba tạo có thể khác và được xác định bởi nhà phát triển trò chơi.

### Khôi phục từ tệp sao lưu CSD

Cài đặt Steam và đăng nhập đúng tài khoản Steam (xem Cài đặt Steam để biết thêm hướng dẫn)
* Khởi chạy hơi nước
* Nhấp vào "Steam" ở góc trên bên trái của ứng dụng Steam
* Chọn "Sao lưu và khôi phục trò chơi..."
* Chọn "Khôi phục bản sao lưu trước"
* Duyệt đến vị trí của các tập tin sao lưu của trò chơi
* Tiếp tục qua các cửa sổ Steam để cài đặt các game cần thiết.

## Người giới thiệu

* [Sử dụng tính năng sao lưu Steam](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

