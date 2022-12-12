{
  "date" : "2019-10-11",
  "keywords" :["ashx", "plik", "rozszerzenie", "format pliku", "ASHX", "Plik ASP.NET Web Handler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Rozszerzenie pliku ASHX — plik modułu obsługi sieci Web ASP.NET",
  "description" :"Dowiedz się, co to jest plik ASHX i interfejsy API, które mogą tworzyć i otwierać pliki ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Czym jest plik ASHX?

Plik ASHX to strona internetowa używana przez moduł obsługi HTTP ASP.NET do udostępniania użytkownikom stron, do których odwołuje się ten plik. Program obsługi HTTP ASP.NET przetwarza przychodzące żądanie, odwołuje się do stron z pliku .ashx i odsyła skompilowaną stronę z powrotem do przeglądarki użytkownika. Metoda przetwarzania jest w większości podobna do metody plików ASPX, z tą różnicą, że w tym przypadku strony/dokumenty, do których się odwołuje, są przetwarzane i odsyłane.

## Format pliku ASHX

Pliki .ashx są zapisywane w formacie zwykłego pliku tekstowego i zawierają odniesienia do innych stron lub dokumentów, które na żądanie są odsyłane do przeglądarki użytkownika. Można je otwierać w dowolnym edytorze tekstu i programistycznych środowiskach IDE, takich jak Xamarin Studio, Microsoft Notepad, Notepad++ i wiele innych. Pliki ASHX są przydatne w przypadku, gdy masz:
* Pliki binarne
* Dynamiczne widoki obrazu
* Strony internetowe o krytycznym znaczeniu dla wydajności
* Pliki XML
* Minimalne strony internetowe

## Jak dynamicznie skompilować plik ASHX?

Aby dodać i skompilować plik ASHX za pomocą programu Microsoft Visual Studio, można wykonać następujące kroki.

* dodaj ogólny program obsługi - Handler1.ashx w Visual Studio
* Usuń plik cs, który został automatycznie utworzony.
* ponownie otwórz ashx,
** usuń CodeBehind="Handler1.ashx.cs"
** dodaj kod C# poniżej

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
### ASHX Przykład

Poniższy kod ASHX zwraca plik obrazu na żądanie użytkownika, gdy plik ASHX jest wywoływany w przeglądarce internetowej.


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

## Bibliografia

* [Skompiluj plik ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


