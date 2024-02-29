{
  "date": "2019-10-11",
  "keywords": [
"ashx",
"فایل",
"افزونه",
"فرمت فایل",
"ASHX",
"فایل ASP.NET Web Handler"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "پسوند فایل ASHX - یک فایل مدیریت وب ASP.NET",
  "description": "درباره فایل ASHX و API هایی که می توانند فایل های ASHX را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ash-fax"
}
},
  "lastmod": "2021-06-10"
}

## فایل ASHX چیست؟

یک فایل ASHX یک صفحه وب است که توسط ASP.NET HTTP Handler برای ارائه خدمات به کاربر با صفحاتی که در داخل این فایل به آنها ارجاع داده شده است استفاده می شود. ASP.NET HTTP Handler درخواست دریافتی را پردازش می کند، به صفحات فایل ashx. ارجاع می دهد و صفحه کامپایل شده را به مرورگر کاربر باز می فرستد. روش پردازش اکثراً مشابه فایل‌های ASPX است با این تفاوت که در این حالت، صفحات/اسناد ارجاع‌شده پردازش و پس داده می‌شوند.

## فرمت فایل ASHX

فایل‌های .ashx در قالب فایل متنی ساده ذخیره می‌شوند و حاوی ارجاعاتی به صفحات یا اسناد دیگر هستند که در صورت درخواست به مرورگر کاربر ارسال می‌شوند. اینها را می توان در هر ویرایشگر متن و IDEهای توسعه دهنده مانند Xamarin Studio، Microsoft Notepad، Notepad++ و بسیاری موارد دیگر باز کرد. فایل های ASHX در موارد زیر مفید هستند:
 * فایل های باینری
 * نماهای تصویر پویا
 * صفحات وب حیاتی برای عملکرد
 * فایل های XML
 * حداقل صفحات وب

## چگونه یک فایل ASHX را به صورت پویا کامپایل کنیم؟

مراحل زیر را می توان برای افزودن و کامپایل یک فایل ASHX با استفاده از Microsoft Visual Studio استفاده کرد.

 * یک کنترل کننده عمومی اضافه کنید - Handler1.ashx در ویژوال استودیو
 * فایل cs که به صورت خودکار ایجاد شده را حذف کنید.
 * دوباره ashx را باز کنید،
** حذف CodeBehind=Handler1.ashx.cs
** کد c# را در زیر اضافه کنید

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

زمانی که فایل ASHX در مرورگر اینترنت فراخوانی می شود، کد ASHX زیر فایل تصویر را به درخواست کاربر برمی گرداند.


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

## منابع

 * [کامپایل فایل ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

