{
  "date" : "2019-10-11",
  "keywords" :["ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX File Extension - ملف ASP.NET Web Handler" ,
  "description" :"تعرف على معلومات حول ملف ASHX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ASHX وفتحها." ,
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-06-10"
}

## ما هو ملف ASHX؟

ملف ASHX هو صفحة ويب يستخدمها ASP.NET HTTP Handler لخدمة المستخدم بالصفحات المشار إليها داخل هذا الملف. يعالج ASP.NET HTTP Handler الطلب الوارد ، ويشير إلى الصفحات من ملف .ashx ، ويرسل الصفحة المترجمة مرة أخرى إلى مستعرض المستخدم. تشبه طريقة المعالجة في الغالب طريقة معالجة ملفات ASPX مع اختلاف أنه في هذه الحالة ، تتم معالجة الصفحات / المستندات المرجعية وإرسالها مرة أخرى.

## تنسيق ملف ASHX

يتم حفظ ملفات .ashx بتنسيق ملف نص عادي وتحتوي على مراجع لصفحات أو مستندات أخرى يتم إرسالها مرة أخرى إلى متصفح المستخدم عند الطلب. يمكن فتحها في أي محرر نصوص و IDEs للمطورين مثل Xamarin Studio و Microsoft Notepad و Notepad ++ وغيرها الكثير. تكون ملفات ASHX مفيدة في حالة وجود:
* الملفات الثنائية
* طرق عرض الصور الديناميكية
* صفحات الويب ذات الأداء الحرج
* ملفات XML
* الحد الأدنى من صفحات الويب

## كيف يتم تجميع ملف ASHX ديناميكيًا؟

يمكن استخدام الخطوات التالية لإضافة ملف ASHX وترجمته باستخدام Microsoft Visual Studio.

* إضافة معالج عام - Handler1.ashx في الاستوديو المرئي
* حذف ملف CS الذي تم إنشاؤه تلقائيًا.
* افتح ashx مرة أخرى ،
** إزالة CodeBehind = "Handler1.ashx.cs"
** أضف كود C # أدناه

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
### مثال ASHX

يعيد رمز ASHX التالي ملف الصورة إلى طلب المستخدم عندما يتم استدعاء ملف ASHX في مستعرض الإنترنت.


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

## مراجع

* [ترجمة ملف ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


