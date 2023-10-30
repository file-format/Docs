{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "קובץ CJS - קובץ קוד CommonJS",
  "description":"מהו קובץ .cjs וכיצד פותחים אותו?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## מהו קובץ CJS?

קובץ CommonJS (CJS) הוא קובץ המכיל קוד JavaScript שנכתב בתחביר CommonJS. CommonJS היא מערכת מודולים המיועדת לעבוד בסביבות מעבר לדפדפני אינטרנט חזיתיים, והיא משמשת לעתים קרובות בסביבות JavaScript בצד השרת, כמו Node.js.

## פורמט קובץ CJS - מידע נוסף

קובצי CJS נכתבים בתחביר CommonJS וניתן לערוך אותם בכל עורך טקסט כגון Microsoft Notepad או Apple TextEdit. מודולי CommonJS מאוחסנים בדרך כלל בקבצים נפרדים ונועדו לכלול קוד מודולרי לארגון ותחזוקה טובים יותר. מודולים אלה משתמשים בפונקציה require כדי לייבא תלות ובאובייקט module.exports או exports כדי לחשוף ערכים ופונקציות שניתן להשתמש בהם בחלקים אחרים של הקוד.

## דוגמה לקוד CJS

למודולי CommonJS יש תחביר ומבנה ספציפיים הכוללים תכונות כגון פונקציית require לייבוא מודולים אחרים וה-modul.exports או ייצוא אובייקטים לייצוא ערכים, פונקציות או אובייקטים ממודול. מודולים אלה משמשים ללקיחת והפרדה של חלקי קוד, מה שמקל על ניהול ותחזוקה של בסיסי קוד JavaScript גדולים. הנה דוגמה בסיסית של מודול CommonJS:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## הפניות

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)