{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ APPCACHE - HTML5 Cache Manifest Format",
  "description" :"למד על מהו קובץ APPCACHE וממשקי API שיכולים ליצור ולפתוח קובצי APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## מהו קובץ APPCACHE?

קובץ APPCACHE הוא קובץ טקסט המכיל את רשימת המשאבים שיש לאחסן במטמון על ידי דפדפנים לגישה לא מקוונת ליישומי האינטרנט. זה שימושי כאשר אין חיבור לאינטרנט. במצב כזה, הדפדפן משתמש במשאבי המטמון הלא מקוונים כדי לספק גישה לתוכן האינטרנט. קובץ APPCACHE מכיל משאבי אינטרנט כגון תמונות (לדוגמה **[PNG](/he/image/png/)**, **[WEBP](/he/image/webp/)** וכו'), גיליונות סגנונות **([ CSS])(/he/web/css/)**, וקובצי סקריפט (כגון קבצי Javascript **[JS](/he/web/js/)**).

יישומים שיכולים **לפתוח קובצי APPCACHE** כוללים דפדפני אינטרנט כגון Google Chrome, Safari ו-Firefox.

## פורמט קובץ APPCACHE - מידע נוסף

קבצי APPCACHE הם קבצי טקסט פשוטים, המספקים גישה לא מקוונת לדפי אינטרנט להפעלה ללא חיבור לאינטרנט. הנוכחות של APPCACHE מציינת דף כזמין במצב לא מקוון.

### כיצד להפנות לקובץ APPCACHE?

בדף ה-HTML שלך, קובץ APPCACHE מופנה כדלקמן.

```
<html manifest="example.appcache">
  ...
</html>
```

## מבנה של קובץ מניפסט APPCACHE

קובץ מניפסט פשוט של APPCACHE נראה כדלקמן.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

זוהי הדוגמה הפשוטה ביותר ויכולים להיות קיימים גם מבנים מורכבים יותר.

## היתרונות של APPCACHE Manifest

השימוש בממשק מטמון מעניק ליישומי אינטרנט את היתרונות הבאים.

1. גלישה לא מקוונת - ממשק המטמון נותן למשתמשי הקצה לגלוש באתר המלא שלך כשהם במצב לא מקוון
1. מהירות - מטמון מאפשר גישה במהירות גבוהה לתוכן לא מקוון ישירות מהדיסק
1. נגישות כל הזמן - במקרה שהאתר שלך נופל, למשתמשים עדיין תהיה גישה לתוכן האינטרנט ויוכלו לקבל את החוויה הלא מקוונת

## הפניות

* [מדריך למתחילים ל-AppCache Manifest](https://web.dev/appcache-beginner/)

