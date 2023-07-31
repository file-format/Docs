{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","קובץ", "פורמט", "סוג קובץ", "הרחבה","מהו קובץ DOCX?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"למד על פורמט קובץ DOCX וממשקי API שיכולים ליצור ולפתוח קובצי DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## מהו קובץ DOCX? ##

DOCX הוא פורמט ידוע עבור מסמכי Microsoft Word. הוצג משנת 2007 עם שחרורו של Microsoft Office 2007, המבנה של פורמט המסמך החדש הזה שונה מבינארי רגיל לשילוב של XML וקבצים בינאריים. ניתן לפתוח קבצי Docx עם Word 2007 וגרסאות רוחביות אך לא עם הגירסאות הקודמות של MS Word התומכות בהרחבות קבצי DOC.

## היסטוריה קצרה ##

לאחר שמיקרוסופט פתחה את המפרטים של פורמט הקובץ DOC, קל היה למתחרותיה לבצע הנדסה לאחור של הפורמט ולספק את אותה תמיכה ביישומים שלהם. בנוסף, התחרות של Open Office בצורת Open Document Format שלה, אילצה את מיקרוסופט לאמץ סטנדרטים פתוחים ורחבים יותר. זה היה בתחילת שנת 2000 כאשר מיקרוסופט החליטה ללכת על השינוי כדי להתאים את התקן עבור **Office Open XML**. מסמכים לפי תקן חדש זה קיבלו [.docx סיומת](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), ה-"X" להיות עבור XML. עד 2007, פורמט הקובץ החדש הזה הפך לחלק מ-Office 2007 והוא ממשיך גם בגרסאות החדשות של Microsoft Office. סוג הקובץ החדש הוסיף יתרונות של גדלי קבצים קטנים, פחות שינויים של שחיתות וייצוג תמונות מעוצבות היטב.

## מפרטי פורמט קובץ DOCX - מידע נוסף

קובץ Docx מורכב מאוסף של קובצי XML הכלולים בתוך ארכיון ZIP. ניתן לצפות בתוכן של מסמך Word חדש על ידי פתיחת התוכן שלו. האוסף מכיל רשימה של קבצי XML המסווגים כ:

* MetaData Files - מכיל מידע על קבצים אחרים הזמינים בארכיון
* מסמך - מכיל את התוכן בפועל של המסמך

### קבצי מטא נתונים ###

Microsoft Word משתמש בקבצים אלה כדי למצוא את הקשר בין קבצים ולאיתור תוכן המסמך. כאשר מחלצים ארכיון מסמכי Word, הוא מכיל מספר קבצים כאלה כמפורט להלן.

#### מערכות יחסים - \_rels/.rels ####

קובץ זה מכיל מידע שאומר ל-MS Word היכן לחפש את תוכן המסמך והפניות אחרות. כל קשר מזוהה על ידי מזהה קשר ייחודי ומציין את קובץ ה-XML שאליו מתייחסים כיעד. קובץ קשרים לדוגמה מוצג כדלקמן:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### סוגי תוכן ####

מסמך יכול להכיל מספר סוגי מדיה בתוכו כמו תמונות, ערכות נושא, אמנות מילים וכו'. ה-[Content_Types].xml מכיל מידע על סוגי מדיה כאלה הקיימים במסמך. התוכן של קובץ XML כזה מוצג כדלקמן:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### הפניות למשאבים - \_rels/document.xml.rels ####

מידע על משאבים, כגון תמונות המוטמעות במסמך, מוזכר בקובץ XML זה.

#### תוכן המסמך הראשי ####

הכוונה היא לקובץ ה-XML הראשי של הארכיון המכיל את תוכן הטקסט של המסמך. תוכן זה מיוצג על ידי מגוון צמתים לפי מפרטי OpenOffice XML. לרוב התוכן של קובץ זה מורכב מפסקאות וטבלאות, אם כי הם יכולים להיות גם צמתים אחרים.

### צמתים בפורמט קובץ ###

הקובץ הראשי document.xml הוא אוסף של צמתים לייצוג התוכן הכולל של קובץ. לכל צומת יש התחלה וסוף שמקיפים או צמתים נוספים או את התוכן. דוגמה פשוטה לקובץ xml כזה היא כדלקמן:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

להלן המידע על חלק מהצמתים הכלולים בקובץ DOCX לייצוג התוכן.

`<w:document> ` - מייצג את אלמנט הבסיס של התוכן הראשי של הקובץ.

`<w:body> ` - מייצג את גוף המסמך שיכול להכיל צמתים רבים אחרים כגון פסקאות, טבלאות וקטעים.

#### פסקאות ####

פסקה היא מחזיק התוכן העיקרי במסמך. זה מיוצג על ידי **<w:p> ** אלמנט בתוך מסמך. פסקה נוספת מורכבת מרוץ אחד או יותר **<w:r> ** שמכיל את הטקסט האמיתי של הפסקה. בנוסף לריצות, פסקאות עשויות להכיל גם רכיבי מסמך אחרים כגון היפר-קישורים, הערות וכו'. מבנה פסקה לדוגמה הוא כפי שמוצג להלן:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## הפניות ##

* [MS - פורמט קובץ DOCX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

