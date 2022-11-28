{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "קובץ", "הרחבה", "פורמט", "Perl", "שפת Perl", "קבצי PL", "תכנות"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ PL וממשקי API שיכולים ליצור ולפתוח קובצי PL.",
  "title" :"קובץ PL - פורמט קובץ סקריפט של Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## מהו קובץ PL?

קובץ עם סיומת .pl הוא קובץ Perl Script שהוא שפת סקריפטים. אלה מורכבים ומופעלים באמצעות תוכנת Perl Interpreter. קובץ סקריפט PL מכיל שורות קוד, משתנים והערות. שפות סקריפטים קשות יחסית
להבין פורמטים אחרים של קבצי תכנות כגון [PHP](/he/programming/php/). ניתן ליצור קבצי PL והם תואמים ל-Windows, macOS ו-Linux.

## היסטוריה קצרה של שפת התסריט של פרל

שפה זו נשמרה לראשונה ב-1987, כך שהקבצים הללו קיבלו את מקורם באותה שנה. בשנת 1989 יצא פרל 2. בהמשך, היא עודכנה ושונתה עד לגרסת 5.35, והגרסה הבאה אמורה לצאת בשנה הבאה.

בכל עדכון, נוספו כלים לגבי הפונקציונליות, הביצועים והמראה של השפה והקבצים. היו שינויים רבים לגבי הגרסאות בשנים אלו. במקור זו הייתה שפת סקריפטים בסיסית, אך כעת היא כוללת גם מודולים רבים אחרים. במקור, זו הייתה שפה פשוטה מאוד, אבל התסריטים של שפה זו היו די קשים להבנה מכיוון שהם היו קומפקטיים.

## מפרטי הרחבת פורמט קובץ Perl

ישנם כמה מאפיינים או מפרטים של קבצי תכנות אלה, חלקם הם כדלקמן:

* הקוד הכלול בקבצים אלה הוא בפורמט טקסט רגיל ומשמש לפיתוח סקריפט
* סקריפט של שרת, ניתוח טקסט וניהול שרת הם ההיבטים העיקריים שהסקריפט של שפה זו מכסה
* תוכניות פופולריות רבות המשויכות לשפה זו הן Active state Active Perl ו-Bare Bones BBEdit (תואמת ל-Mac OS)
* שפה זו נחשבת לשפה ברמה גבוהה
* עבור Win32, ייתכן שהמשתמש יצטרך להתקין הפצה בינארית מקורית של השפה
* זה דורש כמה כלי סקריפטים כדי להפוך לניתנים להפעלה בערכות משאבים שונות של Windows
* Visual Studio .NET היא מסגרת מפורסמת לפיתוח שפות תכנות. הכלי Active State הידוע בשם Visual Perl משמש להוספת Perl לתוך Visual studio
* בקבצים, השורה הראשונה של קוד המקור מתארת את המידע של המתורגמן שבו נעשה שימוש. קבצי PL מתחילים בדרך כלל בשורה **#!/usr/bin/perl** שאומרת למחשב שלך להפעיל את הסקריפט הזה באמצעות מתורגמן Perl המותקן במחשב


## דוגמאות לסקריפט PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

זה יודפס

```
Hello, World
```

### הערה בשורה אחת ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### תגובה מרובת שורות ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### הקצאת משתנה ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### הקצאת משתנה סקלארי ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### פעולות סקלריות פשוטות ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## הפניות ##

- [Python (שפת תכנות) - ויקיפדיה](https://en.wikipedia.org/wiki/Python_(programming_language))

