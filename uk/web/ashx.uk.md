{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "файл", "розширення", "формат файлу", "ASHX", "Файл веб-обробника ASP.NET" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Розширення файлу ASHX - файл веб-обробника ASP.NET",
  "description" :"Дізнайтеся, що таке файл ASHX та API, які можуть створювати та відкривати файли ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Що таке файл ASHX?

Файл ASHX — це веб-сторінка, яка використовується обробником HTTP ASP.NET для надання користувачам сторінок, на які посилається цей файл. HTTP-обробник ASP.NET обробляє вхідний запит, посилається на сторінки з файлу .ashx і надсилає скомпільовану сторінку назад у браузер користувача. Метод обробки здебільшого подібний до файлів ASPX з тією відмінністю, що в цьому випадку сторінки/документи, на які посилаються, обробляються та надсилаються назад.

## Формат файлу ASHX

Файли .ashx зберігаються у форматі простого тексту та містять посилання на інші сторінки чи документи, які надсилаються назад у браузер користувача за запитом. Їх можна відкрити в будь-якому текстовому редакторі та IDE розробника, наприклад Xamarin Studio, Microsoft Notepad, Notepad++ та багатьох інших. Файли ASHX корисні, якщо у вас є:
* Бінарні файли
* Динамічні перегляди зображень
* Важливі для продуктивності веб-сторінки
* Файли XML
* Мінімум веб-сторінок

## Як динамічно скомпілювати файл ASHX?

Наступні кроки можна використати для додавання та компіляції файлу ASHX за допомогою Microsoft Visual Studio.

* додайте загальний обробник - Handler1.ashx у Visual Studio
* видалити автоматично створений файл cs.
* знову відкрити ashx,
** видалити CodeBehind="Handler1.ashx.cs"
** додайте код c# нижче

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
### Приклад ASHX

Наступний код ASHX повертає файл зображення на запит користувача, коли файл ASHX викликається в Інтернет-браузері.


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

## Список літератури

* [Скомпілювати файл ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


