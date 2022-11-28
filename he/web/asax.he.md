{
  "date" : "2019-10-11",
  "keywords" :[ "asax","קובץ asax", "פורמט קובץ asax", "סוג קובץ asax", "קובץ", "סוג", "מהו קובץ asax" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET Server Application File",
  "description" :"למד לדעת מה זה קובץ ASAX וממשקי API שיכולים ליצור ולפתוח קבצי ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## מהו קובץ ASAX?

קובץ עם סיומת .asax הוא קובץ המשמש יישומי ASP.NET שנמצא בצד השרת. הוא מכיל קוד לתגובה לאירועים ברמת האפליקציה וברמת ההפעלה שהועלו על ידי ASP.NET או על ידי מודולי HTTP. זה כולל גם טיפול באירועים מסוימים כאשר האפליקציה מופעלת או נכבית. קבצי ASAX הם אופציונליים ורק קובץ ASAX יחיד נוסף ליישומי אינטרנט כדי לטפל באירועים ובשגיאות ברמת האפליקציה ברמה הגלובלית. שלא כמו דפי ASPX, קבצי ASAX אינם מכילים שום קוד ליישום הפונקציונליות של האפליקציה.

## פורמט קובץ ASAX

קבצי ASAX נכתבים בפורמט קובץ טקסט רגיל וניתנים לקריאה אנושית. קובץ ASAX הנפוץ ביותר הוא Global.asax שנמצא בספריית השורש של יישום ASP.NET. שרתי אינטרנט מוגדרים לדחות כל שיחות נכנסות לקובץ זה כדי לאסור על משתמשים להוריד או לצפות בקוד של קובץ זה.

### Global.ASAX - דוגמה לפורמט קובץ ASAX

קובץ ASAX יחיד מורכב ממספר חלקים שנכתבים כדי לטפל באירועים ברמת היישום. אלה הם כדלקמן.

* **הנחיות יישומים** - הנחיות יישומים הן תגיות המשמשות להגדרת הגדרות אופציונליות ספציפיות ליישום שישמשו את מנתח ASP.NET בעת עיבוד הקובץ Global.asax. הנחיות אלו ממוקמות בתחילת הקובץ Global.asax ומוגדרות כדלקמן.

```
<%@ directive attribute=value [attribute=value … ]%>
```
* **קובצי הצהרת קוד** - בלוקים של הצהרת קוד משמשים להגדרת קטעים של קוד שרת המוטמעים בקבצי יישום ASP.NET בתוך \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Code Render Blocks** - אלה מגדירים את הקוד המוטבע או הביטויים המופעלים כאשר הדף מעובד. שני הסגנונות של בלוקים לעיבוד קוד כוללים קוד מוטבע וביטויים מוטבעים. הראשון משמש להגדרת שורות או בלוקים של קוד עצמאיים, בעוד שהצדדי משמש כקיצור לקריאה לשיטת הכתיבה.

## הפניות

* [סקירה כללית של מטפלי HTTP ומודול HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax תחביר](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

