{
  "date" : "2019-10-11",
  "keywords" :[ "htm","tệp htm", "định dạng tệp htm", "loại tệp htm", "tệp", "loại", "tệp htm là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp HTM",
  "description" :"Hướng dẫn định dạng tệp của bạn để tìm hiểu tệp HTM là gì và các API có thể tạo và mở chúng.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp HTM là gì?

Các tệp có phần mở rộng **.htm** đại diện cho Ngôn ngữ đánh dấu siêu văn bản để tạo các trang web để hiển thị trong các trình duyệt web như Google Chrome, Internet Explorer, Firefox và một số trình duyệt khác. Nó xác định các đánh dấu để tạo các trang tĩnh được xuất bản trên World Wide Web (WWW) để người khác truy cập. Các đánh dấu này cho trình duyệt biết cách hiển thị nội dung của trang web. Các trang như vậy có thể chứa văn bản thuần túy, hình ảnh, siêu liên kết đến các trang khác, video và thông tin phương tiện khác. Khi một trang web được xuất bản, bạn có thể xem mã đánh dấu đằng sau nó bằng cách xem nguồn trang của nó. Các trình duyệt hiện đại cho phép kiểm tra từng phần của trang web nơi từng phần tử phân chia hoặc đánh dấu trong nguồn HTM được xây dựng.

## Tóm tắt lịch sử của HTM

Kể từ khi thành lập và đóng vai trò đầu tiên, các đặc tả HTML đã được duy trì bởi World Wide Web Consortium (W3C) từ năm 1996. Năm 2000, nó cũng trở thành tiêu chuẩn quốc tế (ISO/IEC 15445:2000). Năm 1999, HTML 4.01 được xuất bản. Năm 2004, Nhóm làm việc về Công nghệ Ứng dụng Siêu văn bản Web (WHATWG) bắt đầu làm việc trên phiên bản HTML5, phiên bản này đã trở thành bản phân phối chung với W3C vào năm 2008. Phiên bản này đã được hoàn thành và chuẩn hóa vào ngày 28 tháng 10 năm 2014.

## Định dạng tệp HTML

Một tài liệu HTML 4 bao gồm ba phần:

1. dòng chứa thông tin phiên bản HTML
1. phần tiêu đề khai báo
1. phần thân chứa nội dung thực của tài liệu. Phần thân có thể được triển khai bởi phần tử BODY hoặc phần tử FRAMESET để chứa phần thân trong các khung

Mỗi phần có thể được dẫn đầu hoặc theo sau bởi khoảng trắng, dòng mới, tab và nhận xét. Một ví dụ về một tài liệu HTML đơn giản như hình dưới đây:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Thông tin phiên bản

Dòng mã đầu tiên,<!DOCTYPE html> , được gọi là khai báo loại tài liệu và cho trình duyệt biết trang được viết bằng phiên bản HTML nào. Tùy thuộc vào phiên bản HTML, có một số khai báo loại tài liệu khác nhau đặt tên cho định nghĩa loại tài liệu (DTD) được sử dụng cho tài liệu. Mỗi DTD khác nhau ở các yếu tố mà nó hỗ trợ và khác nhau như sau:

* HTML 4.01 Strict - bao gồm tất cả các thành phần và thuộc tính chưa [không dùng nữa](https://www.w3.org/TR/html401/conform.html#deprecated) hoặc không xuất hiện trong tài liệu bộ khung
* HTML 4.01 Chuyển tiếp - bao gồm mọi thứ trong DTD nghiêm ngặt cộng với các thành phần và thuộc tính không dùng nữa (hầu hết liên quan đến trình bày trực quan
* Bộ khung HTML 4.01 - bao gồm mọi thứ trong DTD chuyển tiếp cùng với các khung

Đối với **HTML5**, thông tin phiên bản đơn giản như được đề cập bên dưới.

```
<!DOCTYPE html>
```

### Thông tin tiêu đề

Tiêu đề của tài liệu HTML có thể bao gồm một số thành phần HTML không được trình duyệt hiển thị. Các phần tử như vậy là siêu dữ liệu mô tả thông tin về trang hoặc bao gồm các phần được sử dụng để tìm nạp thông tin từ các tài nguyên bên ngoài như biểu định kiểu CSS hoặc tệp JavaScript. Tiêu đề của một trang được đại diện bởi \<head> thẻ và kết thúc bằng \</head> nhãn.

<html>Để đặt tiêu đề trang, \<title> là phần tử duy nhất được yêu cầu trong các thẻ \<head>. Điều tương tự cũng được các công cụ Tìm kiếm sử dụng để xác định tiêu đề của một trang. </html>

### Thông tin cơ thể

Đây là phần chính trong tệp chứa tất cả nội dung của tệp được trình duyệt hiển thị. Nội dung Html có thể chứa các đánh dấu có thể tham chiếu đến các khối xây dựng khác nhau dưới dạng thẻ. Nó có thể chứa một số loại thông tin khác nhau như văn bản, hình ảnh, màu sắc, đồ họa, v.v. Ngoài ra, các phần tử âm thanh và video cũng có thể được nhúng vào phần thân html để trình duyệt hiển thị. Với sự hiện diện của ứng dụng biểu định kiểu hiện đại để thể hiện trực quan, các thuộc tính trình bày của BODY chẳng hạn như màu nền, màu liên kết, màu văn bản, v.v. đã không được dùng nữa. Do đó, các hiệu ứng tương tự có thể đạt được bằng cách sử dụng biểu định kiểu như bên dưới:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Biểu định kiểu nội tuyến rất dễ nhúng và để áp dụng nhanh cho hiệu ứng hình ảnh, biểu định kiểu bên ngoài giúp thuận tiện hơn khi triển khai một lần và truy cập ở nhiều nơi.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Phần tử HTML

Như đã đề cập trước đó, nội dung bên trong Nội dung HTML được biểu thị bằng thẻ, còn được gọi là Phần tử Html. Mỗi thẻ có thể có thông tin bổ sung dưới dạng các thuộc tính được viết dưới dạng
```
<tag attribute1#"value1" attribute2#"value2">
```
mặc dù không nhất thiết phải có các thuộc tính với mọi thẻ. Nếu các thuộc tính không được đề cập, các giá trị mặc định sẽ được sử dụng trong từng trường hợp. Sau đây là một số ví dụ về Phần tử:

#### Tiêu đề

```
<head>
  <title>The Title</title>
</head>
```

#### Tiêu đề

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Đoạn văn

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Người giới thiệu

* [Cấu trúc toàn cục của tài liệu HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

