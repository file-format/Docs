{
  "date" : "2021-05-20",
  "keywords" :[ "stml","קובץ stml", "פורמט קובץ stml", "סוג קובץ stml", "קובץ", "סוג", "מהו קובץ stml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML File",
  "description":"למד על פורמט קובץ STML וממשקי API שיכולים ליצור ולפתוח קובצי STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## מהו קובץ STML?

קובץ עם סיומת .stml הוא דף אינטרנט עם הוראות בצד השרת שמתבצעות כאשר משתמש טוען את הדף בדפדפן האינטרנט. דפי STML מכילים קוד צד שרת המכיל כולל צד שרת לביצוע משימות שלא ניתן להשיג עם HTML רגיל. למרות שדומה ל-[HTML](/he/web/html/), STML מציעה יותר כוח על ידי הפעלת הפקודות בשרת, הנקראת גם Server Side Includes (SSI). עם הצגת שפות תכנות חדשות עם סקריפטים בצד השרת כמו PHP, השימוש ב-STML מצטמצם למרות שהוא עדיין נתמך על ידי כל הטכנולוגיות בצד השרת. ניתן לפתוח קבצי STML בכל עורך טקסט ולערוך אותם לצורך עדכון הפקודות.

## פורמט קובץ STML

STML מבוסס על פורמט קובץ טקסט ASCII רגיל הניתן לקריאה אנושית. עם זאת, הוא עוקב אחר התחביר כפי שהוגדר ומופעל באמצעות [פקודות SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) המבוצעות בצד השרת. כמו כל שפת סקריפטים אחרת בצד השרת, STML יכול להשתמש בפקודות בצד השרת כדי לבצע משימות כגון מונה מבקרים בעמוד, לוח שנה של דפי אינטרנט, אחזור רשומות ממסד נתונים ואחרות דומות.

## דוגמה STML

הוראות בצד השרת משמשות ביישומים כגון עבור מונה מבקרים בדפים או לוח שנה של דפי אינטרנט. הדוגמה הבאה מציגה את ארבע העמודות הראשונות של שלוש השורות הראשונות של מסד הנתונים של המשתמשים.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## הפניות

* [Server Side Includes](https://en.wikipedia.org/wiki/Server_Side_Includes)

