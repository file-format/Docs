{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "fișier", "extensie", "format fișier", "ASHX", "ASP.NET Web Handler File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX File Extension - An ASP.NET Web Handler File",
  "description" :"Aflați despre ce este un fișier ASHX și API-urile care pot crea și deschide fișiere ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Ce este un fișier ASHX?

Un fișier ASHX este o pagină web care este utilizată de ASP.NET HTTP Handler pentru a furniza utilizatorului paginile la care se face referire în acest fișier. Handler-ul HTTP ASP.NET procesează cererea primită, face referire la paginile din fișierul .ashx și trimite înapoi pagina compilată înapoi la browserul utilizatorului. Metoda de prelucrare este în mare parte similară cu cea a fișierelor ASPX, cu diferența că în acest caz, paginile/documentele la care se face referire sunt procesate și trimise înapoi.

## Format de fișier ASHX

Fișierele .ashx sunt salvate în format de fișier text simplu și conțin referințe la alte pagini sau documente care sunt trimise înapoi la browserul utilizatorului, la cerere. Acestea pot fi deschise în orice editor de text și IDE de dezvoltator, cum ar fi Xamarin Studio, Microsoft Notepad, Notepad++ și multe altele. Fișierele ASHX sunt utile în cazul în care aveți:
* Fișiere binare
* Vizualizări dinamice ale imaginii
* Pagini web critice pentru performanță
* Fișiere XML
* Pagini web minime

## Cum se compilează dinamic un fișier ASHX?

Următorii pași pot fi utilizați pentru a adăuga și a compila un fișier ASHX utilizând Microsoft Visual Studio.

* adăugați un handler generic - Handler1.ashx în studioul vizual
* ștergeți fișierul cs care a fost creat automat.
* deschide din nou ashx,
** eliminați CodeBehind="Handler1.ashx.cs"
** adăugați codul c# mai jos

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
### ASHX Exemplu

Următorul cod ASHX returnează fișierul imagine la cererea utilizatorului atunci când fișierul ASHX este apelat în browserul de internet.


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

## Referințe

* [Compilați fișierul ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


