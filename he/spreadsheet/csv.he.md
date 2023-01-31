{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "קובץ", "הרחבה", "פורמט קובץ", "ערכים מופרדים בפסיקים", "גיליון אלקטרוני" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ CSV וממשקי API שיכולים ליצור ולפתוח קובצי CSV.",
  "title" :"פורמט קובץ CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## מהו קובץ CSV?

קבצים עם סיומת .csv (ערכים מופרדים בפסיק) מייצגים קבצי טקסט רגיל המכילים רשומות של נתונים עם ערכים מופרדים בפסיק. כל שורה בקובץ CSV היא רשומה חדשה מקבוצת הרשומות הכלולה בקובץ. קבצים כאלה נוצרים כאשר העברת נתונים מיועדת ממערכת אחסון אחת לאחרת. מכיוון שכל היישומים יכולים לזהות רשומות מופרדות בפסיק, ייבוא של קבצי נתונים כאלה למסד הנתונים נעשה בצורה נוחה מאוד. כמעט כל יישומי הגיליון האלקטרוני כגון Microsoft Excel או OpenOffice Calc יכולים לייבא CSV ללא מאמץ רב. נתונים המיובאים מקבצים כאלה מסודרים בתאים של גיליון אלקטרוני לצורך ייצוג למשתמש.

## היסטוריה קצרה ##

להלן כמה עובדות מהירות על המקור וההיסטוריה של פורמט קובץ CSV.

* 1972 - מהדר IBM Fortran (מורחב ברמה H) תמך בהם תחת OS/360

* 1978 - קלט/פלט מכוון רשימה נתמך על ידי FORTRAN 77 שהשתמש בפסיקים ורווחים למפרידים

* 2005 - CSV תוקן עם [RFC4180](https://tools.ietf.org/html/rfc4180) כסוג תוכן MIME.

* 2013 - הליקויים של RFC4180 טופלו על ידי המלצת W3C

* 2015 - W3C הכינה את הטיוטות הראשונות של המלצות לתקני CSV-metadata, שהחלו כהמלצה בדצמבר 2015

## המר קבצי CSV ##

ניתן להמיר קבצי CSV למספר פורמטים שונים של קבצים באמצעות היישומים שיכולים לפתוח קבצים אלה. לדוגמה, Microsoft Excel יכול לייבא נתונים מפורמט קובץ CSV ולשמור אותם ב-XLS, [XLSX](/he/spreadsheet/xlsx/), [PDF](/he/pdf/), [TXT](/he/word-processing/txt/) , XML ו-[HTML](/he/web/html/) פורמטים של קבצים. באופן דומה, שולחן עבודה אחרים כמו גם שירותים מקוונים מספקים את היכולת לייצא קבצי CSV ל-HTML, ODS ו-[RTF](/he/עיבוד תמלילים/rtf/).

## פורמט קובץ CSV ##

ידוע כי פורמט קובץ CSV מצוין תחת [RFC4180](https://tools.ietf.org/html/rfc4180). זה מגדיר כל קובץ כתואם CSV אם:

* כל רשומה ממוקמת בשורה נפרדת, מופרדת במעבר שורה (CRLF). לדוגמה:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* הרשומה האחרונה בקובץ עשויה להיות בעלת מעבר שורת סיום או לא. לדוגמה:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* ייתכן שתופיע שורת כותרת אופציונלית כשורה הראשונה של הקובץ באותו פורמט כמו שורות רשומות רגילות. כותרת זו תכיל שמות התואמים לשדות בקובץ וצריכה להכיל את אותו מספר שדות כמו הרשומות בשאר הקובץ (יש לציין את נוכחות או היעדר שורת הכותרת באמצעות פרמטר "כותרת" האופציונלי של זה סוג MIME). לדוגמה:
* field_name,field_name,field_name CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* בתוך הכותרת וכל רשומה, עשוי להיות שדה אחד או יותר, מופרדים בפסיקים. כל שורה צריכה להכיל את אותו מספר שדות בכל הקובץ. מרחבים נחשבים לחלק מתחום ואין להתעלם מהם. אסור לעקוב אחרי השדה האחרון ברשומה פסיק. לדוגמה:
* aaa,bbb,ccc
* כל שדה עשוי להיות מוקף במירכאות כפולות או לא (עם זאת תוכנות מסוימות, כגון Microsoft Excel, אינן משתמשות כלל במירכאות כפולות). אם שדות אינם מוקפים במירכאות כפולות, ייתכן שמירכאות כפולות לא יופיעו בתוך השדות. לדוגמה:\
* "aaa","bbb","ccc" CRLF
* zzz,yyy,xxx
* שדות המכילים מעברי שורה (CRLF), מרכאות כפולות ופסיקים צריכים להיות מוקפים במירכאות כפולות. לדוגמה:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* אם משתמשים במירכאות כפולות כדי להקיף שדות, אזי יש לחמוק ממירכאה כפולה המופיעה בתוך שדה על ידי הקדמתו למרכאה כפולה נוספת. לדוגמה:
* "aaa","b""bb","ccc"

עם זאת, לאור השימוש המודרני, המפריד אינו מוגבל לפסיקים בלבד ויכול להיות גם נקודה-פסיק, טאב או רווחים. יישומים כגון Microsoft Excel מספקים אפשרות לציין את תו המפריד לייבוא רשומות מקובץ CSV.

## הפניות

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - ויקיפדיה](https://en.wikipedia.org/wiki/Comma-separated_values)
