{
"ngày": "2023-04-20",
  "keywords": [
"tệp ldb",
"tệp ldb là gì",
"ldb chứa thông tin gì",
"mục đích của tệp ldb là gì",
"phần mở rộng ldb",
"tài liệu",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp LDB - Tệp Microsoft Access Lock",
  "description":"Tìm hiểu về định dạng LDB và nó chứa thông tin gì.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
}
},
"lastmod": "2023-04-20"
}

## Một tập tin LDB là gì?

Tệp LDB là tệp khóa được Microsoft Access sử dụng để ngăn nhiều người dùng chỉnh sửa cùng một cơ sở dữ liệu. Khi người dùng mở cơ sở dữ liệu Access, Access sẽ tạo tệp LDB tương ứng trong cùng thư mục với cơ sở dữ liệu. Tệp này chứa thông tin về người hiện đang sử dụng cơ sở dữ liệu và họ đang chỉnh sửa hồ sơ nào.

Tệp LDB được Microsoft Access tự động tạo khi cơ sở dữ liệu được mở và bị xóa khi đóng cơ sở dữ liệu. Điều quan trọng cần lưu ý là không bao giờ được xóa tệp LDB theo cách thủ công vì điều này có thể gây ra sự cố với cơ sở dữ liệu.

Nếu bạn gặp sự cố với cơ sở dữ liệu Microsoft Access, một giải pháp tiềm năng là thử xóa tệp LDB được liên kết với cơ sở dữ liệu đó. Điều này sẽ giải phóng mọi khóa có thể ngăn bạn truy cập cơ sở dữ liệu. Tuy nhiên, hãy đảm bảo tạo bản sao lưu cơ sở dữ liệu trước khi thực hiện việc này, vì việc xóa tệp LDB có thể gây mất hoặc hỏng dữ liệu nếu thực hiện không đúng cách.

## Định dạng tệp LDB - Thông tin thêm

Tệp LDB trong Microsoft Access chứa thông tin về người dùng hiện đang truy cập cơ sở dữ liệu như tên người dùng, tên máy tính và thời gian đăng nhập của họ. Tệp LDB cũng chứa thông tin về bất kỳ khóa nào đã được đặt trên cơ sở dữ liệu, chẳng hạn như bản ghi nào đang được người dùng nào chỉnh sửa.

Dưới đây là danh sách chi tiết hơn về các loại thông tin có thể tìm thấy trong tệp LDB:

- **Tên người dùng** - tên của người dùng hiện đang truy cập cơ sở dữ liệu
- **Tên máy tính** - tên của máy tính mà người dùng đang truy cập cơ sở dữ liệu từ đó
- **Thời gian đăng nhập** - thời điểm người dùng mở cơ sở dữ liệu lần đầu tiên
- **Khóa bản ghi** - thông tin về bản ghi nào hiện đang được người dùng nào chỉnh sửa
- **Khóa đối tượng** - thông tin về đối tượng cơ sở dữ liệu nào (chẳng hạn như bảng, biểu mẫu hoặc báo cáo) hiện đang được chỉnh sửa bởi người dùng nào
- **Thông tin kết nối** - thông tin về cách người dùng được kết nối với cơ sở dữ liệu (ví dụ: họ đang sử dụng kết nối cục bộ hay mạng)

Thông tin trong tệp LDB được Microsoft Access sử dụng để ngăn nhiều người dùng thực hiện các thay đổi xung đột đối với cùng một cơ sở dữ liệu cùng một lúc. Khi người dùng cố gắng chỉnh sửa một bản ghi hoặc đối tượng đã bị người dùng khác khóa, Microsoft Access sẽ hiển thị thông báo cho biết đối tượng đó đã được sử dụng. Tệp LDB được cập nhật khi người dùng mở và đóng cơ sở dữ liệu cũng như thực hiện các thay đổi đối với các đối tượng bị khóa.

## Người giới thiệu
* [Tệp LDB là gì?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

