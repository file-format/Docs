{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "קובץ asmx", "פורמט קובץ asmx", "סוג קובץ asmx", "קובץ", "סוג", "מהו קובץ asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET Web Service File",
  "description" :"למד על מהו קובץ ASMX וממשקי API שיכולים ליצור ולפתוח קובצי ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## מהו קובץ ASMX?

קובץ עם סיומות .asmx הוא קובץ ASP.NET Web Service המספק תקשורת בין שני אובייקטים דרך האינטרנט באמצעות פרוטוקול הגישה לאובייקטים פשוטים (SOAP). הוא נפרס כשירות בשרת האינטרנט מבוסס Windows כדי לעבד בקשה נכנסת ולהחזיר את התגובה. בניגוד לקבצי [ASPX](/he/web/aspx/) המכילים את הקוד לתצוגה ויזואלית של דפי אינטרנט של ASP.NET, קבצי ASMX רצים בשרת ברקע ומבצעים משימות שונות כגון חיבור למסד נתונים, אחזור נתונים והחזרתם ב- פורמט שבו הוגשה הבקשה. אלה משמשים במיוחד עבור שירותי אינטרנט של XML.

## פורמט קובץ ASMX

קבצי ASMX הם בפורמט טקסט רגיל וניתן לפתוח אותם או לערוך אותם ביישומים כגון Microsoft Visual Studio או עורכי טקסט. זהו פורמט קובץ קנייני של מיקרוסופט ויש לו תחביר מוגדר היטב ליצירת שירותי אינטרנט. תגובה על ידי קובץ ASMX בצורה של SOAP XML כוללת את האלמנטים הבאים.

* `Envelop` - אלמנט שורש המזהה את מסמך ה-XML כהודעת SOAP.
* `Header` - רכיב אופציונלי המכיל מידע ספציפי ליישום כגון נתוני אימות. אם הרכיב Header קיים, הוא חייב להיות רכיב הצאצא הראשון של רכיב Envelope.
* `גוף` - מכיל את הודעת SOAP המיועדת לנמען.
* 'תקלה' - רכיב אופציונלי המשמש לציון הודעות שגיאה. אם הרכיב Fault קיים, הוא חייב להיות רכיב צאצא של אלמנט ה-Body.

ניתן לכתוב קבצי ASMX בשפות NET כגון [C#](/he/programming/cs/), [Visual Basic](/he/programming/vb/) או JScript.

## במה שונה ASMX מ-ASPX ו-ASCX?

קבצי ASMX שונים מקובצי ASPX ו-ASCX.

* ASPX, Active Server Pages, קבצים הם קבצי תכנות שנוצרים באמצעות Microsoft ASP.NET Framework הפועל על שרתי אינטרנט. אלה מוצגים בדפדפן האינטרנט של הלקוח כאשר משתמש מבקש לגשת לדף כזה.
* ASCX, Active Server User Control, מגדיר פקדי משתמש המשמשים להגדרת פקדים הניתנים לשימוש חוזר בדפי אינטרנט של ASP.NET או באתר כולו.

## הפניות

* [צורך שירות ASMX](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [בקרת משתמש ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

