{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","tệp dhtml", "định dạng tệp dhtml", "loại tệp dhtml", "tệp", "loại", "tệp dhtml là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Định dạng tệp HTML động",
  "description":"Tìm hiểu về định dạng tệp DHTML và các API có thể tạo và mở tệp DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp DHTML là gì?

Tệp có phần mở rộng .dhtml là tệp [HTML](/vi/web/html/) động được sử dụng để tạo nội dung động của trang web. Phần tử web được tạo bằng DHTML được điều khiển theo sự kiện và không yêu cầu tải lại trang. Trong hầu hết các trường hợp, tệp DHTML được sử dụng để tạo nội dung động của trang web, chẳng hạn như menu thả xuống, lớp nổi, nút cuộn qua và nội dung động khác. Bạn bắt gặp các phần tử html động gần như hàng ngày trong cuộc sống của mình khi bạn di chuột vào một mục menu và nó sẽ mở ra các tùy chọn menu phụ khác. DHTML sử dụng các công nghệ web như [HTML](/vi/web/html/), [Javascript](/vi/web/js/), HTML DOM, Sự kiện HTML và [CSS](/vi/web/css/) để đạt được hiệu suất động hành vi của các phần tử.

## Định dạng tệp DHTML

Các tệp DHTML là các tệp văn bản thuần có chứa mã DHTML để triển khai hành vi động của các phần tử web.


### DHTML DOM

Mô hình đối tượng Tài liệu DHTML (DOM) dựa trên DOM HTML là cấu trúc cây với các thành phần, thuộc tính và văn bản như trong hình ảnh sau đây.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Nút `Tài liệu` có thể được sử dụng để gọi một số hàm nhằm triển khai các chức năng khác nhau. Ví dụ sau đây chỉ sử dụng phương thức document.write() của JavaScript trong DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Mã này viết văn bản "Xin chào thế giới" để xuất ra trình duyệt.

### Sự kiện DHTML

|S.No.|Sự kiện|Xảy ra|
---|---|---|
|1|onabort|Xảy ra khi người dùng hủy tải trang hoặc tệp phương tiện.|
|2|onblur|Xảy ra khi người dùng rời khỏi một đối tượng HTML.|
|3|onchange|Xảy ra khi người dùng thay đổi hoặc cập nhật giá trị của một đối tượng.|
|4|onclick|Xảy ra hoặc kích hoạt khi bất kỳ người dùng nào nhấp vào phần tử HTML.|
|5|ondblclick|Xảy ra khi người dùng nhấp vào một thành phần HTML hai lần cùng lúc.|
|6|onfocus|Xảy ra khi người dùng tập trung vào một phần tử HTML. Trình xử lý sự kiện này hoạt động ngược lại với onblur.|
|7|onkeydown|Nó kích hoạt khi người dùng đang nhấn một phím trên thiết bị bàn phím. Trình xử lý sự kiện này hoạt động với tất cả các khóa.|
|8|onkeypress|Nó kích hoạt khi người dùng nhấn một phím trên bàn phím. Trình xử lý sự kiện này không được kích hoạt cho tất cả các khóa.|
|9|onkeyup|Xảy ra khi người dùng nhả phím khỏi bàn phím sau khi nhấn vào một đối tượng hoặc thành phần.|
|10|onload|Xảy ra khi một đối tượng được tải hoàn toàn.|
|11|onmousedown|Xảy ra khi người dùng nhấn nút chuột trên phần tử HTML.|
|12|onmousemove|Xảy ra khi người dùng di chuyển con trỏ trên một đối tượng HTML.|
|13|onmouseover|Xảy ra khi người dùng di chuyển con trỏ qua một đối tượng HTML.|
|14|onmouseout|Xảy ra hoặc kích hoạt khi con trỏ chuột được di chuyển ra khỏi phần tử HTML.|
|15|onmouseup|Xảy ra hoặc kích hoạt khi thả nút chuột trên một phần tử HTML.|
|16|onreset|Nó được người dùng sử dụng để đặt lại biểu mẫu.|
|17|onselect|Xảy ra sau khi chọn nội dung hoặc văn bản trên trang web.|
|18|onsubmit|Nó được kích hoạt khi người dùng nhấp vào nút sau khi gửi biểu mẫu.|
|19|onunload|Nó được kích hoạt khi người dùng đóng một trang web.|

## Người giới thiệu

* [HTML động - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

