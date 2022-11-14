{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "file", "estensione", "formato file", "ASHX", "File gestore Web ASP.NET"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Estensione file ASHX - Un file gestore Web ASP.NET",
  "description" :"Scopri cos'è un file ASHX e le API che possono creare e aprire file ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Che cos'è un file ASHX?

Un file ASHX è una pagina Web utilizzata dal gestore HTTP ASP.NET per fornire all'utente le pagine a cui si fa riferimento all'interno di questo file. Il gestore HTTP ASP.NET elabora la richiesta in entrata, fa riferimento alle pagine del file .ashx e rinvia la pagina compilata al browser dell'utente. Il metodo di elaborazione è per lo più simile a quello dei file ASPX con la differenza che in questo caso le pagine/documenti di riferimento vengono elaborati e rispediti.

## Formato file ASHX

I file .ashx vengono salvati in formato di file di testo normale e contengono riferimenti ad altre pagine o documenti che vengono inviati al browser dell'utente su richiesta. Questi possono essere aperti in qualsiasi editor di testo e IDE per sviluppatori come Xamarin Studio, Microsoft Notepad, Notepad++ e molti altri. I file ASHX sono utili nel caso in cui tu abbia:
* File binari
* Viste di immagini dinamiche
* Pagine Web critiche per le prestazioni
* File XML
* Pagine web minime

## Come compilare dinamicamente un file ASHX?

I seguenti passaggi possono essere utilizzati per aggiungere e compilare un file ASHX utilizzando Microsoft Visual Studio.

* aggiungi un gestore generico - Handler1.ashx in Visual Studio
* elimina il file cs creato automaticamente.
* riapri ashx,
** rimuovi CodeBehind="Handler1.ashx.cs"
** aggiungi il codice c# di seguito

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
### Esempio ASHX

Il seguente codice ASHX restituisce il file immagine alla richiesta dell'utente quando il file ASHX viene chiamato nel browser Internet.


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

## Riferimenti

* [Compila file ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


