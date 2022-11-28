---
date: 2019-10-11
keywords: scss, .scss, פורמט קובץ scss, כיצד לפתוח קבצי scss, גיליון סגנונות מדהים מבחינה תחבירית, מעבד קדם css, sass
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ SCSS - גיליון סגנונות מדורג של Sass
linktitle: SCSS
description: "למד על פורמט קבצי SCSS וממשקי API שיכולים ליצור ולפתוח קובצי SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## מהו קובץ SCSS? ##

SCSS הוא התחביר השני של Sass (Syntactically Awesome Stylesheet) המשתמש בסוגריים במקום הזחות. SCSS תוכנן בצורה כזו שקובץ CSS3 חוקי הוא גם קובץ SCSS חוקי. קבצי SCSS מאוחסנים עם סיומת .scss.

## למה להשתמש ב-SCSS ##

ככל שהעיצובים של אתרי אינטרנט הופכים מורכבים וכתוצאה מכך נוצרים קבצי [CSS](/he/web/css/) גדולים. קבצים כאלה קשים יותר לתחזוקה. כאן נכנס לתמונה SCSS. SCSS מציג משתנים, קינון, מיקסים, ייבוא ותורשה של בורר בפיתוח CSS. התוספות הללו הופכות את העבודה עם עיצוב למהנה הרבה יותר.

## כיצד להשתמש בקבצי SCSS ##

קובצי SCSS אינם כלולים ישירות במסמך [HTML](/he/web/html/) כמו CSS. במקום זאת, קבצי SCSS מומרים לקובצי CSS הכלולים בקובצי HTML. כדי להתקין SCSS במערכת שלך, עקוב אחר ההוראות הניתנות ב[אתר Sass הרשמי](https://sass-lang.com/install).
כדי להמיר SCSS ל-CSS, אתה יכול להמיר קובץ SCSS שכבר שמור או לצפות בשינויים ולהמיר בזמן שהקובץ נשמר. הפקודות עבור שניהם ניתנות להלן.

### המרה פעם אחת ###

הפרמטר הראשון הוא קובץ ה-SCSS המקור והפרמטר השני הוא קובץ הפלט CSS.

```cmd
sass main.scss main.css
```

### צפו לשינויים ###

לפקודה יש דגל נוסף *watch** ששומר על הפקודה פועלת וברגע שקובץ ה-SCSS נשמר, נוצר פלט CSS.

```cmd
sass --watch main.scss main.css
```

## תחביר SCSS ##

SCSS תומך במשתנים, קינון, mixins, יבוא, תורשה של בורר וכו'. להלן דוגמאות לתכונות אלו.

### משתנים ###

על ידי שימוש במשתנים, ניתן להגדיר מידע לשימוש חוזר כגון צבע ראשי או צבע רקע עבור כפתור השמירה. זה שימושי אם אתה צריך לשנות את המידע הזה, אתה פשוט משנה אותו במיקום אחד והוא מתעדכן בכל מקום שבו נעשה בו שימוש.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS שנוצר**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### קינון ###

אתה יכול לקנן את בוררי ה-CSS בדומה להיררכיה של HTML. בדוגמה שניתנה להלן, הטווח מקונן בתוך בלוק h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS שנוצר**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### מיקסינים ###

ניתן להשתמש במיקסינים כדי לקבץ מאפיינים דומים המשמשים יחד במספר מקומות. אתה יכול גם להעביר פרמטרים למיקסינים.

**SCSS**

**הכריז על מיקסין**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**באמצעות מיקסין**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**CSS שנוצר**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### הארך ###

הרחבה/ירושה שימושית במקרים שבהם יש צורך לשתף את המאפיינים של בורר אחד עם בורר אחר. בדוגמה למטה, בורר *.error-notice* לוקח את כל המאפיינים של בורר *.error-text* ומוסיף מאפייני גבול וריפוד.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**CSS שנוצר**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### ייבוא ###

ייבוא יכול להיות שימושי בהפרדת חששות. ניתן לחלק את הסגנונות בצורה כזו שסגנונות הכותרות נמצאים בקובץ נפרד, סגנונות הכותרות בקובץ נפרד, כל משתני הצבע המשמשים בסגנונות יכולים להיות בקובץ נפרד וכו'. באמצעות טכניקה זו, סגנונות נשארים מאורגנים. אתה פשוט מייבא את הקבצים לקובץ ה-SCSS הראשי שלך כפי שמוצג בדוגמה למטה. אין צורך לציין את סיומת הקובץ בהוראת הייבוא. Sass מרכיב את כל קבצי ה-SCSS ישירות. כדי להימנע מקבצי ייבוא להידור ישיר, אתה יכול להפוך אותם לחלקים על ידי הוספת קו תחתון (_) לפני שמם. אתה יכול לייבא חלקים בדומה לקבצי SCSS רגילים ללא קו תחתון.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

ל-CSS הפלט יהיו הסגנונות מכל הקבצים המיובאים.

## הפניות ##

- [SCSS - ויקיפדיה](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

