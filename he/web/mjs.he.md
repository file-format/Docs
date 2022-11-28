{
  "date" : "2021-07-20",
  "keywords" :["MJS", "File", "Extension", "File Format", "File Extension", "Node.js ES Module File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES Module Javascript File",
  "description" :"למד על מהו קובץ MJS וממשקי API שיכולים ליצור ולפתוח קובץ MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## מהו קובץ MJS?

קובץ עם סיומת .mjs הוא קובץ קוד מקור JavaScript המשמש כמודול ECMA (ECMAScript Module) ביישומי Node.js. מערכת המודול natvie של Node.js היא CommonJS המשמשת לפיצול הקוד בקבצים שונים כדי לשמור על הקוד [JS](/he/web/js/) מסודר. MJS היא הדרך היחידה שבה משתמש Node.js כדי לזהות אם המודול הוא CommonJS או ES6. מודולי ECMAScript הם פורמטים סטנדרטיים לאריזת קוד JavaScript לשימוש חוזר. ניתן לפתוח קבצי MJS בעורכי טקסט כגון Atom, Vim, Apple xCode, Microsoft Visual Studio ו-Notepad.

## פורמט קובץ MJS - מידע נוסף

קבצי MJS נשמרים בדיסק כפורמט טקסט רגיל בתחביר JavaScript. ניתן לפתוח אותם בכל עורך טקסט והם ניתנים לקריאה אנושית. מאז 2018, כמעט כל הדפדפנים הגדולים תומכים כעת במודולי ES.

## הבדלים בין מודולי ES לבין CommonJS

אז מה מייחד קבצי MJS מקבצי JS רגילים? ניתן לסכם את ההבדל בין מודולי ES ל-CommonJS כדלקמן:

* אין צורך, ייצוא או module.exports
* אין \__שם קובץ או \__שם קובץ
* אין טעינת מודול JSON
* אין טעינת מודול מקורי
* אין צורך. לפתור
* אין NODE_PATH
* אין צורך. הרחבות
* אין require.cache

## הפניות

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [הבדל בין JS ל-MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

