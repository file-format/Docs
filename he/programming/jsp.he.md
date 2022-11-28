{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - פורמט קובץ דפי Java Server",
  "description":"למד על פורמט קובץ JSP עם דוגמה של JSP וממשקי API שיכולים ליצור ולפתוח קובצי JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## מהו קובץ JSP?
קובצי ה-JSP מתממשים כדפים דינמיים, מונעי נתונים עבור יישומי האינטרנט שלך ב-Java. ה-JSP פירושו Java Server Pages; יכול להתממש כהרחבה ל-Servlet מכיוון שהיא מאפשרת יותר פונקציונליות מ-servlet כמו שפת ביטוי. ה-JSP וה-Servlet עושים את אותה עבודה ביחד ביישומי אינטרנט ישנים יותר של Java. מנקודת מבט של תכנות, ההבדל הברור ביותר ביניהם הוא שעם servlets אתה כותב תוכנית Java ואז מטמיע סימון סטטי (כמו HTML) לתוך הקוד הזה, בעוד ש-JSP מתחיל עם הסקריפט או הסימון בצד הלקוח, ואז מטמיע תגיות JSP כדי חבר את הדף שלך ל-Java Backend.

## פורמט קובץ JSP
קובץ שנשמר עם **סיומת הקובץ jsp** מכיל את הסעיפים הבאים בסדר הרשימה:

1. הערות פתיחה
2. הנחיות דף JSP
3. הנחיות אופציונליות של ספריית תגים
4. הצהרת JSP אופציונלית
5. קוד HTML ו-JSP

### הערות פתיחה
קובץ JSP או קובץ פרגמנט מתחיל בהערה בסגנון צד השרת:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
ההערה למעלה מופיעה רק בצד השרת מכיוון שהיא מוסרת בזמן עיבוד הדף בדפדפן. ההערה עשויה להכיל את המידע על המחבר/ים, התאריך והודעת זכויות היוצרים של הגרסה, מזהה ותיאור על דף JSP למפתחים. שילוב התווים "@(#)" מזוהה על ידי תוכניות מסוימות כמציין תחילתו של מזהה.

### הנחיות עמוד JSP
הוראת עמוד JSP מגדירה תכונות המשויכות לדף JSPF בזמן התרגום. מפרט JSP אינו מטיל מגבלה על כמה הנחיות עמוד JSP ניתן לכתוב בעמוד בודד. ראה את הדוגמה הבאה:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
אם הנחיית עמוד חורגת מהרוחב הרגיל של דף JSP, ההנחיה מחולקת למספר שורות:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### הנחיות אופציונליות של ספריית תגים
בדף JSP, הוראת ספריית תגים מכריזה על ספריות תגים מותאמות אישית. ניתן להכריז על הנחיה קצרה בשורה אחת. הוראות ספריית תגים מרובות מוערמות יחד באותו מיקום בגוף דף ה-JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### הצהרת JSP אופציונלית
  


השיטות והמשתנים המוצהרים בקובץ JSPF צריכים להיות קיימים בהצהרות JSP. שיטות ומשתנים אלו דומים להצהרות בשפת התכנות Java, וזו הסיבה שיש לעקוב אחר מוסכמות הקוד הרלוונטיות. הצהרות נכתבות בדרך כלל ב-% בודד! ... %> בלוק הצהרת JSP, לריכוז הצהרות באזור אחד בגוף דף ה-JSP. תסתכל על הדוגמאות הבאות:

#### בלוקי הצהרה שונים:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### בלוק הצהרה מועדף:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### קוד HTML ו-JSP
חלק זה של דף JSP מכיל את גוף ה-HTML של דף JSP ואת קוד JSPF, כגון ביטויי JSP, scriptlets והוראות JavaBeans.

## מחזור חיים של דף JSP

זרימת עמודי ה-JSP מבחינת השלב ניתנת כאן:

- תרגום של דף JSP
- קומפילציה של דף JSP
- טעינת כיתות (מטעין הכיתות טוען קובץ כיתות)
- מופע (נוצר אובייקט הסרבל שנוצר).
- אתחול (המכל מפעיל את שיטת jspInit()).
- עיבוד בקשה (המכולה מפעילה את שיטת _jspService()).
- Destroy (המכל מפעיל את שיטת jspDestroy()).

{{< figure src="../jsp.jpg" alt="פורמט קובץ JSP" >}}

## דוגמה JSP

ללמוד על טכנולוגיות JSP קל מאוד כיום מכיוון שהרבה מדריכי JSP זמינים דרך האינטרנט. דוגמה ה-JSP הבאה מיועדת לעיבוד ההזמנה, על ידי עדכון הרשומות המתאימות במסד הנתונים.
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## הפניות

* [מוסכמות קוד עבור דפי JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [מדריך JSP](https://www.javatpoint.com/jsp-tutorial)

