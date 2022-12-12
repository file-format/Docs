{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "định dạng tệp", "loại tệp", "tệp .asa là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - Tệp cấu hình ASP",
  "description" :"Tìm hiểu về tệp ASA là gì và các API có thể tạo và mở tệp ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Tệp ASA là gì?

Tệp ASA là tệp cấu hình, được tạo cho các dự án [ASP](/vi/web/asp/)/ASP.NET. Nó chứa các khai báo về biến, chứa và các hàm có nghĩa là có thể truy cập được ở cấp độ Toàn cầu trong ứng dụng. Tất cả các trang trong dự án đều có thể truy cập các biến và hàm này, do đó tránh được yêu cầu viết lại chúng. Một ví dụ như vậy là trang Global.asa được lưu trữ trong thư mục gốc để các trang web ASP khác có thể truy cập được. Các tệp Global.asa là tùy chọn, nhưng nếu được sử dụng, mỗi ứng dụng chỉ có thể có một tệp Global.asa.

## Định dạng tệp ASA - Thông tin khác

Các tệp ASA là các tệp văn bản thuần túy có thông tin sau.

* Sự kiện ứng dụng
* Sự kiện phiên
* \<object> tuyên bố
* TypeLibrary khai báo
* chỉ thị #incoide

## Ví dụ về tệp ASA

Tệp Global.asa có thể trông giống như thế này.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Người giới thiệu

* [Tệp ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

