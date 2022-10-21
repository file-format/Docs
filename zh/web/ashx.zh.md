{
  "date" : "2019-10-11",
  "keywords" :["ashx","文件","扩展名","文件格式","ASHX","ASP.NET Web 处理程序文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX 文件扩展 - 一个 ASP.NET Web 处理程序文件",
  "description" :"了解什么是 ASHX 文件以及可以创建和打开 ASHX 文件的 API。",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## 什么是一 .ASHX 文件？

ASHX 文件是 ASP.NET HTTP 处理程序用来为用户提供此文件中引用的页面的网页。 ASP.NET HTTP 处理程序处理传入的请求，引用 .ashx 文件中的页面，并将编译后的页面发送回用户的浏览器。处理方法与 ASPX 文件的处理方法大多相似，不同之处在于在这种情况下，引用的页面/文档被处理并发送回。

## ASHX 文件格式

.ashx 文件以纯文本文件格式保存，并包含对其他页面或文档的引用，这些页面或文档会根据请求发送回用户的浏览器。这些可以在任何文本编辑器和开发人员 IDE（例如 Xamarin Studio、Microsoft Notepad、Notepad++ 等）中打开。 ASHX 文件在您有以下情况时很有用：
* 二进制文件
*动态图像视图
* 性能关键网页
* XML 文件
*最小的网页

## 如何动态编译 ASHX 文件？

以下步骤可用于使用 Microsoft Visual Studio 添加和编译 ASHX 文件。

* 在 Visual Studio 中添加一个通用处理程序 - Handler1.ashx
* 删除自动创建的cs文件。
* 再次打开 ashx，
** 删除 CodeBehind="Handler1.ashx.cs"
** 在下面添加 c# 代码

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
### ASHX 示例

当在 Internet 浏览器中调用 ASHX 文件时，以下 ASHX 代码将图像文件返回给用户的请求。


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

## 参考

* [编译 ASHX 文件](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


