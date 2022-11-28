---
date: 2019-10-11
keywords: sass, .sass, פורמט קובץ sass, כיצד לפתוח קבצי sass, גיליון סגנונות מדהים מבחינה תחבירית, מעבד קדם css, sass
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ Sass
linktitle: Sass
description: "למד על פורמט קבצי Sass וממשקי API שיכולים ליצור ולפתוח קבצי Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## מהו קובץ SASS? ##

Sass (גליונות סגנונות מדהימים מבחינה תחבירית) היא שפת סקריפטים קדם-מעבד. הוא מקומפל לתוך [CSS](/he/web/css/) ומאוחסן עם סיומת .sass. Sass מורכב משני תחבירים, המקור מבוסס על הזחה שמשתמש בסיומת .sass וה-SCSS החדש יותר עם עיצוב בלוק כמו CSS שמשתמש בסיומת .scss.

## למה להשתמש ב-Sass ##

Sass מאוד מועיל בשמירה על סגנונות מכיוון שהוא מספק תכונות רבות כמו הצגת משתנים, קינון, מיקסים, ייבוא ותורשה של בורר שהופכים את העבודה עם סגנונות למהנה.

## כיצד להשתמש בקבצי SASS ##

קובצי SASS אינם כלולים ישירות במסמך [HTML](/he/web/html/) אלא מומרים לקובצי CSS הכלולים בקובצי HTML. אתה יכול להתקין את Sass של המערכת שלך על ידי ביצוע ההוראות הניתנות ב[אתר Sass הרשמי](https://sass-lang.com/install).

ניתן להמיר את Sass ל-CSS על ידי המרת קובץ SASS שכבר שמור או על ידי מעקב אחר שינויים והמרה בזמן שמירת הקובץ. הפקודות עבור שניהם ניתנות להלן.

### המרה פעם אחת ###

הפרמטר הראשון של הפקודה הוא קובץ המקור SASS והפרמטר השני הוא קובץ הפלט CSS.

```cmd
sass main.sass main.css
```

### צפו לשינויים ###

ניתן להריץ את הפקודה לעיל עם דגל *watch* נוסף ששומר על הפקודה פועלת וברגע שמירת קובץ Sass נוצר פלט CSS.

```cmd
sass --watch main.sass main.css
```

## תחביר Sass ##

Sass תומך במשתנים, קינון, mixins, יבוא, תורשה של בורר וכו'. להלן דוגמאות לתכונות אלו.

### משתנים ###

ניתן להשתמש במשתנים כדי להגדיר מידע לשימוש חוזר כגון צבע ראשי או ריפוד עבור כפתור. זה יכול להיות שימושי אם בעתיד תצטרך לשנות את המידע הזה, פשוט תשנה אותו במיקום אחד והוא מתעדכן בכל מקום.

**סאס**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

ניתן לקנן בוררי CSS בדומה להיררכיה של HTML. בדוגמה הבאה, הטווח מקונן בתוך בלוק h1.

**סאס**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

מיקסינים משמשים לקיבוץ מאפיינים דומים המשמשים במספר מקומות. Mixins תומכים גם בפרמטרים.

**סאס**

**הכריז על מיקסין**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**באמצעות מיקסין**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

הרחבה/ירושה יכולה להיות שימושית במקרים שבהם יש צורך לשתף את המאפיינים של בורר אחד עם בורר אחר. בדוגמה למטה, בורר *.error-notice* לוקח את כל המאפיינים של בורר *.error-text* ומוסיף מאפייני גבול וריפוד.

**סאס**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

ייבוא יכול להיות שימושי אם אתה מבנה את הסגנונות שלך לקבצים שונים על סמך פונקציונליות או כל מבנה אחר שאתה עוקב אחריהם. אתה יכול לייבא את כל הקבצים האלה בקובץ SASS ראשי שיומר מאוחר יותר ל-CSS. בזמן הייבוא, אין צורך לציין את סיומת הקובץ בהוראת הייבוא. Sass מרכיב את כל קבצי SASS ישירות. כדי להימנע מקבצי ייבוא להידור ישיר, אתה יכול להפוך אותם לחלקים על ידי הוספת קו תחתון (_) בתחילת שמם. חלקים מיובאים בדומה לקבצי Sass רגילים.

**סאס**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

ל-CSS הפלט יהיו הסגנונות מכל הקבצים המיובאים.

## הפניות ##

- [Sass - ויקיפדיה](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

