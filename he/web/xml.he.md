{
  "date" : "2019-10-11",
  "keywords" :["xml", "קובץ", "הרחבה", "פורמט קובץ", "הרחבת קובץ", "שפת סימון הניתנת להרחבה"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ XML",
  "description":"למד על פורמט קובץ XML וממשקי API שיכולים ליצור ולפתוח קובצי XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ XML?

XML מייצג Extensible Markup Language הדומה ל-**[HTML](/he/web/html/)** אך שונה בשימוש בתגים להגדרת אובייקטים. כל הרעיון מאחורי יצירת פורמט קובץ XML היה לאחסן ולהעביר נתונים מבלי להיות תלוי בתוכנה או בכלי חומרה. הפופולריות שלו נובעת מכך שהוא קריא אנושי וגם במכונה. זה מאפשר לו ליצור פרוטוקולי נתונים נפוצים בצורת אובייקטים שיש לאחסן ולשתף ברשת כגון World Wide Web (WWW). ה-"X" ב-XML מיועד להרחבה, מה שמרמז שניתן להרחיב את השפה לכל מספר סמלים לפי דרישות המשתמש. עבור תכונות אלה, פורמטים סטנדרטיים רבים של קבצים עושים בהם שימוש כגון Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/he/web/xhtml/)** ו-**[SVG](/he/page-description-language /svg/)**.

## פורמט קובץ XML

פורמט קובץ ה-XML מבוסס על מודל ה-XML Document Object Model (DOM) שהוא ממשק API לתכנות עבור מסמכי HTML ו-XML. ה-XML DOM מגדיר שיטה סטנדרטית לגישה ולטפל ברכיבי מסמך ה-XML. זה יוצר תצוגת מבנה עץ של מסמך XML שניתן להשתמש בו כדי לגשת לכל האלמנטים דרך עץ ה-DOM. ניתן לשנות/למחוק אלמנטים קיימים וכן ניתן ליצור אלמנטים חדשים בעץ ה-XML. כל רכיב במסמך XML נקרא צומת. ה-XML DOM הוא כפי שמוצג בתמונה הבאה.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### גישה אוניברסלית של XML

העוצמה של XML הופכת אותה לשפה אוניברסלית לתקשורת נתונים ברשת על ידי הפיכת העברת הנתונים ושינויי הפלטפורמה לפשוטים יותר. זה גם מבטיח החלפת נתונים בין מערכות לא תואמות על ידי אחסון נתונים בפורמט טקסט רגיל. HTML מיועד לייצוג נתונים דרך האינטרנט, בעוד ש-XML מיועד להחלפת נתונים. צמדי תגי הסימון המשמשים ב-XML מגדירים את מרכיבי המפתח של המבנה שישמשו על ידי קריאת יישומים.

## דוגמה XML

להלן דוגמה פשוטה של קטלוג תקליטורים שבו כל רשומה מכילה מידע על תקליטורים כגון אמן, מדינה, חברה, מחיר ושנת ייצור.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## הפניות

* [XML - מאת ויקיפדיה](https://en.wikipedia.org/wiki/XML)

