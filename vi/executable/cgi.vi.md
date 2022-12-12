{
  "date" : "2021-06-28",
  "keywords" :[ "tệp cgi", "tệp cgi là gì", "tệp", "ví dụ cgi", "phần mở rộng tệp cgi","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp CGI và các API có thể tạo và mở tệp CGI.",
  "title" :"CGI - Tệp tập lệnh giao diện cổng chung",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Tệp CGI là gì?
Tệp CGI được gọi là tập lệnh Giao diện cổng chung được máy chủ web sử dụng để chạy chương trình bên ngoài nhằm xử lý yêu cầu của người dùng. Tập lệnh được lưu trong tệp có phần mở rộng .cgi thường được viết bằng ngôn ngữ lập trình C hoặc Perl. Nó đã được giới thiệu từ những ngày đầu của Web, khi các nhà phát triển Web muốn kết nối cơ sở dữ liệu với các máy chủ Web của họ. Một máy chủ hỗ trợ một cổng chung giữa máy chủ Web và cơ sở dữ liệu rất phù hợp để thực thi mã CGI.

## Định dạng tệp CGI
Các tập lệnh CGI được máy chủ Web sử dụng để tạo điều kiện cho chủ sở hữu định cấu hình cách xử lý một URL. Quy trình này thường được thực hiện bằng cách đánh dấu một thư mục mới (nơi chủ yếu chứa các tài liệu) là có chứa các tập lệnh CGI; tên thường được biết đến của nó là cgi-bin. Ví dụ: /usr/local/apache/htdocs/cgi-bin có thể được chọn làm thư mục CGI trên máy chủ Web. Khi một trình duyệt Web yêu cầu một URL trỏ đến một tệp trong thư mục CGI, thì thay vì chỉ gửi tệp đó (/vi/usr/local/apache/htdocs/cgi-bin/printenv.pl) tới trình duyệt Web, HTTP máy chủ thực thi tập lệnh đã chỉ định và trả lại đầu ra của tập lệnh cho trình duyệt Web. Nói tóm lại, bất kỳ thứ gì mà tập lệnh CGI được gửi đến đầu ra tiêu chuẩn đều được chuyển đến máy khách Web thay vì được hiển thị trong thiết bị đầu cuối của cửa sổ.

### Ví dụ CGI

Tập lệnh CGI sau được viết bằng Perl hiển thị tất cả các biến môi trường được máy chủ Web chuyển qua:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

Đầu ra sẽ giống như sau:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Công dụng của CGI script
Các tệp CGI chứa tập lệnh CGI thường được sử dụng để xử lý dữ liệu đầu vào từ người dùng và tạo dữ liệu đầu ra có liên quan. Triển khai wiki là một trong những ví dụ về chương trình CGI. Nếu tác nhân người dùng gửi yêu cầu về tên của một mục, thì máy chủ Web sẽ chạy chương trình CGI. Chương trình CGI lấy mã nguồn của trang đó, chuyển đổi nó thành HTML và in kết quả. Máy chủ Web nhận đầu ra từ chương trình CGI và gửi lại cho tác nhân người dùng. Sau đó, nếu tác nhân người dùng gọi chức năng chỉnh sửa bằng cách nhấp vào nút "Chỉnh sửa trang", chương trình CGI sẽ hiển thị vùng văn bản HTML hoặc điều khiển chỉnh sửa khác với nội dung của trang. Cuối cùng, nếu tác nhân người dùng nhấp vào nút "Xuất bản trang", chương trình CGI sẽ chuyển đổi HTML đã cập nhật thành nguồn của trang của mục nhập đó và lưu nó.



## Người giới thiệu

* [Giao diện cổng chung - của Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

