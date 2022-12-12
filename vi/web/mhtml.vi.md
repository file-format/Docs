{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","tệp mhtml", "định dạng tệp mhtml", "loại tệp mhtml", "tệp", "loại", "tệp mhtml là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - Tệp HTML MIME",
  "description":"Tìm hiểu về định dạng tệp MHTML và các API có thể tạo và mở tệp MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp MHTML là gì?

Các tệp có phần mở rộng MHTML đại diện cho định dạng lưu trữ trang web có thể được tạo bởi một số ứng dụng khác nhau. Định dạng này được gọi là định dạng lưu trữ vì nó lưu mã web **[HTML](/vi/web/html/)** và các tài nguyên liên quan trong một tệp duy nhất. Những tài nguyên này bao gồm mọi thứ được liên kết với trang web, chẳng hạn như hình ảnh, applet, hoạt ảnh, tệp âm thanh, v.v. Các tệp MHTML có thể được mở trong nhiều ứng dụng như Internet Explorer và Microsoft Word. Microsoft Windows sử dụng định dạng tệp MHTML để ghi lại các kịch bản sự cố được quan sát thấy trong quá trình sử dụng bất kỳ ứng dụng nào trên Windows phát sinh sự cố. Định dạng tệp MHTML mã hóa nội dung trang tương tự như thông số kỹ thuật được xác định trong message/rfc822 là thông số kỹ thuật liên quan đến email văn bản thuần túy. Thông số kỹ thuật thực tế của định dạng được nêu chi tiết trong [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Định dạng tệp MHTML

MHTML còn được gọi là Đóng gói MIME của các tài liệu HTML tổng hợp vì khả năng mã hóa các trang web HTML cùng với các tài nguyên của nó vào một kho lưu trữ web duy nhất. Theo thông số kỹ thuật RFC 2557, một tài liệu tổng hợp là một thông báo được mã hóa MIME có chứa tài nguyên gốc (đối tượng) cũng như các tài nguyên khác được liên kết với nó thông qua URI. Các tài nguyên khác như vậy có thể là đại diện của ảnh nội tuyến, biểu định kiểu, applet, v.v. Ngoài ra, chúng có thể là gốc của các tài liệu đa phương tiện khác. Thông số tài liệu đầy đủ cho định dạng tệp MHTML được trình bày chi tiết trong [RFC 2557](https://tools.ietf.org/html/rfc2557) và nên được tham chiếu cho bất kỳ loại phát triển ứng dụng nào để đọc/ghi định dạng tệp này. Tiêu chuẩn chỉ định rằng các bộ phận cơ thể được tham chiếu có thể được xác định bằng ID nội dung hoặc Vị trí nội dung.

### Tiêu đề nội dung MIME

Một tiêu đề nội dung MIME, Content-Location, được xác định để giải quyết các tham chiếu URI tới các tài nguyên trong các phần nội dung khác. Tiêu đề này có thể xuất hiện trong bất kỳ tiêu đề thư hoặc nội dung nào.

### Tiêu đề Nội dung-Vị trí

Vị trí nội dung là một đại diện của URI gắn nhãn nội dung của phần cơ thể nơi nó được đặt. Giá trị của nó có thể là một URI tuyệt đối hoặc tương đối. Nó có thể được sử dụng để gắn nhãn cho một tài nguyên mà một số hoặc tất cả những người nhận thư không thể truy xuất được. Một tin nhắn chỉ được phép có một tiêu đề Vị trí nội dung duy nhất. Ví dụ về cấu trúc nhiều phần/có liên quan chứa các phần cơ thể có cả nhãn Vị trí nội dung và ID nội dung:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI của Tập hợp MHTML

URI của tổng hợp MHTML khác với URI gốc của nó. Trường tiêu đề Nội dung-Vị trí sẽ áp dụng cho toàn bộ tổng hợp nếu nó được sử dụng trong tiêu đề của tiêu đề nhiều phần/liên quan. Tương tự, tập hợp tài nguyên được truy xuất có thể khác với tập hợp tài nguyên được truy xuất bằng cách sử dụng Vị trí-Nội dung của các phần của nó khi URI tham chiếu đến tập hợp MHTML được sử dụng để truy xuất tập hợp này. Ví dụ: việc truy xuất một tập hợp MHTML có thể trả về một phiên bản cũ, trong khi truy xuất URI gốc và các đối tượng được liên kết trong dòng của nó có thể trả về một phiên bản mới hơn.

## Người giới thiệu

* [MIME Encapsulation of Aggregate Documents - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Định dạng tệp MHTML - Theo Wikipedia](https://en.wikipedia.org/wiki/MHTML)

