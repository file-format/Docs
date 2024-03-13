{
  "date": "2019-10-11",
  "keywords": [
"ashx",
"fayl",
"uzadılması",
"fayl formatı",
"ASHX",
"ASP.NET Veb İşləyici Faylı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASHX Fayl Genişlənməsi - ASP.NET Veb İşləyici Faylı",
  "description": "ASHX faylı və ASHX fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ash-azx"
}
},
  "lastmod": "2021-06-10"
}

## ASHX faylı nədir?

ASHX faylı ASP.NET HTTP İşləyicisi tərəfindən istifadəçiyə bu faylın içərisində istinad edilən səhifələrlə xidmət göstərmək üçün istifadə edilən veb səhifədir. ASP.NET HTTP İşləyicisi daxil olan sorğunu emal edir, .ashx faylındakı səhifələrə istinad edir və tərtib edilmiş səhifəni istifadəçinin brauzerinə geri göndərir. Emal üsulu əsasən ASPX fayllarına bənzəyir ki, bu halda istinad edilən səhifələr/sənədlər işlənir və geri göndərilir.

## ASHX fayl formatı

.ashx faylları sadə mətn faylı formatında saxlanılır və sorğu əsasında istifadəçinin brauzerinə göndərilən digər səhifələrə və ya sənədlərə istinadlar ehtiva edir. Bunlar Xamarin Studio, Microsoft Notepad, Notepad++ və daha çox kimi istənilən mətn redaktoru və tərtibatçı İDE-lərində açıla bilər. ASHX faylları aşağıdakı hallarda faydalıdır:
 * Binar fayllar
 * Dinamik görüntü görünüşləri
 * Performans baxımından kritik veb səhifələr
 * XML faylları
 * Minimal veb səhifələr

## ASHX faylını dinamik şəkildə necə tərtib etmək olar?

Microsoft Visual Studio proqramından istifadə edərək ASHX faylını əlavə etmək və tərtib etmək üçün aşağıdakı addımlardan istifadə edilə bilər.

 * Ümumi işləyici əlavə edin - vizual studiyada Handler1.ashx
 * avtomatik yaradılmış cs faylını silin.
 * ashx-i yenidən açın,
** CodeBehind=Handler1.ashx.cs-ni silin
** aşağıya c# kodu əlavə edin

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
### ASHX nümunəsi

Aşağıdakı ASHX kodu internet brauzerində ASHX faylı çağırıldıqda istifadəçinin tələbinə şəkil faylını qaytarır.


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

## İstinadlar

 * [ASHX Faylını Tərtib edin](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

