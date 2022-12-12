{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp HAML - Tệp mã nguồn Haml",
  "description":"Tìm hiểu về định dạng tệp HAML và các API có thể tạo và mở tệp HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Tệp HAML là gì?

Tệp HAML là tệp ngôn ngữ đánh dấu trừu tượng hóa HTML chứa mã nguồn được viết bằng ngôn ngữ [Haml](https://haml.info/). Nó có thể được sử dụng để thay thế cho ERB (Tập lệnh mẫu Ruby). Tệp HAML chứa mã nguồn mẫu để tạo HTML của tài liệu web. Có thể thay thế các tệp ERB bằng cách thay thế các tệp này trong thư mục ứng dụng/lượt xem thành Haml bằng cách thay đổi phần mở rộng của tệp. Các tệp HAML có thể được mở bằng bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Microsoft Notepad, Notepad ++, Apple TextEdit,

## Định dạng tệp HAML

Các tệp HAML là các tệp nguồn được lưu vào đĩa dưới dạng tệp văn bản thuần túy. Nó chứa mã được viết theo cú pháp HAML. HAML thay thế các thẻ *<>** bằng dấu **%** để làm cho mã đơn giản và dễ dàng hơn. Các tệp ERB có thể thay thế bằng HAML như trong ví dụ đơn giản sau.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Ví dụ về HAML

Sau đây là ví dụ Hello World của HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
kết xuất thành đầu ra HTML sau đây.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Người giới thiệu

* [HAML - Github](https://github.com/haml/haml)

