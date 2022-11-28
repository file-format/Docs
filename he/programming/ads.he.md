
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ ADS - פורמט קובץ מפרט Ada",
  "description":"למד מה זה פורמט קובץ ADS עם דוגמה וממשקי API שיכולים ליצור ולפתוח קובצי ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## מהו קובץ ADS?

קובץ ADS הוא קובץ מפרט עבור פרויקט תכנות של עדה. זה דומה למחלקה עבור Java, או צמד הכותרת והיישום במקרה של C++. המפרט הציבורי והפרטי של חבילת Ada מאוחסן בקובץ .ads. הקובץ, .adb, לעומת זאת מכיל את היישום, או גופי Ada. כמו [C++](/he/programming/cpp/), Ada מציעה הפרדה בין מפרטים והטמעות ללא תלות ב-OPP.

ניתן לפתוח קובצי ADS בכל עורך טקסט כגון Microsoft Notepad, Notepad++ ו-Atom.

## פורמט קובץ ADS

קובצי ADS הם בפורמט קובץ טקסט פשוט וניתן לפתוח/לערוך אותם בכל עורך טקסט. ניתן לארגן חבילות עדה לפי היררכיות. ניתן להכריז על יחידת ילד באופן הבא:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## הפניות

* [חבילות עדה](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

