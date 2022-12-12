{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "файл", "разширение", "файлов формат", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файлово разширение ASHX – файл за уеб манипулатор на ASP.NET",
  "description" :"Научете какво е ASHX файл и API, които могат да създават и отварят ASHX файлове.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Какво е ASHX файл?

ASHX файлът е уеб страница, която се използва от ASP.NET HTTP Handler, за да обслужва потребителя със страниците, които са посочени в този файл. ASP.NET HTTP Handler обработва входящата заявка, препраща към страниците от .ashx файла и изпраща обратно компилираната страница обратно към браузъра на потребителя. Методът на обработка е до голяма степен подобен на този на ASPX файловете с тази разлика, че в този случай посочените страници/документи се обработват и изпращат обратно.

## Файлов формат ASHX

Файловете .ashx се записват във формат на обикновен текстов файл и съдържат препратки към други страници или документи, които се изпращат обратно към браузъра на потребителя при поискване. Те могат да бъдат отворени във всеки текстов редактор и IDE за разработчици като Xamarin Studio, Microsoft Notepad, Notepad++ и много други. ASHX файловете са полезни в случай, че имате:
* Двоични файлове
* Динамични изгледи на изображения
* Критични за производителността уеб страници
* XML файлове
* Минимални уеб страници

## Как динамично да компилирам ASHX файл?

Следните стъпки могат да се използват за добавяне и компилиране на ASHX файл с помощта на Microsoft Visual Studio.

* добавете Generic манипулатор - Handler1.ashx във Visual Studio
* изтрийте cs файла, който е създаден автоматично.
* отворете отново ashx,
** премахнете CodeBehind="Handler1.ashx.cs"
** добавете C# код по-долу

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
### Пример за ASHX

Следният ASHX код връща файла с изображение към заявка на потребителя, когато ASHX файлът бъде извикан в интернет браузъра.


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

## Препратки

* [Компилиране на ASHX файл](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


