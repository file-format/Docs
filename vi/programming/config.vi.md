{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Tệp cấu hình",
  "description":"Tìm hiểu về định dạng tệp CONFIG với ví dụ CONFIG và các API có thể tạo và mở tệp CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Tệp CONFIG là gì?
Tệp CONFIG được gọi là tệp cấu hình; được sử dụng để định cấu hình các tham số và cài đặt chính cho một số phần mềm máy tính. Một số phần mềm chỉ đọc **tệp cấu hình** của chúng khi khởi động. Những người khác kiểm tra các tệp cấu hình để thay đổi định kỳ.

## CẤU HÌNH Định dạng tệp
**Định dạng tệp CONFIG** được sử dụng cho các quy trình máy chủ, ứng dụng phần mềm và cài đặt hệ điều hành. Một lập trình viên có thể viết mã để hướng dẫn phần mềm đọc đi đọc lại các tệp cấu hình sau một khoảng thời gian nhất định và áp dụng các thay đổi cho quy trình hiện tại. Không có tiêu chuẩn rõ ràng hoặc quy ước mạnh mẽ cho hệ thống tệp CONFIG. Ví dụ: tệp Web.config của Microsoft thuộc định dạng tệp CONFIG, bao gồm một bộ thẻ dựa trên [XML](https://docs.fileformat.com/web/xml/); có thể được chỉnh sửa bằng Microsoft Visual Studio hoặc bất kỳ trình soạn thảo văn bản nào khác.

## Ví dụ về các tệp cấu hình:
Vì các tệp cấu hình không được tạo bằng cách tuân theo bất kỳ quy tắc, tiêu chuẩn hoặc quy ước nào nên các tệp này có thể đã được ghi bằng cách sử dụng các định dạng khác nhau. Tệp .config có thể dựa trên XML, [JSON](https://docs.fileformat.com/web/json/) hoặc bất kỳ định dạng nào khác. Sau đây là các ví dụ về tệp cấu hình cho các hệ điều hành và phần mềm nổi tiếng:

### Tệp cấu hình trong Linux
Mọi chương trình Linux đều là một tệp thực thi chứa danh sách **opcodes** mà CPU thực thi để hoàn thành các hoạt động điển hình. Các hoạt động của hầu hết mọi chương trình có thể được tùy chỉnh theo yêu cầu của bạn bằng cách thay đổi các tệp cấu hình của nó. Một số tệp cấu hình trong hệ thống Linux nằm trong thư mục /etc. Các tệp cấu hình có thể được phân loại thành các loại sau:
|Danh mục|Ví dụ| Bình luận|
---|---|---|
|Truy cập tệp|/etc/host.conf|Cho máy chủ miền mạng biết cách tra cứu tên máy chủ.|
|Khởi động và đăng nhập/đăng xuất|/etc/rc.d/rc.local|Không chính thức. Có thể được gọi từ rc, rc.sysinit hoặc /etc/inittab.|
|Hệ thống tệp|/etc/mtools.conf|Cấu hình cho tất cả các thao tác (mkdir, sao chép, định dạng, v.v.) trên hệ thống tệp kiểu DOS.|
|Quản trị hệ thống|/etc/shells|Giữ danh sách các “shell” có thể có cho hệ thống.|
|Mạng|/etc/gated.conf|Cấu hình cho gated. Chỉ được sử dụng bởi daemon gated.|
|Các lệnh hệ thống|/etc/logrotate.conf|Cấu hình cho Trình liên kết động.|
|Daemons|/etc/httpd.conf|Tệp cấu hình cho Apache, máy chủ Web. Tập tin này thường không có trong /etc.|
|Chương trình người dùng| /etc/lynx.cfg| Cài đặt proxy|
### Ví dụ về tệp AWS CONFIG
Thông tin xác thực và cài đặt cấu hình được sử dụng thường xuyên có thể được lưu trong các tệp CONFIG do AWS CLI duy trì. Tệp CONFIG phải là tệp văn bản gốc sử dụng định dạng sau:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Ví dụ về tệp CẤU HÌNH SSH
Tệp cấu hình phía máy khách của OpenSSH có tên là CONFIG và được lưu trữ trong thư mục .ssh. Tệp SSH CONFIG bao gồm cấu trúc sau:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Ví dụ về tệp CONFIG của Python
Tệp CONFIG của Python có thể trông như thế này:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Người giới thiệu

* [Tìm hiểu các tệp cấu hình Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Cài đặt tệp cấu hình và thông tin xác thực](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Tệp cấu hình trong Python](https://martin-thoma.com/configuration-files-in-python/)

