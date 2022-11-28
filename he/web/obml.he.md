{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"תבנית קובץ OBML - קובץ דף אינטרנט שמור של Opera Mini",
  "description" :"למד על מהו קובץ OBML וממשקי API שיכולים ליצור ולפתוח קובץ OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## מהו קובץ OBML?

קובץ OBML (Opera Binary Markup Language) הוא גרסה לא מקוונת של דף אינטרנט שנשמר על ידי דפדפן האינטרנט הנייד Opera Mini. זוהי גרסה עצמאית וקומפקטית של קבצי [HTML](/he/web/html/) המכילה את כל רכיבי הדף להצגה במכשירים ספציפיים במצב לא מקוון. פורמט הקובץ OBML שודרג למספר גרסאות כאשר נעשה שימוש ב-OBML15 ו-OBML16 באופן כללי. נקודה חשובה שיש לקחת בחשבון היא שכל גרסת Opera Mini תואמת רק פורמט OBML אחד. לפיכך, שדרוג של Opera Mini ישאיר דפים שנשמרו בעבר קריאים. ניתן להמיר קובצי OBML ל-HTML ו-[PDF](/he/pdf/).

## פורמט קובץ OBML

פורמט הקובץ OBML נשמר בפורמט הקובץ הקנייני של Opera ומפרטי פורמט הקובץ שלו אינם זמינים לציבור. עם זאת, [פורמט OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) עבר הנדסה הפוכה כדי לפענח את המבנה שלו כדלקמן.

### סוגי נתונים OBML

בהתאם לתוצאות הנדסה לאחור, OBML משתמש בסוגים הפרימיטיביים הבאים:

* `בית` - מספר שלם ללא סימן (1 בייט)
* 'קצר' - מספר שלם בסימן (2 בתים, גדול-אנדיאן)
* `בינוני` - מספר שלם בסימן (3 בתים, גדול-אנדיאן)
 * `blob` – { length: short, data: byte[length] }
* `char` - בית המכיל תו ASCII
* `מחרוזת` - כתם המכיל טקסט מקודד UTF-8

### כותרת OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## הפניות

* [פורמט OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

