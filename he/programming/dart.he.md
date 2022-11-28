---
date: 2019-10-11
keywords: dart, .dart, פורמט קובץ dart, קובץ dart, כיצד להפעיל קבצי dart, סיומת .dart
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ Dart
linktitle: Dart
description: "למד על פורמט קובץ Dart וממשקי API שיכולים ליצור ולפתוח קובצי Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## מהו קובץ Dart? ##

קובץ Dart מכיל את קוד המקור של שפת התכנות Dart שהיא שפת תכנות מותאמת ללקוח שפותחה על ידי גוגל המשמשת לבניית אפליקציות למובייל, שולחן עבודה, אינטרנט, Iot (Internet of things) וכו'. Dart היא שפה מונחה עצמים עם תחביר דומה ל-C. Dart ניתן להידור ל-JavaScript או לקוד מקורי. אתה יכול להפעיל את קבצי Dart בדפדפן אינטרנט מפורסם בדיוק כמו שאתה יכול להפעיל קובץ javascript. כלי שורת פקודה המכונה Dart Virtual Machine שמגיע עם Dart SDK can משמש גם כדי להדר ולהפעיל את קבצי Dart.

## היסטוריה קצרה ##

פרויקט Dart הוקם על ידי לארס בק וקספר לונד והגרסה הראשונה שוחררה ב-14 בנובמבר 2013. בהתחלה, הדארט ספג ביקורת על פיצול האינטרנט עקב התוכניות לכלול Dart VM ב-Google Chrome. התוכניות הללו בוטלו ודארט התמקדה בהידור ל-JavaScript עם שחרורו של גרסה 1.9 ב-2015.

Dart 2.0 שוחרר באוגוסט 2018, בו הוצגה התוסף dart2native שהידור קוד Dart לפלטפורמות Linux, Windows, macOS מקוריות. הרחבה זו אפשרה קובצי הפעלה עצמאיים שבגללם ה-Dart SDK לא נדרש להריץ אפליקציות Dart בפלטפורמות אלו. הרחבה זו משולבת גם עם Flutter המאפשרת ליצור אפליקציות חוצות פלטפורמות.

ECMA תיקנן את Dart עם המהדורה הראשונה ביולי 2014 והמהדורה השנייה בדצמבר 2014.


## כיצד להפעיל/להפעיל קוד Dart ##

קוד Dart יכול לפעול בדרכים הבאות:

- **מורכב כ-JavaScript**:</br> קוד Dart מקומפל ל-JavaScript באמצעות המהדר dart2js. קוד ה-JavaScript המהודר תואם לכל דפדפני האינטרנט הגדולים.
- **עצמאי**:</br> ערכת פיתוח התוכנה של Dart (SDK) נשלחת עם Dart VM עצמאי המאפשר הפעלת קוד Dart בממשק שורת הפקודה. Dart מגיעה עם ספרייה סטנדרטית מלאה המאפשרת למשתמשים לכתוב אפליקציות פונקציונליות במלואן.
- **הידור מראש (AOT)**:</br> ניתן להרכיב קוד Dart AOT לקוד מכונה המאפשר לבנות אפליקציות לנייד עם Flutter.
- **יליד**:</br> עם המהדר dart2native, ניתן להרכיב קוד Dart לקובצי הפעלה עצמאיים שיכולים לפעול ב-Windows, Linux ו-macOS.

## פורמט קובץ Dart ##

Dart היא שפה מונחית עצמים בסגנון C התומכת בממשקים, מיקסינים, מחלקות מופשטות, גנריות משוכללות וממשק טיפוס.

### תחביר ###

להלן כמה דוגמאות לתחביר Dart.

#### הדפס לקונסולה ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### לולאות ומערכים ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

#### פונקציות ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### שיעורים ####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### מיקסינס ####

מיקסינים הם מחלקות רגילות שמהן נוכל לשאול שיטות/משתנים מבלי לרשת אותם. זה נעשה על ידי שימוש במילת המפתח *"עם"*.

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## הפניות ##

- [Dart (שפת תכנות) - ויקיפדיה](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [חץ](https://dart.dev/)

