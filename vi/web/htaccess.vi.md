{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp HTACCESS - Định dạng tệp HTACCESS của Apache",
  "description" :"Hướng dẫn định dạng tệp của bạn để tìm hiểu tệp HTACCESS là gì",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp HTACCESS là gì?

Tệp HTACCESS là tệp cấu hình Apache cung cấp cơ chế cho phép thay đổi cấu hình cho các thư mục/thư mục khác nhau của trang web. Nó bao gồm các chỉ thị cấu hình có thể áp dụng cho thư mục và thư mục con.

Tệp HTACCESS thực hiện một số kiểm tra như xác định trang chỉ mục của trang web, liệt kê trang lỗi 404 (Không tìm thấy trang), thực hiện chuyển hướng trang 301 hoặc 302, chặn truy cập từ một địa chỉ IP cụ thể hoặc các trang web khác. Do đó, việc sử dụng các tệp .htaccess sẽ làm chậm hiệu suất tổng thể của máy chủ Apache [HTTP](/vi/web/http/).

## Định dạng tệp HTACCESS

Các tệp HTACCESS được lưu vào đĩa ở định dạng tệp văn bản thuần túy. Điều này có nghĩa là bạn có thể mở và chỉnh sửa các tệp này trong bất kỳ trình soạn thảo văn bản nào. Không có tên trước dấu "." trong một tệp .htaccess, cho thấy rằng đó là một tệp ẩn trong thư mục.

## Các cách sử dụng phổ biến của Tệp HTACCESS

Năm cách sử dụng phổ biến của tệp HTACCESS như sau.

### Mod_Rewrite

Tệp HTACCESS có thể được sử dụng để chỉ định và thay đổi cách hiển thị URL và trang web trên trang web cho người dùng.

### Xác thực

Có thể đạt được xác thực với .htaccess bằng cách tạo tệp mật khẩu có tên .htpasswd. Điều này cho phép khách truy cập trang web cung cấp mật khẩu nếu họ muốn truy cập một phần nhất định của trang web.

### Trang lỗi tùy chỉnh

Bạn có thể tạo các trang lỗi tùy chỉnh như 400 Bad Request, 401 Authorization Request, 403 Forbidden Page, 404 File not Found và 500 Internal Error với tệp .htaccess. Tuy nhiên, những điều này sẽ làm chậm hiệu suất của máy chủ vì tất cả các kiểm tra này sẽ được thực hiện khi các trang được truy cập.

### Các loại MIME

Các tệp HTACCESS của Apache có thể được sửa đổi để bao gồm các loại Tiện ích mở rộng thư Internet đa năng (MIME). Điều này cho phép máy chủ của bạn hỗ trợ phân phối các tệp ứng dụng không được trang web hỗ trợ.

### SSI

Bao gồm phía máy chủ (SSI) hoạt động như một trình tiết kiệm thời gian tuyệt vời trên trang web. SSI có thể được kích hoạt bằng cách chèn mã hte sau vào tệp .htaccess của bạn.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Ví dụ về tệp HTACCESS của Apache

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Người giới thiệu

* [Hướng dẫn máy chủ HTTP Apache: tệp .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

