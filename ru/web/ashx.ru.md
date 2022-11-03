{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "файл", "расширение", "формат файла", "ASHX", "файл веб-обработчика ASP.NET" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Расширение файла ASHX — файл веб-обработчика ASP.NET",
  "description" :"Узнайте, что такое файл ASHX и API, которые могут создавать и открывать файлы ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## .ASHX вариант №

Файл ASHX — это веб-страница, используемая обработчиком HTTP ASP.NET для предоставления пользователю страниц, на которые есть ссылки в этом файле. Обработчик HTTP ASP.NET обрабатывает входящий запрос, ссылается на страницы из файла .ashx и отправляет скомпилированную страницу обратно в браузер пользователя. Метод обработки в основном аналогичен способу файлов ASPX с той разницей, что в этом случае страницы/документы, на которые есть ссылки, обрабатываются и отправляются обратно.

## Формат файла ASHX

Файлы .ashx сохраняются в текстовом формате и содержат ссылки на другие страницы или документы, которые по запросу отправляются обратно в браузер пользователя. Их можно открыть в любом текстовом редакторе и среде разработки для разработчиков, например Xamarin Studio, Microsoft Notepad, Notepad++ и многих других. Файлы ASHX полезны в случае, если у вас есть:
* Бинарные файлы
* Динамические просмотры изображений
* Критически важные для производительности веб-страницы
* XML-файлы
* Минимум веб-страниц

## Как динамически скомпилировать файл ASHX?

Следующие шаги можно использовать для добавления и компиляции файла ASHX с помощью Microsoft Visual Studio.

* добавить общий обработчик - Handler1.ashx в Visual Studio
* удалить автоматически созданный файл cs.
* снова открыть ashx,
** удалить CodeBehind="Handler1.ashx.cs"
** добавьте код С# ниже

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
### Пример ASHX

Следующий код ASHX возвращает файл изображения по запросу пользователя, когда файл ASHX вызывается в интернет-браузере.


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

## использованная литература

* [Скомпилировать файл ASHX] (https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


