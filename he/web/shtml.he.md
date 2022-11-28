{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","קובץ shtml", "פורמט קובץ shtml", "סוג קובץ shtml", "קובץ", "סוג", "מהו קובץ shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - צד שרת כלול קובץ HTML",
  "description":"למד על פורמט קובץ SHTML וממשקי API שיכולים ליצור ולפתוח קובצי SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## מהו קובץ SHTML?

קובץ עם סיומת .shtml הוא דף אינטרנט שנכתב ב-[HTML](/he/web/html/) וכולל הוראות שרת. הוא עשוי גם להכיל רכיבים בצד השרת הדומים לקבצי ASP לטעינה מהירה יותר. הקבצים בצד השרת יכולים להכיל גם קוד הפעלה שיכול לגרום לשרת להיטען לאט מהרגיל. קבצי SHTML דומים ל-HTML אך הם גם מאפשרים שימוש בפקודות שרת פשוטות. פקודות שרת אלו מבוצעות בשפת תכנות מחשב פשוטה הנקראת Server Side Includes (SSI). SHTML הוחלף במידה רבה על ידי שפות תכנות אחרות בצד השרת, כגון [PHP](/he/programming/php/) כולל.

## פורמט קובץ SHTML

קובצי SHTML נכתבים בטקסט רגיל ומשתמשים ב[פקודות SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) המופעלות בצד השרת. ניתן להשתמש בפקודות אלו בצד השרת אפילו כדי להתחבר למסד נתונים באמצעות מנהלי ההתקן של מסד הנתונים ולהביא נתוני משתמשים מטבלאות.

## דוגמה SHTML

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

