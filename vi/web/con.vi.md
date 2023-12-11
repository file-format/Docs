{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp CON - Định dạng tệp nguồn ứng dụng khái niệm",
  "description" :"Tìm hiểu về tệp CON là gì và các API có thể tạo và mở tệp CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Tệp CON là gì?

Tệp CON là tệp mã nguồn dành cho ứng dụng được phát triển cho **Máy chủ ứng dụng khái niệm**. Nó được sử dụng để viết các ứng dụng trao đổi dữ liệu giữa máy chủ và người dùng. Các tệp CON được lưu trữ trên máy chủ có thể truy cập được bằng trình duyệt Web miễn là Máy khách Khái niệm được cài đặt ở phía người dùng. Khái niệm Máy chủ ứng dụng là một máy chủ web với ngôn ngữ lập trình quy mô nhỏ có thể có một công cụ cơ sở dữ liệu tập hợp con [SQL](/vi/database/sql/) (TinDB).

Các tệp CON có thể mở/chạy với Máy chủ Ứng dụng Khái niệm RadGs.

## Định dạng tệp CON - Thông tin thêm

Các tệp CON được lưu trữ trên máy chủ và được truy cập bằng trình duyệt web trên máy người dùng. Khái niệm [URL](/vi/web/url/) khác với các url HTTP thông thường và bắt đầu bằng **concept://**.

### Ví dụ URL tệp CON

Có thể truy cập tệp CON được lưu trữ trên Máy chủ ứng dụng khái niệm thông qua trình duyệt web bằng các URL như:

```
concept://domain.server.com/web_application/main.con.
```
## Người giới thiệu

* [Máy chủ ứng dụng khái niệm](https://github.com/Devronium/ConceptApplicationServer)

