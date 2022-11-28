{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "פורמט קובץ", "סוג קובץ", "מהו קובץ .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - קובץ תצורה של ASP",
  "description" :"למד על מהו קובץ ASA וממשקי API שיכולים ליצור ולפתוח קבצי ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## מהו קובץ ASA?

קובץ ASA הוא קובץ תצורה, שנוצר עבור פרויקטים של [ASP](/he/web/asp/)/ASP.NET. הוא מכיל הצהרות על משתנים, מכיל ופונקציות שנועדו להיות נגישים ברמה גלובלית באפליקציה. כל הדפים בפרויקט יכולים לגשת למשתנים ולפונקציות הללו, ובכך להימנע מהדרישה לשכתב אותם. דוגמה אחת כזו היא הדף Global.asa המאוחסן בספריית השורש כדי שיהיה נגיש לדפי אתר אחרים של ASP. קבצי Global.asa הם אופציונליים, אך אם משתמשים בהם, כל יישום יכול לכלול רק קובץ Global.asa אחד.

## פורמט קובץ ASA - מידע נוסף

קבצי ASA הם קבצי טקסט רגיל עם המידע הבא.

* אירועי אפליקציה
* אירועי מושב
*\<object> הצהרות
* הצהרות TypeLibrary
* ההנחיה #include

## דוגמה לקובץ ASA

קובץ Global.asa יכול להיראות בערך כך.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## הפניות

* [קובץ ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

