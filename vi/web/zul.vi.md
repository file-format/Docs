{
  "date" : "2021-05-24",
  "keywords" :["zul", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "mở"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - Tệp giao diện người dùng ZK",
  "description":"Tìm hiểu về định dạng tệp ZUL và API có thể tạo và mở tệp ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Tệp ZUL là gì?

Tệp có phần mở rộng .zul là tệp web được tạo bằng Ngôn ngữ đánh dấu giao diện người dùng (ZUML) và chứa các định nghĩa cho các phần tử giao diện người dùng. Các lớp Ajax và Java hỗ trợ sử dụng ZUML dựa trên [XML](/vi/web/xml/) để phát triển các tệp phía máy chủ. Định dạng tệp ZUL được phát triển bởi ZK, một khung giao diện người dùng cho phép bạn xây dựng các ứng dụng web và di động mà không cần biết về JavaScript hoặc AJAX.

## Định dạng tệp ZUL

Các tệp ZUL dựa trên XML, bao gồm các thành phần khác nhau để xây dựng giao diện người dùng. Trình tải ZK sử dụng từng phần tử XML để tạo một thành phần. Quá trình xử lý tổng thể các thành phần trang như tiêu đề trang, mô tả, v.v. được mô tả bởi từng hướng dẫn xử lý XML của ZUML.

### Ví dụ ZUL

Trong ví dụ sau về mã ZUML, dòng đầu tiên chỉ định tiêu đề trang, dòng thứ hai tạo thành phần gốc có tiêu đề và đường viền và dòng thứ ba tạo nút có nhãn và trình xử lý sự kiện.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Có thể tải xuống lược đồ ZUL từ http://www.zkoss.org/2005/zul/zul.xsd.
## Người giới thiệu

* [ZUL - Bởi ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Lược đồ ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

