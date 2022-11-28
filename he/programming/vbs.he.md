{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "קובץ", "סיומת", "פורמט קובץ", "Visual Basic Script", "מדריך תכנות", "vbs example", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic Script File",
  "description":"למד על פורמט קובץ VBS וממשקי API שיכולים ליצור ולפתוח קובצי VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## מהו קובץ VBS?

VBS או VBScript קשורים למהדורת הסקריפט של Microsoft Visual Basic. בסביבת המחשוב, המשתמש רשאי לגשת ולשלוט בהיבטים רבים שלה. ל-VBScript מותר להשתמש במודל בשם **Component Object Model** כדי להיעזר באלמנטים ובכלים של הסביבה. סביבה זו מוגדרת לעבודה ולהפעלה של VBScript.

הוא משמש כדומה ל-Javascript כאשר הלקוח ניגש אליו בתחום של פיתוח אתרים. הוא משמש גם את השרתים לעיבוד דפי אינטרנט. זה יכול להיחשב בכמה סוגים אחרים של קבצי סקריפטים, כגון יישומים של [HTML](/he/web/html/).


## היסטוריה קצרה ##

הוא הושק לראשונה בשנת 1996, כחלק מהטכנולוגיות המשמשות את מיקרוסופט שצוינו עבור סקריפטים של Windows. זה פותח במיוחד לעזרת מפתחי אינטרנט בתחילה. באותה שנה שוחרר הסייר של Microsoft Windows בשם Internet Explorer יחד עם התכונות של Visual Basic Script.

עם ההתקדמות בטכנולוגיה ובפיתוח אתרים, הושקו גרסאות רבות של VBScript יחד עם תכונות מתקדמות רבות. יתרה מכך, בשנה הקרובה, שפת סקריפטים זו תהיה חלק מ-Microsoft Windows עם תכונות חדשות.

## מפרט טכני ##

עבור דפי האינטרנט בצד השרת, נעשה שימוש בכלים כגון **Active Server Pages** יחד עם VBScript. ניתן להשתמש בשפת סקריפט זו גם ברכיב הסקריפט של Windows. הקבצים של שפה זו מאוחסנים עם סיומת .vbs ב-Windows.

ישנם מבני בקרה רבים כגון לולאות המשמשות בקוד של שפה זו. הוא כולל גם ארגומנטים שהם שורת פקודה ויכולים לקבל שם או ללא שם. ניתן לאחסן את הקבצים של שפה זו פשוט בתיקיות או בשולחן העבודה של מערכת הפעלה Windows. למרות שאין סביבת פיתוח משולבת ספציפית עבור תוכניות VBScript כמו Microsoft Script Editor מספקות את המתקן לפיתוח של שפה זו.

כאשר VBScript מתארח על ידי מארח הסקריפט של Windows, הוא מספק תכונות שונות שדי נפוצות לשפות הסקריפט אך אינן זמינות ב-Visual Basic 6.0. התכונות הכרוכות בגישה קלה או ישירה כוללות מדפסות רשת, ארגומנטים של שורת פקודה ללא שם ושם, stdout ו-stdin, שיתופי רשת, מכשור לניהול Windows, מידע משתמש של רשתות כמו חברות בקבוצה ועוד הרבה יותר.

## דוגמה לפורמט קובץ VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## התייחסות ##

* [VBS - מאת ויקיפדיה](https://en.wikipedia.org/wiki/VBScript)



