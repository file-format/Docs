{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "fil", "tillägg", "filformat", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX File Extension - En ASP.NET Web Handler File",
  "description" :"Läs mer om vad som är en ASHX-fil och API:er som kan skapa och öppna ASHX-filer.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Vad är en ASHX fil?

En ASHX-fil är en webbsida som används av ASP.NET HTTP-hanteraren för att betjäna användaren med sidorna som det refereras till i denna fil. ASP.NET HTTP-hanteraren bearbetar den inkommande begäran, refererar till sidorna från .ashx-filen och skickar tillbaka den kompilerade sidan till användarens webbläsare. Metoden för bearbetning liknar för det mesta den för ASPX-filer med skillnaden att i detta fall bearbetas de refererade sidorna/dokumenten och skickas tillbaka.

## ASHX filformat

.ashx-filerna sparas i vanlig textfilformat och innehåller referenser till andra sidor eller dokument som skickas tillbaka till användarens webbläsare på begäran. Dessa kan öppnas i vilken textredigerare och utvecklare som helst som Xamarin Studio, Microsoft Notepad, Notepad++ och många fler. ASHX-filerna är användbara om du har:
* Binära filer
* Dynamiska bildvyer
* Prestandakritiska webbsidor
* XML-filer
* Minimalt med webbsidor

## Hur man dynamiskt kompilerar en ASHX-fil?

Följande steg kan användas för att lägga till och kompilera en ASHX-fil med Microsoft Visual Studio.

* lägg till en generisk hanterare - Handler1.ashx i visual studio
* ta bort cs-filen som skapades automatiskt.
*öppna ashx igen,
** ta bort CodeBehind="Handler1.ashx.cs"
** lägg till c#-kod nedan

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
### ASHX Exempel

Följande ASHX-kod returnerar bildfilen till användarens begäran när ASHX-filen anropas i webbläsaren.


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

## Referenser

* [Kompilera ASHX-fil](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


