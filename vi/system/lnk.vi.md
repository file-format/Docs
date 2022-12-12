{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "phần mở rộng", "tệp", "định dạng", "hệ thống", "tệp LNK", "liên kết", "tệp LNK", "tài liệu LNK", "ứng dụng", "chương trình" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Định dạng tệp liên kết",
  "description":"Tìm hiểu về định dạng tệp LNK và các API có thể tạo và mở tệp LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Tệp LNK là gì? ##

Tệp LNK, tương tự như danh tính trên hệ thống Mac, là một "liên kết" hoặc thay thế Windows đóng vai trò kết nối với thư mục hoặc chương trình tài liệu hình ảnh gốc. Nó chứa loại, vị trí và tên tệp của đích phím tắt, cũng như ứng dụng mở tài liệu đích và một phím tắt bổ sung.

Trong Windows, chuyển thẳng một tệp, thư mục hoặc chương trình thực thi và chọn Tạo lối tắt. Vị trí của định dạng tệp và thư mục “Bắt đầu” là hai tính năng cơ bản của tệp LNK. Định dạng tệp của tệp LNK bị che và mũi tên cong cho biết chúng là lối tắt.

## Định dạng tệp LNK ##

Các định dạng tệp LNK thường có biểu tượng giống như tệp đích của chúng, nhưng có thêm một mũi tên cuộn tròn nhỏ để cho biết rằng tệp trỏ đến một vị trí khác. Khi nhấp đúp vào phím tắt, nó sẽ hoạt động như thể người dùng đã nhấp đúp vào tệp thực tế.

Các tệp LNK chứa lối tắt ứng dụng có thể có các thuộc tính ảnh hưởng đến cách chương trình chạy. Để thay đổi các thuộc tính, nhấp chuột phải vào tệp lối tắt và chọn **Thuộc tính**, sau đó thay đổi trường Mục tiêu.

Thay vì là phần mở rộng tệp, tệp LNK là phần mở rộng của Windows Explorer. Là một phần mở rộng đầu cuối, các tài liệu .lnk chỉ có thể được sử dụng trong Windows Explorer để thay thế một tệp và chúng có các mục đích khác trong Windows Explorer ngoài việc phục vụ như một lối tắt đến một tài liệu cục bộ. Các tệp này cũng bắt đầu bằng chữ "L".

Mặc dù các phím tắt liên kết đến các tệp và thư mục cụ thể khi chúng được tạo, nhưng chúng có thể không hoạt động được nếu mục tiêu được thay đổi sang một vị trí khác. Explorer sẽ bắt đầu sửa chữa một thư mục lối tắt trỏ đến một mục tiêu đã chết khi nó được mở.


## Đặc điểm kỹ thuật ##

Chỉ khi bỏ chọn cài đặt xem thư mục "Ẩn phần mở rộng cho các loại tệp được nhận dạng", Windows mới không hiển thị phần mở rộng tài liệu .lnk cho các lối tắt tài liệu. Mặc dù không nên, nhưng bạn có thể cho phép hiển thị phần mở rộng tệp bằng cách xóa thuộc tính "NeverShowExt" khỏi mục đăng ký tệp Windows HKEY_CLASSES_ROOT\lnk.

Để làm như vậy, hãy thực hiện các bước sau:

* Mở "Registration Editor" bằng cách nhập "Regedit" vào trường tìm kiếm trên thanh tác vụ và chọn chương trình
* Trong ứng dụng, tìm đến vị trí Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Tạo bản sao lưu của mục bằng cách nhấp chuột phải vào mục đó và chọn Xuất
* Chọn và xóa thuộc tính "NeverShowExt"
* Windows nên được khởi động lại


## Tài liệu tham khảo ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
