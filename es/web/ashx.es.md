{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "archivo", "extensión", "formato de archivo", "ASHX", "Archivo de controlador web ASP.NET" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Extensión de archivo ASHX: un archivo de controlador web ASP.NET",
  "description" :"Obtenga información sobre qué es un archivo ASHX y las API que pueden crear y abrir archivos ASHX",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## ¿Qué es un archivo ASHX?

Un archivo ASHX es una página web que utiliza el controlador HTTP de ASP.NET para proporcionar al usuario las páginas a las que se hace referencia dentro de este archivo. El controlador HTTP de ASP.NET procesa la solicitud entrante, hace referencia a las páginas del archivo .ashx y devuelve la página compilada al navegador del usuario. El método de procesamiento es en su mayoría similar al de los archivos ASPX con la diferencia de que, en este caso, las páginas/documentos a los que se hace referencia se procesan y se devuelven.

## Formato de archivo ASHX

Los archivos .ashx se guardan en formato de archivo de texto sin formato y contienen referencias a otras páginas o documentos que se envían de vuelta al navegador del usuario a pedido. Estos se pueden abrir en cualquier editor de texto e IDE de desarrollador, como Xamarin Studio, Microsoft Notepad, Notepad ++ y muchos más. Los archivos ASHX son útiles en caso de que tenga:
* Archivos binarios
* Vistas de imágenes dinámicas
* Páginas web críticas para el rendimiento
* Archivos XML
* Páginas web mínimas

## ¿Cómo compilar dinámicamente un archivo ASHX?

Los siguientes pasos se pueden usar para agregar y compilar un archivo ASHX usando Microsoft Visual Studio.

* agregue un controlador genérico - Handler1.ashx en Visual Studio
* elimine el archivo cs que se creó automáticamente.
* abre ashx de nuevo,
** eliminar CodeBehind="Handler1.ashx.cs"
** agregue el código C# a continuación

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
### Ejemplo de ASHX

El siguiente código ASHX devuelve el archivo de imagen a la solicitud del usuario cuando se llama al archivo ASHX en el navegador de Internet.


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

## Referencias

* [Compilar archivo ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


