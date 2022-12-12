{
  "date" : "2019-10-11",
  "keywords" :[ "tpl","tệp tpl", "định dạng tệp tpl", "loại tệp tpl", "tệp", "loại", "tệp tpl là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL - Mẫu máy chủ tệp HTTP",
  "description" :"Tìm hiểu về Tệp TPL và các API để tạo và mở tệp TPL.",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Tệp TPL là gì?

Tệp có phần mở rộng .tpl là tệp mẫu được tạo và sử dụng bởi Máy chủ tệp HTTP (HFS), đây là chương trình ứng dụng chia sẻ tệp để gửi và nhận tệp qua công nghệ web HTTP thay vì giao thức FTP. Nó được sử dụng để xây dựng các trang [HTML](/vi/web/html/) động dựa trên thông tin mẫu được xác định để có các cài đặt có bố cục, kiểu dáng và tập lệnh tương tự. Các ứng dụng yêu cầu cùng cài đặt có thể được chỉ định cùng một tệp mẫu và HFS sẽ tự động trả về trang được yêu cầu trong thời gian chạy dựa trên tệp mẫu này.


## Định dạng tệp TPL

Các tệp TPL được lưu trữ ở định dạng con người có thể đọc được và chứa HTML là Ngôn ngữ đánh dấu con người có thể đọc được. Ngoài HTML, tệp TPL cũng có thể chứa CSS và Javascript cấp mẫu để xác định bố cục và hành động được thực hiện bởi tất cả các trang được tạo từ tệp mẫu này.

### Phần TPL

Các phần TPL chứa mã HTML, CSS hoặc JavaScript được HFS sử dụng trong khi tạo trang đầu ra. Mỗi phần bắt đầu bằng dấu ngoặc vuông ([]) và được xác định bằng dấu phần trăm (%). Một tệp TPL có thể có các phần sau.

#### Phần Phong cách TPL

Nó bao gồm thông tin liên quan đến kiểu dáng có thể sử dụng hoặc không sử dụng tham chiếu tệp CSS được nhúng. Một ví dụ về phần tạo kiểu như sau.

```
[style]
.row { color: #666 }
span.size_file { font-size:10px; color:#666 }
.button, .big, .little, th { font-weight:normal; font-size:9pt; color:#222; }
#back { background:#222;border:1px solid #000;padding:5px;margin-top:10px;}
.little { font-size: 8pt; color:#2F4F4F;margin-top:10px; }
.path_title { color: #999;margin-top:10px; }
img { border-style:none }
.row { background:#f8f8f8;}
.row a { text-decoration:none; }
.comment { font-size:7pt; color:#666; background:#f3f3f3; padding:3px; border:1px solid #ccc; margin-top:2px; }
.column { color:#222; font-size:13pt; font-weight:bold; padding-bottom:0; }
.flag { font-weight:bold; font-size:8pt; background:#fff; color:#990000; text-align:center; border:1px solid #ff0000; }
.text { color:#222; }
span.desc { color: #999; }
#everything { margin-top:20px;border-top:1px solid #ccc;padding-top:10px; }
html {
font-size: 62.5%;
}
body {margin:0px; padding:0px; background-color:#fff; color:#222; font-family:"Lucida Grande", "Tahoma", "Helvetica", "Arial", sans-serif; font-size:120%;quotes:"\201C" "\201E" "\2018" "\2019";}
table, tr, td {font-size: inherit;}
a:link {color: #222;}
a:visited {color: #666;}
a:hover {	color: #000;}
a:active {}
a:focus {}
img, a img {border: none;}
#path {color: #333;background-color: #f8f8f8; border-bottom: 1px solid #ccc;padding: 3px 8px;margin: 0px;}
#path li {display: inline;padding-left: 13px; padding-right: 3px; background-image: url(arrow.gif);background-repeat: no-repeat;background-position: 1px 5px;}
#path span {font-weight: bold;}
#header {margin: 24px 48px;}
#header h1 {font-size: 250%;color: #222;  margin: 0;margin-bottom: 6px;}
#header h2 {font-size: 120%;color: #aaa;  margin: 0;}
#content { margin: 24px 48px;}
#footer {    margin-top: 48px;    border-top: 1px solid #ccc;    padding: 6px;    text-align: center;    color: #888;    font-size: 80%;}
#footer a {color: #888;}
```

#### Phần liên kết TPL

Phần liên kết chứa thông tin về URL và có thể bao gồm tham chiếu đến các sự kiện như nút và hành động của nó.

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### Phần bình luận

Phần bình luận của TPL bao gồm để tạo bình luận và được định nghĩa như sau.
```
[comment]
<div class=comment>%item-comment%</div>
```

#### Phần Tải lên

Phần tải lên trả về phản hồi HTML thực tế từ máy chủ dựa trên cài đặt mẫu như trong ví dụ sau.

```
[upload]
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html><head>
<title>myHFS</title>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<style type="text/css">\n%style%\n</style>
</head>
<body>
<ul id=path>
<li><strong>Folder:</strong> <a href="/">root</a>%folder%</li>
</ul>
<div id=header>
<h1>myHFS</h1>
<h2>Final HFS Template Framework for Ishare USM Community</h2>
</div>
<div id=content>

<h3>myHFS Rules</h3>
<p>I'm sharing stuffs unpaid, so please respect me by understanding these rules: </p>
<ul class="contacts">
<li>Sorry if your downloading activity was suddenly interrupted/disconnected. It might be due to some technical problems.</li>
<li>Be nice. Don't use IDM or any download manager program with many connections. Set it to 1 or you will be banned from my server.</li>
<li>Anything I shared here is the right of my freedom. Good or bad, the decision is in your hands. I'm not be responsible for any consequences.</li>
</ul>
<p class=credit>Sharing among my university fellows is an unique culture here, in Engineering Campus, USM. Sharing via LAN by using HFS software is the best underground activity for everyone. Sharing is loving!</p>
</div>

</body></html>
```

## Người giới thiệu

* [HFS](https://www.rejetto.com/wiki/index.php/Refinements)
* [Ví dụ TPL - Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

