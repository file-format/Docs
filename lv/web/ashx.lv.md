{
  "date": "2019-10-11",
  "keywords": [
"ashx",
"failu",
"pagarinājumu",
"faila formātā",
"ASHX",
"ASP.NET tīmekļa apdarinātāja fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASHX faila paplašinājums — ASP.NET tīmekļa apdarinātāja fails",
  "description": "Uzziniet, kas ir ASHX fails un API, kas var izveidot un atvērt ASHX failus.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ash-lvx"
}
},
  "lastmod": "2021-06-10"
}

## Kas ir ASHX fails?

ASHX fails ir tīmekļa lapa, ko izmanto ASP.NET HTTP apdarinātājs, lai apkalpotu lietotāju ar lapām, uz kurām ir atsauces šajā failā. ASP.NET HTTP apdarinātājs apstrādā ienākošo pieprasījumu, atsaucas uz lapām no faila .ashx un nosūta apkopoto lapu atpakaļ uz lietotāja pārlūkprogrammu. Apstrādes metode lielākoties ir līdzīga ASPX failu metodei ar atšķirību, ka šajā gadījumā atsauces lapas/dokumenti tiek apstrādāti un nosūtīti atpakaļ.

## ASHX faila formāts

.ashx faili tiek saglabāti vienkārša teksta faila formātā un satur atsauces uz citām lapām vai dokumentiem, kas pēc pieprasījuma tiek nosūtīti atpakaļ uz lietotāja pārlūkprogrammu. Tos var atvērt jebkurā teksta redaktorā un izstrādātāju IDE, piemēram, Xamarin Studio, Microsoft Notepad, Notepad++ un daudzās citās. ASHX faili ir noderīgi, ja jums ir:
 * Binārie faili
 * Dinamiskie attēlu skati
 * Veiktspējai svarīgas tīmekļa lapas
 * XML faili
 * Minimālas tīmekļa lapas

## Kā dinamiski apkopot ASHX failu?

Tālāk norādītās darbības var izmantot, lai pievienotu un apkopotu ASHX failu, izmantojot Microsoft Visual Studio.

 * pievienojiet vispārīgo apdarinātāju — Handler1.ashx programmā Visual Studio
 * izdzēsiet automātiski izveidoto cs failu.
 * vēlreiz atver ashx,
** noņemt CodeBehind=Handler1.ashx.cs
** zemāk pievienojiet c# kodu

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
### ASHX piemērs

Šis ASHX kods atgriež attēla failu pēc lietotāja pieprasījuma, kad ASHX fails tiek izsaukts interneta pārlūkprogrammā.


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

## Atsauces

 * [Kompilēt ASHX failu](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

