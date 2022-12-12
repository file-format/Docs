{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Phần mở rộng tệp ASHX - Tệp xử lý web ASP.NET",
  "description" :"Tìm hiểu về tệp ASHX là gì và các API có thể tạo và mở tệp ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Tệp ASHX là gì?

Tệp ASHX là một trang web được Trình xử lý HTTP ASP.NET sử dụng để cung cấp cho người dùng các trang được tham chiếu bên trong tệp này. Trình xử lý HTTP ASP.NET xử lý yêu cầu đến, tham chiếu các trang từ tệp .ashx và gửi lại trang đã biên dịch trở lại trình duyệt của người dùng. Phương pháp xử lý hầu hết tương tự như phương pháp xử lý tệp ASPX với điểm khác biệt là trong trường hợp này, các trang/tài liệu được tham chiếu được xử lý và gửi lại.

## Định dạng tệp ASX

Các tệp .ashx được lưu ở định dạng tệp văn bản thuần túy và chứa các tham chiếu đến các trang hoặc tài liệu khác được gửi lại cho trình duyệt của người dùng theo yêu cầu. Chúng có thể được mở trong bất kỳ trình soạn thảo văn bản và IDE dành cho nhà phát triển nào, chẳng hạn như Xamarin Studio, Microsoft Notepad, Notepad ++, v.v. Các tệp ASHX rất hữu ích trong trường hợp bạn có:
* Tệp nhị phân
* Chế độ xem hình ảnh động
* Các trang web quan trọng về hiệu suất
* Tệp XML
* Các trang web tối thiểu

## Làm cách nào để tự động biên dịch tệp ASHX?

Có thể sử dụng các bước sau để thêm và biên dịch tệp ASHX bằng Microsoft Visual Studio.

* thêm trình xử lý Chung - Handler1.ashx trong studio trực quan
* xóa tệp cs được tạo tự động.
* mở lại ashx,
** xóa CodeBehind="Handler1.ashx.cs"
** thêm mã c # bên dưới

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
}

    public bool IsReusable
    {
        get
        {
            return false;
    }
}
}
```
### Ví dụ về ASHX

Mã ASHX sau trả về tệp hình ảnh theo yêu cầu của người dùng khi tệp ASHX được gọi trong trình duyệt internet.


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  


using System;  

using System.Web;  


public class QueryStringHandler : IHttpHandler   

{  

    public void ProcessRequest (HttpContext context)   

    {  

        HttpResponse r = context.Response;  

        r.ContentType = "image/png";  

        string file = context.Request.QueryString["file"];  

        if (file == "Arrow")  

        {  

            r.WriteFile("Arrow.gif");  

        }  

        else  

        {  

            r.WriteFile("Image.gif");  

        }  

    }  


    public bool IsReusable   

    {  

        get  

        {  

            return false;  

        }  

    }  

}  

```

## Người giới thiệu

* [Biên dịch tệp ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


