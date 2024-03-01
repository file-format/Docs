{
  "date": "2019-10-11",
  "keywords": [
"ashx",
"tiedosto",
"laajennus",
"tiedosto muoto",
"ASHX",
"ASP.NET Web Handler -tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASHX-tiedostopääte – ASP.NET-verkkokäsittelijätiedosto",
  "description": "Opi mikä on ASHX-tiedosto ja API:t, jotka voivat luoda ja avata ASHX-tiedostoja.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ash-fix"
}
},
  "lastmod": "2021-06-10"
}

## Mikä on ASHX-tiedosto?

ASHX-tiedosto on verkkosivu, jota ASP.NET HTTP-käsittelijä käyttää palvelemaan käyttäjää sivuilla, joihin tässä tiedostossa viitataan. ASP.NET HTTP Handler käsittelee saapuvan pyynnön, viittaa .ashx-tiedoston sivuihin ja lähettää käännetyn sivun takaisin käyttäjän selaimeen. Käsittelytapa on enimmäkseen samanlainen kuin ASPX-tiedostoilla, joiden ero on, että tässä tapauksessa viitatut sivut/asiakirjat käsitellään ja lähetetään takaisin.

## ASHX tiedostomuoto

.ashx-tiedostot tallennetaan vain tekstitiedostomuodossa ja sisältävät viittauksia muihin sivuihin tai asiakirjoihin, jotka lähetetään pyynnöstä takaisin käyttäjän selaimeen. Ne voidaan avata missä tahansa tekstieditorissa ja kehittäjän IDE:ssä, kuten Xamarin Studiossa, Microsoft Notepadissa, Notepad++:ssa ja monissa muissa. ASHX-tiedostot ovat hyödyllisiä, jos sinulla on:
 * Binaaritiedostot
 * Dynaamiset kuvanäkymät
 * Suorituskykykriittiset verkkosivut
 * XML-tiedostoja
 * Minimi nettisivut

## Kuinka kääntää ASHX-tiedosto dynaamisesti?

Seuraavien vaiheiden avulla voidaan lisätä ja kääntää ASHX-tiedosto Microsoft Visual Studion avulla.

 * lisää yleinen käsittelijä - Handler1.ashx Visual Studiossa
 * poista automaattisesti luotu cs-tiedosto.
 * avaa ashx uudelleen,
** poista CodeBehind=Handler1.ashx.cs
** lisää c#-koodi alle

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
### ASHX Esimerkki

Seuraava ASHX-koodi palauttaa kuvatiedoston käyttäjän pyynnöstä, kun ASHX-tiedostoa kutsutaan Internet-selaimessa.


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

## Viitteet

 * [Käännä ASHX-tiedosto](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

