---
date: 2019-10-11
keywords: css, .css, פורמט קובץ css, כיצד לפתוח קבצי css, גיליונות סגנונות מדורגים
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ CSS
linktitle: CSS
description: "למד על פורמט קובץ CSS וממשקי API שיכולים ליצור ולפתוח קובצי CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## מהו קובץ CSS? ##

CSS (Cascading Style Sheets) הם קבצים המתארים כיצד רכיבי HTML מוצגים על המסך, נייר וכו'. עם HTML, אתה יכול לקבל סגנונות מוטבעים או שניתן להגדיר סגנונות בגיליון סגנונות חיצוני. להטמעת הסגנונות, ה-\ <style>\</style> נעשה שימוש בתגים. גיליונות הסגנונות החיצוניים מאוחסנים בקבצים עם סיומת .css. עם ה-CSS החיצוני, אתה יכול לכלול אותו במספר דפי HTML כדי לעדכן את הסגנון של אותם דפים. אפילו קובץ CSS בודד יכול לשמש לעיצוב אתר שלם.

## היסטוריה קצרה ##

CSS1 שוחרר בשנת 1996 עם ברט בוס כמחבר המשותף. קבוצת העבודה של CSS החלה לעבוד על הנושאים שלא טופלו ב-CSS1. זה הביא ליצירת CSS2 בנובמבר 1997 שפורסם כהמלצת W3C ב-12 במאי 1998. גרסה זו הוסיפה תמיכה בהתקנים ספציפיים למדיה כמו מדפסות, גופנים להורדה, טבלאות ומיקום אלמנטים. ביוני 1999, CSS3 הפכה להמלצה של W3C. זה חילק את התיעוד למודולים כאשר לכל מודול היו תכונות הרחבה שהוגדרו ב-CSS2.

## כיצד להשתמש בקבצי CSS ##

כדי להשתמש בקובץ CSS, אתה כולל אותו בחלק הראשי של מסמך ה-HTML. אתה משתמש בתג הקישור כדי לכלול את הקובץ כפי שמוצג להלן.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

התכונה *href* של תג הקישור מכילה את הנתיב לקובץ ה-CSS. על ידי כך, הסגנונות הרלוונטיים הכלולים בקובץ ה-CSS הכלול מוחלים על מסמך ה-HTML.

## תחביר CSS ##

כלל CSS מורכב משני רכיבים, בורר והצהרה. בורר מצביע על אלמנט במסמך HTML. זה יכול להיות תג אלמנט, שם מחלקה, שם מזהה, תגים מרובים המציגים את ההיררכיה וכו'. הצהרה מכילה את הגדרת הסגנון המורכבת מנכס וערך. המאפיין מזהה את המאפיין של האלמנט שברצונך לשנות והערך מגדיר את הערך החדש שלו. לכל כלל CSS יכולים להיות מספר הצהרות. להלן דוגמה לכלל CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

בדוגמה שלמעלה, יש לנו את **h1** כבורר שבוחר את כל תגי ה-h1 במסמך ה-HTML. לכלל יש שתי הצהרות, האחת עבור משקל גופן והשנייה עבור צבע. *משקל גופן* ו-*צבע* הם מאפיינים ו-*700* ו-*יער ירוק* הם הערכים שלהם בהתאמה.

## דוגמה לשימוש ב-CSS ##

להלן מוצג מסמך HTML לדוגמה ואת גיליון הסגנונות המשמש לסגנון אותו. תמונת ההשוואה מתווספת גם כדי להשוות בין מסמכי HTML מעוצבים ופשוטים

### מסמך HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### גיליון סגנונות CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### השוואת פלט ###

הצד השמאלי של התמונה מציג את מסמך ה-HTML ללא הסגנונות שהוחלו והצד הימני מציג את מסמך ה-HTML עם הסגנונות שהוחלו.

{{< figure src="../CssExample.jpg" alt="תמונה לדוגמה" >}}

## הפניות ##

- [CSS - ויקיפדיה](https://en.wikipedia.org/wiki/CSS)

