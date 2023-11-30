{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ AXD - ASP.NET Web Handler Format",
  "description" :"למד על מהו קובץ AXD וממשקי API שיכולים ליצור ולפתוח קובצי AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## מהו קובץ AXD?

קובץ AXD הוא קובץ הגדרות אינטרנט המשמש לטיפול ואחזור של בקשות משאבים משובצות ב-ASP.NET. הוא מורכב מהוראות לאחזור משאבים מוטמעים כגון תמונות, קבצי JavaScript ([.JS](/he/web/js/)) וקבצי [.CSS](/he/web/css/). קבצי AXD משמשים להזרקת משאבים לדפים בצד הלקוח. זה מאפשר לדפי לקוח לגשת למשאבים אלה בשרת בצורה סטנדרטית.

## פורמט קובץ AXD

קבצי AXD מאוחסנים כקבצים בינאריים בצד השרת. זה מתייחס לקובץ Web Handler ב-ASP.NET שהם רכיבים שמייצרים תגובות לבקשות ספציפיות לשרת אינטרנט. קובצי AXD מבצעים עיבוד מותאם אישית לפני יצירת התגובה בהתבסס על בקשות עמוד צד הלקוח. אלה נשמרים בדרך כלל כקבצי **WebResource.axd**.

### מהו קובץ WebResource.axd?

רוב הפרויקטים של ASP.NET שומרים קבצי AXD כקבצי WebResource.axd המאפשרים לדפים בצד הלקוח להוריד משאבים המוטמעים במכלול. היישום שלך עשוי להתמודד עם ביצועים איטיים במקרה שתפעיל אותו במצב ניפוי באגים מכיוון שהמטפל WebResources.axd אינו שמור במטמון.

## הפניות

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

