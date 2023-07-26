{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "קובץ wpl", "הרחבה", "פורמט", "מהו קובץ wpl", "מוזיקה", "פורמט קובץ wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ WPL וממשקי API שיכולים ליצור, להמיר ולפתוח קובצי WPL.",
  "title" :"WPL - קובץ רשימת השמעה של Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## מהו קובץ WPL?

קובץ עם סיומת .wpl מכיל את רשימת ההשמעה של השירים שיופעלו ב-Microsoft Windows Media Player. קבצים אלה נוצרים בדרך כלל על ידי משתמשים עבור אוספי הווידאו והשמע שלהם. התוכן שנכתב בקובץ WPL, הוא רק נתיבים או מיקומים של ספרייה עבור קובצי המולטימדיה שנבחרו על ידי היוצר של קובץ ה-wpl, כך שאפליקציית נגן המדיה יכולה למצוא ולהשמיע מיד את תוכן המולטימדיה ממיקומי הספרייה שלהם.

## פורמט קובץ WPL

WPL (רשימת השמעה של Windows Media Player) הוא פורמט קובץ קנייני המשמש ב-Microsoft Windows Media Player גרסאות 9 ומעלה. זהו פורמט קובץ מחשב המאחסן רשימות השמעה מולטימדיה. כברירת מחדל, רשימת ההשמעה נשמרת עם סיומת .wpl (רשימת השמעה של Windows Media Player). אתה יכול להשתמש בתוסף [.m3u](/he/audio/m3u/) במקום זאת, אם ברצונך להפעיל את תקליטורי הנתונים שלך במכשיר שאינו תומך בתוסף זה. הרכיבים של קובץ WPL מיוצגים בפורמט XML.

האלמנט ברמה העליונה "smil" מציין שרכיבי הקובץ עוקבים אחר המבנה של SMIL (Synchronized Multimedia Integration Language). הקובץ נוצר ונשמר עם סיומת .wpl וסוג MIME שלו הוא application/vnd.ms-wpl.

### דוגמה של WPL

הנה דוגמה לקובץ wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## הפניות ##

* [MPEG-1 Audio Layer II - מאת ויקיפדיה](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

