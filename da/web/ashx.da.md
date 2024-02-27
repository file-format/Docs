{
  "date": "2019-10-11",
  "keywords": [
"ashx",
"fil",
"udvidelse",
"filformat",
"ASHX",
"ASP.NET Web Handler-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASHX File Extension - En ASP.NET Web Handler-fil",
  "description": "Lær om, hvad en ASHX-fil og API'er er, der kan oprette og åbne ASHX-filer.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ash-dax"
}
},
  "lastmod": "2021-06-10"
}

## Hvad er en ASHX fil?

En ASHX-fil er en webside, der bruges af ASP.NET HTTP-handleren til at betjene brugeren med de sider, der henvises til i denne fil. ASP.NET HTTP-handleren behandler den indkommende anmodning, refererer til siderne fra .ashx-filen og sender den kompilerede side tilbage til brugerens browser. Behandlingsmetoden ligner for det meste ASPX-filer med den forskel, at i dette tilfælde behandles de refererede sider/dokumenter og sendes tilbage.

## ASHX filformat

.ashx-filerne gemmes i almindeligt tekstfilformat og indeholder referencer til andre sider eller dokumenter, der sendes tilbage til brugerens browser efter anmodning. Disse kan åbnes i enhver teksteditor og udvikler-IDE'er som Xamarin Studio, Microsoft Notepad, Notepad++ og mange flere. ASHX-filerne er nyttige, hvis du har:
 * Binære filer
 * Dynamiske billedvisninger
 * Præstationskritiske websider
 * XML-filer
 * Minimale websider

## Hvordan kompilerer man en ASHX-fil dynamisk?

Følgende trin kan bruges til at tilføje og kompilere en ASHX-fil ved hjælp af Microsoft Visual Studio.

 * tilføje en generisk handler - Handler1.ashx i visual studio
 * slet cs-filen, der blev oprettet automatisk.
 * åben ashx igen,
** fjern CodeBehind=Handler1.ashx.cs
** tilføje c# kode nedenfor

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
### ASHX Eksempel

Følgende ASHX-kode returnerer billedfilen til brugerens anmodning, når ASHX-filen kaldes i internetbrowseren.


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

## Referencer

 * [Kompiler ASHX-fil](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

