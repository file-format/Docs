{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX fájlkiterjesztés – ASP.NET webkezelő fájl",
  "description" :"További információ az ASHX-fájlokról és az API-król, amelyek ASHX-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Mi az ASHX fájl?

Az ASHX-fájl egy olyan weboldal, amelyet az ASP.NET HTTP-kezelő a fájlban hivatkozott oldalak kiszolgálására használ a felhasználónak. Az ASP.NET HTTP-kezelő feldolgozza a bejövő kérést, hivatkozik az .ashx fájl oldalaira, és visszaküldi a lefordított oldalt a felhasználó böngészőjének. A feldolgozás módja többnyire hasonló az ASPX fájlokéhoz, azzal a különbséggel, hogy ebben az esetben a hivatkozott oldalak/dokumentumok feldolgozásra és visszaküldésre kerülnek.

## ASHX fájlformátum

Az .ashx fájlok egyszerű szöveges fájlformátumban kerülnek mentésre, és hivatkozásokat tartalmaznak más oldalakra vagy dokumentumokra, amelyeket kérésre visszaküldenek a felhasználó böngészőjének. Ezek bármely szövegszerkesztőben és fejlesztői IDE-ben megnyithatók, mint például a Xamarin Studio, a Microsoft Notepad, a Notepad++ és még sok más. Az ASHX fájlok akkor hasznosak, ha:
* Bináris fájlok
* Dinamikus képnézet
* Teljesítménykritikus weboldalak
* XML fájlok
* Minimális weboldalak

## Hogyan lehet dinamikusan lefordítani egy ASHX fájlt?

A következő lépésekkel adhat hozzá és fordíthat ASHX-fájlt a Microsoft Visual Studio használatával.

* Adjon hozzá egy általános kezelőt - Handler1.ashx a Visual Studio-ban
* Törölje az automatikusan létrehozott cs fájlt.
* nyissa meg újra az ashx-t,
** távolítsa el a CodeBehind="Handler1.ashx.cs"
** Adjon hozzá c# kódot alább

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
### ASHX példa

A következő ASHX kód visszaküldi a képfájlt a felhasználó kérésére, amikor az ASHX fájlt meghívja az internetböngészőben.


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

## Hivatkozások

* [Az ASHX-fájl fordítása](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


