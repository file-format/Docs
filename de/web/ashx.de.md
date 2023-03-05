{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX-Dateierweiterung - Eine ASP.NET-Web-Handler-Datei",
  "description" :"Erfahren Sie, was eine ASHX-Datei und APIs sind, die ASHX-Dateien erstellen und öffnen können.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Was ist eine ASHX-Datei?

Eine ASHX-Datei ist eine Webseite, die vom ASP.NET-HTTP-Handler verwendet wird, um dem Benutzer die Seiten bereitzustellen, auf die in dieser Datei verwiesen wird. Der ASP.NET-HTTP-Handler verarbeitet die eingehende Anforderung, verweist auf die Seiten aus der ASHX-Datei und sendet die kompilierte Seite zurück an den Browser des Benutzers. Die Art der Verarbeitung ähnelt weitgehend der von ASPX-Dateien mit dem Unterschied, dass hier die referenzierten Seiten/Dokumente verarbeitet und zurückgesendet werden.

## ASHX-Dateiformat

Die .ashx-Dateien werden im Nur-Text-Dateiformat gespeichert und enthalten Verweise auf andere Seiten oder Dokumente, die auf Anfrage an den Browser des Benutzers zurückgesendet werden. Diese können in jedem Texteditor und Entwickler-IDEs wie Xamarin Studio, Microsoft Notepad, Notepad++ und vielen mehr geöffnet werden. Die ASHX-Dateien sind nützlich, wenn Sie Folgendes haben:
* Binäre Dateien
* Dynamische Bildansichten
* Performance-kritische Webseiten
* XML-Dateien
* Minimale Webseiten

## Wie kompiliere ich dynamisch eine ASHX-Datei?

Die folgenden Schritte können verwendet werden, um eine ASHX-Datei mit Microsoft Visual Studio hinzuzufügen und zu kompilieren.

* Hinzufügen eines generischen Handlers – Handler1.ashx in Visual Studio
* Löschen Sie die automatisch erstellte cs-Datei.
* ashx erneut öffnen,
** CodeBehind="Handler1.ashx.cs" entfernen
** C#-Code unten hinzufügen

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
### ASHX-Beispiel

Der folgende ASHX-Code gibt die Bilddatei an die Benutzeranforderung zurück, wenn die ASHX-Datei im Internetbrowser aufgerufen wird.


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

## Verweise

* [ASHX-Datei kompilieren](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


