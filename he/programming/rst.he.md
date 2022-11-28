{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ RST- קובץ reStructuredText",
  "description":"למד על פורמט קובץ RST וממשקי API שיכולים ליצור ולפתוח קובצי RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## מהו קובץ RST?

קובץ RST הוא פורמט קובץ תיעוד טכני, המשמש בעיקר בקהילת התכנות של Python. זהו קובץ טקסט שנכתב בשפת הסימון reStructuredText המחיל סגנונות ועיצוב על מסמכי טקסט רגיל ליצירת תיעוד. קובצי RST משתמשים בהערות ובמידע אחר בקוד תוכניות Python כדי ליצור תיעוד טכני של היישום. עם זאת, אלה יכולים להכיל גם טקסט שניתן להמיר לדפי אינטרנט פשוטים ול-[eBooks](/he/ebook/). ניתן להשתמש בעורכי טקסט כגון Github Atom, GNU Emacs (בפלטפורמות שונות), Microsoft Notepad (Windows), Apple TextEdit (Mac) ו-Vim (Linux) לפתיחת קובצי RST.

## פורמט קובץ RST

קובצי RST מכילים קוד שנכתב בשפת סימון reStructuredText. זה חלק מפרויקט Docutils של Python Doc-SIG (Documentation Special Interest Group) המספק סט כלים עבור Python בדומה ל-Javadoc עבור Java. המנתח לפורמט קובץ RST מוטבע ב-Docutils ויכול לחלץ מידע מתוכנות Python לצורך עיצובם לתיעוד תוכנית.

### reStructuredText RST דוגמה

ניקח טקסט לדוגמה שנכתב בפורמט קובץ RST כדלקמן.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

כאשר טקסט זה מוזן למעבד rST כגון Docutils, הפלט הוא כדלקמן.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## התייחסות ##

* [reStructuredText - מאת ויקיפדיה](https://en.wikipedia.org/wiki/ReStructuredText)

