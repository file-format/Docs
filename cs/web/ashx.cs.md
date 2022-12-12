{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "soubor", "přípona", "formát souboru", "ASHX", "Soubor webového obslužného programu ASP.NET" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Přípona souboru ASHX - soubor webového obslužného programu ASP.NET",
  "description" :"Zjistěte, co je soubor ASHX a rozhraní API, která mohou vytvářet a otevírat soubory ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Co je soubor ASHX?

Soubor ASHX je webová stránka, kterou používá obslužná rutina HTTP ASP.NET, aby uživateli poskytla stránky, na které se v tomto souboru odkazuje. ASP.NET HTTP Handler zpracuje příchozí požadavek, odkazuje na stránky ze souboru .ashx a odešle zkompilovanou stránku zpět do prohlížeče uživatele. Způsob zpracování je většinou podobný jako u souborů ASPX s tím rozdílem, že v tomto případě jsou odkazované stránky/dokumenty zpracovány a odeslány zpět.

## Formát souboru ASHX

Soubory .ashx jsou uloženy ve formátu prostého textového souboru a obsahují odkazy na jiné stránky nebo dokumenty, které jsou na vyžádání zaslány zpět do prohlížeče uživatele. Ty lze otevřít v jakémkoli textovém editoru a vývojářských IDE, jako je Xamarin Studio, Microsoft Notepad, Notepad++ a mnoho dalších. Soubory ASHX jsou užitečné v případě, že máte:
* Binární soubory
* Dynamické zobrazení obrázků
* Výkon-kritické webové stránky
* XML soubory
* Minimální počet webových stránek

## Jak dynamicky zkompilovat soubor ASHX?

Následující kroky lze použít k přidání a kompilaci souboru ASHX pomocí Microsoft Visual Studio.

* přidat Obecný ovladač - Handler1.ashx ve vizuálním studiu
* smažte soubor cs, který se automaticky vytvořil.
* znovu otevřete ashx,
** odstranit CodeBehind="Handler1.ashx.cs"
** níže přidejte kód c#

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
### Příklad ASHX

Následující kód ASHX vrátí soubor obrázku na žádost uživatele, když je soubor ASHX vyvolán v internetovém prohlížeči.


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

## Reference

* [Zkompilujte soubor ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


