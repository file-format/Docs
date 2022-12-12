{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Tệp tập lệnh Bash Shell",
  "description":"Tìm hiểu về định dạng tệp SH và các API có thể tạo và mở tệp SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Tệp SH là gì?

Tệp có phần mở rộng .sh là tệp lệnh ngôn ngữ kịch bản chứa chương trình máy tính được chạy bởi Unix shell. Nó có thể chứa một loạt các lệnh chạy tuần tự để thực hiện các hoạt động như xử lý tệp, thực thi chương trình và các tác vụ tương tự khác. Chúng được thực thi từ giao diện dòng lệnh bởi người dùng hoặc theo đợt để thực hiện nhiều thao tác cùng một lúc. Các tệp tập lệnh có thể được mở trong các trình soạn thảo văn bản như Notepad, Notepad ++, Vim, Apple Terminal và các ứng dụng tương tự khác trên Windows, MacOS và Linux OS.

## Định dạng tệp SH

Các tệp SH được viết bằng văn bản thuần túy theo cú pháp đã xác định. Các tệp script này hỗ trợ:

* `Nhận xét` - Nhận xét bắt đầu bằng dấu # và bị trình bao bỏ qua.
* `Phím tắt` - Có thể sử dụng các phím tắt này để đổi tên lệnh để thực hiện ngắn gọn và dễ dàng.
* `Công việc hàng loạt` - Một số lệnh có thể được thực thi tự động mà nếu không thì cần phải nhập thủ công. Điều này loại bỏ nhu cầu đợi người dùng kích hoạt từng giai đoạn của trình tự.
* `Khái quát hóa` - Sử dụng các vòng lặp đơn giản, có thể đạt được khả năng khái quát hóa cao hơn nhiều đối với các thao tác như chuyển đổi hình ảnh từ trạng thái này sang trạng thái khác.

## Ví dụ về tệp SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Làm thế nào để chạy tập tin SH?
Các tệp SH thường chạy trên Linux, ngay cả trong Windows, bạn cần kết nối với thiết bị đầu cuối Linux bằng phần mềm như Putty để chạy các tệp sh. Sau đây là các bước để chạy tệp SH trên thiết bị đầu cuối Linux.

1. Mở thiết bị đầu cuối Linux và chuyển đến thư mục chứa tệp SH.
2. Bằng cách sử dụng lệnh `chmod`, hãy đặt quyền thực thi trên tập lệnh của bạn (nếu chưa được đặt).
3. Chạy tập lệnh bằng một trong các cách sau
1. `./filename.sh`
2. `tên tệp sh.sh`
3. `bash script-name-here.sh`

## Người giới thiệu

* [Bashscripting cho người mới bắt đầu](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

