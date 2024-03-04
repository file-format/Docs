{
  "date": "2019-10-11",
  "keywords": [
"ashx",
"failą",
"pratęsimas",
"Dokumento formatas",
"ASHX",
"ASP.NET žiniatinklio tvarkyklės failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASHX failo plėtinys – ASP.NET žiniatinklio tvarkyklės failas",
  "description": "Sužinokite, kas yra ASHX failas ir API, kurios gali kurti ir atidaryti ASHX failus.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ash-ltx"
}
},
  "lastmod": "2021-06-10"
}

## Kas yra ASHX failas?

ASHX failas yra tinklalapis, kurį naudoja ASP.NET HTTP tvarkytoja, kad aptarnautų vartotoją su puslapiais, kurie nurodyti šiame faile. ASP.NET HTTP tvarkytojas apdoroja gaunamą užklausą, nurodo puslapius iš .ashx failo ir siunčia sukompiliuotą puslapį atgal į vartotojo naršyklę. Apdorojimo metodas dažniausiai yra panašus į ASPX failų, kurių skirtumas yra tas, kad šiuo atveju nurodyti puslapiai / dokumentai yra apdorojami ir siunčiami atgal.

## ASHX failo formatas

.ashx failai išsaugomi paprasto teksto failo formatu ir juose yra nuorodų į kitus puslapius arba dokumentus, kurie vartotojo prašymu siunčiami atgal į naršyklę. Juos galima atidaryti bet kuriame teksto rengyklėje ir kūrėjo IDE, pvz., Xamarin Studio, Microsoft Notepad, Notepad++ ir daugelyje kitų. ASHX failai yra naudingi, jei turite:
 * Dvejetainiai failai
 * Dinaminiai vaizdo rodiniai
 * Našumui svarbūs tinklalapiai
 * XML failai
 * Minimalūs tinklalapiai

## Kaip dinamiškai kompiliuoti ASHX failą?

Norėdami pridėti ir kompiliuoti ASHX failą naudodami Microsoft Visual Studio, galite atlikti šiuos veiksmus.

 * pridėti bendrąjį tvarkyklę - Handler1.ashx Visual Studio
 * ištrinti cs failą, kuris buvo sukurtas automatiškai.
 * vėl atidaryk ashx,
** pašalinti CodeBehind=Handler1.ashx.cs
** žemiau pridėkite c# kodą

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
### ASHX pavyzdys

Šis ASHX kodas grąžina vaizdo failą pagal vartotojo užklausą, kai ASHX failas iškviečiamas interneto naršyklėje.


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

## Nuorodos

 * [Sudaryti ASHX failą](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

