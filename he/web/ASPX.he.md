{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","קובץ aspx", "פורמט קובץ aspx", "סוג קובץ aspx", "קובץ", "סוג", "מהו קובץ aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ ASPX",
  "description" :"מדריך פורמט הקבצים שלך כדי ללמוד מהו קובץ ASPX וממשקי API שיכולים ליצור ולפתוח קובצי ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ ASPX?

קובץ עם סיומת .aspx הוא דף אינטרנט שנוצר באמצעות Microsoft ASP.NET Framework הפועל על שרתי אינטרנט. ASPX ראשי תיבות של Active Server Pages Extended ודפים אלה מוצגים בדפדפן אינטרנט בקצה המשתמש כאשר הגישה לכתובת ה-URL. הוא יורש של טכנולוגיית [ASP](/he/web/asp/) אשר נוצרת גם בקצה השרת אך אינה משתמשת ב-.NET Framework. דפי ASP.NET עשויים להכיל סקריפטים [C#](/he/programming/cs/) או [VB.NET](/he/programming/vb/) המתורגמים ל-HTML על ידי שרת האינטרנט להצגה בפני המשתמש בדפדפן האינטרנט. דפי ASPX נקראים גם .NET Web Forms. ניתן לפתוח וליצור באמצעות יישומים כמו Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ וכל עורך טקסט.

## פורמט קובץ ASPX

טפסי אינטרנט של ASP.NET מבוססים על מודל מונחה אירועים לאינטראקציות עם יישום האינטרנט. הדפדפן, בהיותו משתמש קצה, שולח טופס אינטרנט לשרת והשרת מחזיר עמוד סימון מלא או דף HTML בתגובה. מודל רכיב ASP.NET מציע מודל אובייקט עבור דפי ASPX. מודל זה מתאר:

* מקבילים בצד השרת של כמעט כל רכיבי HTML או תגיות, כגון \<form style=";text-align:right;direction:rtl"> ו\<input> .
* בקרות שרת, המסייעות בפיתוח ממשק משתמש מורכב. לדוגמה, פקד לוח השנה או פקד Gridview.

קובצי ASPX משתמשים במודל ASP.NET **Code Behind** לבניית דפים אלה.

### קוד בשורה

קוד לדוגמה שמוטבע בשורה בדף ASPX ומספק את כל הפונקציונליות עבור הטמעת המשתמש. קוד [C#](/he/programming/cs/) הבא מייצג דף ASP.NET לדוגמה הכולל קוד בשורה:

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### קוד-מאחורי

ניתן לכתוב ולאחסן קוד בקבצי מחלקה נפרדים להפרדה נקייה של HTML מהיגיון המצגת. זה הופך את שכבת המצגת לבלתי תלויה בקוד ההפעלה. להלן הקוד שמאחורי להצגה למשתמש.

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

יישום ה-C# של ההיגיון בפועל עבור שכבת המצגת הוא כדלקמן.

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## הפניות

* [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

