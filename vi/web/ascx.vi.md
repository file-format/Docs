{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","tệp ascx", "định dạng tệp ascx", "loại tệp ascx", "tệp", "loại", "tệp ascx là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp ASCX",
  "description" :"Tìm hiểu về tệp ASCX là gì và các API có thể tạo và mở tệp ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp ASCX là gì?

Tệp có phần mở rộng .ascx là điều khiển người dùng được sử dụng làm thành phần có thể tái sử dụng trong các trang web. Nó được tham chiếu trong bất kỳ trang web ASP nào bằng cách kéo nó từ hộp điều khiển vào trang. Kiểm soát người dùng ASCX được thêm vào dự án dưới dạng nguồn trung tâm, dẫn đến mọi thay đổi trong kiểm soát người dùng sẽ được phản ánh trên toàn bộ trang web. Không giống như các tệp ASMX xác định cơ chế giao tiếp trong 2 đối tượng qua internet, các tệp ASCX là các điều khiển của người dùng để nhúng vào các trang hoặc trang web.

## Định dạng tệp ASCX

Các tệp ASCX đang ghi ở định dạng văn bản thuần túy và có thể sử dụng mã đằng sau tính năng như các trang web kết thúc bằng .ascx.cs. Mã đánh dấu của điều khiển người dùng bắt đầu bằng chỉ thị @Control như trong ví dụ sau.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Điều khiển người dùng web này có thể được sử dụng lại trên nhiều trang như chân trang, đầu trang hoặc một số loại điều hướng trang web. Điều khiển người dùng web có các thuộc tính, phương thức và sự kiện giống như bất kỳ điều khiển nào khác khiến chúng trở nên hữu ích trong việc thiết lập hành vi trực quan của chúng.

### Ví dụ về Đăng ký điều khiển người dùng trong web.config

Để sử dụng một điều khiển người dùng trên nhiều trang, điều khiển web có thể được đăng ký trong web.config. Điều này cho phép sử dụng quyền kiểm soát trên toàn bộ trang web thay vì đăng ký trên từng trang riêng lẻ. Mã mẫu sau xác định cách đăng ký điều khiển web trong web.config để được hiển thị dưới dạng chân trang trên toàn bộ trang web.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Người giới thiệu

* [Kiểm soát người dùng ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

