{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP Fragment File Format",
  "description":"למד על פורמט קובץ JSPF וממשקי API שיכולים ליצור ולפתוח קובצי JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## מהו קובץ JSPF?
הקובץ עם סיומת jspf נקרא JSP fragment; קובץ סטטי הכלול בקובץ JSP אחר. קובצי ה-JSPF אינם מורכבים בפני עצמם, עם זאת, הם מורכבים לצד הדף שבו הם כללו. התחביר שלו דומה לקוד Java Server Pages (JSP). הוא מכיל רק קטע של JSP; לא כלל את כל מסמך ה-JSP.

## פורמט קובץ JSPF
המונח "קטע JSP" משמש במקום זאת מכיוון שהמונח "קטע JSP" עמוס יתר על המידה במפרט JSP 2.0. קטעי ה-JSP יכולים להשתמש בסיומות .jsp או .jspf ויש למקם אותם ב-**/WEB-INF/jspf** או עם שאר הקבצים הסטטיים. קטעי JSP שאינם דפים שלמים חייבים להשתמש בסיומת .jspf ויש למקם אותם ב-**/WEB-INF/jspf**

### JSP או JSP Fragment File Organization
קובץ JSP מכיל את הסעיפים הבאים לפי סדר הרשימה:

1. הערות פתיחה
2. הנחיות דף JSP
3. הנחיות אופציונליות של ספריית תגים
4. הצהרת JSP אופציונלית
5. קוד HTML ו-JSP

קובץ JSP או JSPF מתחילים שניהם בהערה בסגנון צד השרת הנקראת **הערת פתיחה**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
הערה זו יכולה להיות גלויה רק בצד השרת מכיוון שהיא מוסרת במהלך עיבוד עמודי JSP.

## מתי להשתמש בקובץ JSP Fragment?
כאשר דף JSP דורש מבנה מסוים אך מורכב שעשוי לעשות שימוש חוזר גם בדפי JSP אחרים, אחת הדרכים להתמודד עם זה היא לפרק אותו לחתיכות, באמצעות תבנית התצוגה המרוכבת (הקטע Patterns של Java Blueprints). לדוגמה, לדף JSP יש לפעמים את הפריסה ההגיונית הבאה במבנה המצגת שלו:

{{< figure src="../jspf.png" alt="פורמט קובץ JSPF" >}}

במצב זה, ניתן להמיר עמוד JSP מורכב זה למודולים שונים, כל אחד מהם ייקרא קטע JSP נפרד. לאחר מכן ניתן למקם את קטעי ה-JSP במקומות המתאימים בדף ה-JSP המשולב. לפיכך, נעשה שימוש בקובץ JSPF כאשר משתמשים בהנחיות כוללות סטטיות כדי לכלול דף שלא ייקרא בעצמו, יש למקם את הקבצים עם סיומת .jspf בספריית /WEB-INF/jspf/ של ארכיון יישומי האינטרנט ( מִלחָמָה).

## דוגמה JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## הפניות

* [מוסכמות קוד עבור דפי JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

