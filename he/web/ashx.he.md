{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "קובץ", "סיומת", "פורמט קובץ", "ASHX", "קובץ מטפל אינטרנט של ASP.NET" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"הרחבת קובץ ASHX - קובץ מטפל אינטרנט של ASP.NET",
  "description" :"למד על מהו קובץ ASHX וממשקי API שיכולים ליצור ולפתוח קבצי ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## מהו קובץ ASHX?

קובץ ASHX הוא דף אינטרנט המשמש את ASP.NET HTTP Handler כדי לספק למשתמש את הדפים שאליהם מפנים קובץ זה. ה-HTTP Handler של ASP.NET מעבד את הבקשה הנכנסת, מפנה לדפים מקובץ ה-.ashx ושולח בחזרה את הדף המהודר בחזרה לדפדפן המשתמש. שיטת העיבוד דומה ברובה לזו של קבצי ASPX עם ההבדל שבמקרה זה, הדפים/מסמכים שהפניה אליהם מעובדים ונשלחים חזרה.

## פורמט קובץ ASHX

קבצי ה-.ashx נשמרים בפורמט קובץ טקסט רגיל ומכילים הפניות לדפים או מסמכים אחרים הנשלחים חזרה לדפדפן המשתמש לפי בקשה. אלה ניתנים לפתיחה בכל עורך טקסט ומפתחים IDE כגון Xamarin Studio, Microsoft Notepad, Notepad++ ועוד רבים אחרים. קבצי ASHX שימושיים למקרה שיש לך:
* קבצים בינאריים
* תצוגות תמונה דינמיות
* דפי אינטרנט קריטיים לביצועים
* קבצי XML
* מינימום דפי אינטרנט

## כיצד לבצע קומפילציה דינמית של קובץ ASHX?

ניתן להשתמש בשלבים הבאים כדי להוסיף ולהדר קובץ ASHX באמצעות Microsoft Visual Studio.

* הוסף מטפל גנרי - Handler1.ashx ב- Visual Studio
* מחק את קובץ cs שנוצר אוטומטית.
*פתח שוב את אשקס,
** הסר CodeBehind="Handler1.ashx.cs"
** הוסף קוד c# למטה

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
### דוגמה של ASHX

קוד ASHX הבא מחזיר את קובץ התמונה לבקשת המשתמש כאשר קובץ ASHX נקרא בדפדפן האינטרנט.


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

## הפניות

* [הידור קובץ ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


