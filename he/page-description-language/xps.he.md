{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "XML Paper Specifications", "File", "Extension", "File Format", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - פורמט קובץ פריסת עמוד",
  "description":"למד על פורמט קובץ XPS וממשקי API שיכולים ליצור ולפתוח קובצי XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## מהו קובץ XPS? ##

קובץ XPS מייצג קובצי פריסת עמודים המבוססים על XML Paper Specifications שנוצרו על ידי Microsoft. הוא פותח כתחליף לפורמט קובץ EMF והוא דומה לפורמט קובץ [PDF](/he/pdf/), אך משתמש ב-XML בפריסה, במראה ובמידע ההדפסה של מסמך. זה, למעשה, מוצדק יותר לומר ש-XPS הוא ניסיון ל-PDF, אבל לא הצליח להשיג מספיק פופולריות בבעלות PDF מסיבות רבות. Microsoft מספקת XPS Document Writer כברירת מחדל מ-Windows 7 ואילך ליצירת קובצי XPS. ניתן להפיק קובצי XPS על ידי בחירת "כותב מסמכים של Microsoft XPS" כמדפסת בזמן הדפסת המסמך.

צופי XPS מגיעים משולבים כחלק מ-Windows Vista, Windows 7, Windows 8 ו-Internet Explorer 6 ואילך. קובצי XPS הופכים לקריאה בלבד ברגע שהם נוצרים. זה מוסיף לביטחון של המשתמש במסמכים שהתקבלו שנשלחו כ-XPS עבור האותנטיות של המסמך. מסמך XPS יכול להכיל עמוד אחד או יותר כפי שהומרו מהמסמך המקורי.

## היסטוריה קצרה ##

מיקרוסופט הגישה את מפרט ה-XPS ל-Ecma International. ביוני 2007, הוקמה הוועדה הטכנית של Ecma 46 (TC46) כדי לפתח תקן המבוסס על מפרטי נייר OpenXPS. Ecma International אישרה את תקן Ecma (ECMA-388) [מפרט XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) ביוני 2009 בעצרת הכללית ה-97.

## פורמט קובץ XPS ##

פורמט XPS מורכב מסימון XML המגדיר את הרכב המסמך ואת המראה החזותי של כל עמוד יחד עם כללי עיבוד לתצוגה או הדפסה של המסמך. הוא שומר את כל המידע כדי ליצור מחדש מסמך בכל מערכת, מה שהופך אותו לבלתי תלוי במשאבים הזמינים במערכת זו. הפורמט הוא בעצם ארכיון ZIP ואם תשנה את שם סיומת הקובץ ל-ZIP, תראה את הקבצים המרכיבים את נתוני המסמך. מסמכים אלה כוללים:

* קבצי דפי מסמך (.fpage) - מכיל תוכן מסמך והגדרות פורמט מסמך. לכל עמוד במסמך XPS יש קובץ FPAGE אחד.
* קובץ הגדרות מסמך (.fdoc) - מאחסן את ההגדרות הכלולות בארכיון XPS.
* קבצי שברי מסמכים (.frag) - מגדיר את ההגדרות עבור קובץ ה-XPS בפועל ולכל עמוד במסמך יש קובץ .frag משלו.

{{< figure src="../XPS-1.png" alt="פורמט קובץ XPS" >}}

קבצים אלה שומרים על תוכן המסמך בצורה כזו שאם, למשל, למישהו אין אותם גופנים מותקנים במחשב שלו, מציג XPS עדיין יציג את הגופנים המקוריים האלה. זה מרמז על הכללת קובץ סימון XML עבור כל אחד מהם:

* עמוד
* טקסט
* גופנים משובצים
* תמונות רסטר
* גרפיקה וקטורית דו מימדית
* ניהול זכויות דיגיטליות

פורמט XPS Document כולל קבוצה מוגדרת היטב של חלקים ויחסים, שכל אחד מהם ממלא מטרה מסוימת במסמך. הפורמט גם מרחיב את תכונות החבילה, כולל חתימות דיגיטליות, תמונות ממוזערות ושזירה.

מסמך XPS טיפוסי נראה כדלקמן וניתן לנתח אותו לאור פורמט קובץ XPS [מפרטים](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="פורמט קובץ XPS" >}}


## הפניות ##

* [מפרט פורמט קובץ XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

