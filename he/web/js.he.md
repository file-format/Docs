---
date: 2019-10-11
keywords: פורמט קובץ js, .js, js, כיצד לפתוח קבצי js, קבצי javascript
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ JS
linktitle: JS
description: "למד על פורמט קובץ JS וממשקי API שיכולים ליצור ולפתוח קובצי JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## מהו קובץ JS? ##

JS (JavaScript) הם קבצים המכילים קוד JavaScript לביצוע בדפי אינטרנט. קובצי JavaScript מאוחסנים עם סיומת js. בתוך מסמך [HTML](/he/web/html/), אתה יכול להטביע את קוד ה-JavaScript באמצעות ה-\ <script>\</script> תגיות או כלול קובץ JS. בדומה לקובצי [CSS](/he/web/css/), ניתן לכלול קובצי JS במספר מסמכי HTML לצורך שימוש חוזר בקוד. ניתן להשתמש ב-JavaScript כדי לתפעל את ה-HTML DOM.

## היסטוריה קצרה ##

JavaScript נשלח לראשונה כחלק מדפדפן Navigator בספטמבר 1995 עם השם LiveScript על ידי Netscape. שמה שונה ל-JavaScript שלושה חודשים לאחר מכן. בשנת 1996, מיקרוסופט הנדסה לאחור את המתורגמן של Navigator ליצירת JScript. JScript שוחרר עם Internet Explorer והיה שונה מאוד מ-JavaScript.

Netscape הגישה JavaScript ל-ECMA International שהובילה לשחרור הרשמי של מפרט ה-ECMAScript הראשון בשנת 1997. ECMAScript 2 שוחרר בשנת 1998, ECMAScript 3 בשנת 1999, והעבודה על ECMAScript 4 החלה בשנת 2000 אך מעולם לא הגיעה למימוש.

ג'סי ג'יימס גארט ב-2005 פרסם מאמר לבן שבו טבע את המונח *אייאקס*. זה השתמש ב-JavaScript כשדרת שדרה כדי ליצור יישומי אינטרנט שטענו נתונים ברקע ונמנעו מטעינה מחדש של עמודים מלאים. זה הביא ליצירת ספריות כמו JQuery, אב טיפוס, דוג'ו וכו'.

גוגל הוציאה את דפדפן כרום עם מנוע ה-JavaScript V8 בשנת 2008. בתחילת 2009 בוצע הסכם לשילוב כל העבודה הרלוונטית ולהניע את JavaScript קדימה. זה הביא לשחרור תקן ECMAScript 5 בדצמבר 2009.

## כיצד להשתמש בקבצי JS ##

כדי להשתמש בקובץ JS, אתה כולל אותו במסמך HTML. אתה משתמש בתג הקישור כדי לכלול את הקובץ כפי שמוצג להלן.

```html
<script src="site.js"></script>
```

התכונה *src* של תג *script* מכילה את הנתיב לקובץ JS. על ידי כך, פונקציונליות JS מתווספת למסמך HTML.

## תחביר JS ##

קובצי JavaScript יכולים להכיל משתנים, אופרטורים, פונקציות, תנאים, לולאות, מערכים, אובייקטים וכו'. להלן סקירה קצרה של התחביר של JavaScript.

- כל פקודה מסתיימת בנקודה-פסיק(;).
- השתמש במילת המפתח *var* כדי להצהיר על משתנים.
- תומך באופרטורים אריתמטיים ( + - * / ) לחישוב ערכים.
- הערות בשורה אחת מתווספות עם // והערות מרובות שורות מוקפות ב- /* ו-*/.
- כל המזהים הם תלויי רישיות כלומר *modelNo* ו-*modelno* הם שני משתנים שונים.
- פונקציות מוגדרות באמצעות מילת המפתח *פונקציה*.
- ניתן להגדיר מערכים באמצעות סוגריים מרובעים [].
- JS תומך באופרטורים להשוואה כמו ==, != , >=, !== וכו'.
- ניתן להגדיר שיעורים באמצעות מילת המפתח *class*.

## דוגמה לשימוש ב-JS ##

להלן מוצג קובץ JavaScript לדוגמה לשימוש פשוט.

### מסמך HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### קוד JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## הפניות ##

- [JS - ויקיפדיה](https://en.wikipedia.org/wiki/JavaScript)

