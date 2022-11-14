{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "bestand", "extensie", "bestandsindeling", "ASHX", "ASP.NET Web Handler-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX-bestandsextensie - een ASP.NET-webhandlerbestand",
  "description" :"Meer informatie over wat een ASHX-bestand is en API's die ASHX-bestanden kunnen maken en openen.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Wat is een ASHX-bestand?

Een ASHX-bestand is een webpagina die door de ASP.NET HTTP Handler wordt gebruikt om de gebruiker te voorzien van de pagina's waarnaar in dit bestand wordt verwezen. De ASP.NET HTTP Handler verwerkt het binnenkomende verzoek, verwijst naar de pagina's uit het .ashx-bestand en stuurt de gecompileerde pagina terug naar de browser van de gebruiker. De verwerkingsmethode is grotendeels gelijk aan die van ASPX-bestanden met het verschil dat in dit geval de pagina's/documenten waarnaar wordt verwezen worden verwerkt en teruggestuurd.

## ASHX-bestandsindeling

De .ashx-bestanden worden opgeslagen in platte tekstbestandsindeling en bevatten verwijzingen naar andere pagina's of documenten die op verzoek worden teruggestuurd naar de browser van de gebruiker. Deze kunnen worden geopend in elke teksteditor en ontwikkelaars-IDE's zoals Xamarin Studio, Microsoft Notepad, Notepad++ en nog veel meer. De ASHX-bestanden zijn handig voor het geval u:
* Binaire bestanden
* Dynamische beeldweergaven
* Prestatiekritische webpagina's
* XML-bestanden
* Minimale webpagina's

## Hoe een ASHX-bestand dynamisch te compileren?

De volgende stappen kunnen worden gebruikt om een ASHX-bestand toe te voegen en te compileren met Microsoft Visual Studio.

* voeg een generieke handler toe - Handler1.ashx in visuele studio
* verwijder het cs-bestand dat automatisch is gemaakt.
* open ashx weer,
** verwijder CodeBehind="Handler1.ashx.cs"
** voeg hieronder c# code toe

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
### ASHX Voorbeeld

De volgende ASHX-code retourneert het afbeeldingsbestand op verzoek van de gebruiker wanneer het ASHX-bestand wordt aangeroepen in de internetbrowser.


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

## Referenties

* [ASHX-bestand compileren](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


