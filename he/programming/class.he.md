{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class","what is a class file","how to open a class file", "extension", "file", "class file","class file", ".class extension" , "קובץ כיתה ב-java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Class - פורמט קובץ Java Class",
  "description":"למד על פורמט קובץ Class וממשקי API שיכולים ליצור ולפתוח קבצי Class.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ Class?

**קובץ מחלקה ב-Java** הוא הפלט המהודר של מחלקה [.java](/he/programming/java/) שמבוצעת בפועל על ידי מכונה וירטואלית של Java (JVM). ניתן להפעיל קבצי מחלקה בנפרד וכן יכולים להיות חלק מקובץ [JAR](/he/programming/jar/) כחבילה יחד עם קובצי חבילה אחרים. ניתן ליצור אותם באמצעות הפקודה **`javac`** מממשק שורת הפקודה. חלק מה-Java IDEs כמו [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) ו-NetBeans מספקים קבצי פלט ליצירת .class מ-Java של הפרויקט קבצים.

## פורמט קובץ כיתה

קובץ בכיתה Java מורכב מקוד בתים שהוא קוד ביניים שיופעל על ידי JVM. קובץ מחלקה מורכב מזרם של בתים של 8 סיביות ופריטי נתונים מרובי בייטים מאוחסנים תמיד בסדר גדול.

### מבנה ClassFile

מבנה קובץ הכיתה הוא כפי שמוצג להלן.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
איפה:

* u1 = כמות בת אחד ללא סימן
* u2 = כמות שני בתים ללא סימן
* u4 = כמות של ארבעה בתים ללא סימן

פרטים על מבנה הקובץ ‎.class מוסברים גם ב-Oracle [פורמט קובץ class](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) וניתן להפנות אותם על ידי מפתחים לעיון. סיכום של שדות אלה הוא כדלקמן.

* `קסם` - פריט הקסם מספק את מספר הקסם המזהה את פורמט קובץ הכיתה; יש לו את הערך 0xCAFEBABE.
* `מינור_version`, `major_version` - הערכים של הפריטים minor_version ו-major_version הם מספרי הגרסה המשנית והמג'ורית של קובץ המחלקה הזה.
* `constant_pool_count` - הערך של הפריט constant_pool_count שווה למספר הערכים בטבלת constant_pool פלוס אחד. אינדקס constant_pool נחשב תקף אם הוא גדול מאפס וקטן מ-constant_pool_count, למעט קבועים מסוג ארוך וכפול.
* `constant_pool[]` - ה- constant_pool הוא טבלת מבנים (§4.4) המייצגת קבועי מחרוזת שונים, שמות מחלקות וממשקים, שמות שדות וקבועים אחרים שאליהם מתייחסים בתוך מבנה ClassFile ותתי המבנים שלו. הפורמט של כל ערך בטבלת constant_pool מצוין על ידי בית ה"תג" הראשון שלו.
* `access_flags` - הערך של הפריט access_flags הוא מסכת דגלים המשמשת לציון הרשאות גישה ומאפיינים של המחלקה או הממשק הזה.
* `this_class` - הערך של הפריט this_class חייב להיות אינדקס חוקי בטבלת constant_pool.
* `super_class` - עבור מחלקה, הערך של הפריט super_class חייב להיות אפס או חייב להיות אינדקס חוקי בטבלת constant_pool.
* `interfaces_count` - הערך של הפריט interfaces_count נותן את מספר ממשקי העל הישירים של המחלקה או סוג הממשק הזה.
* `interfaces[]` - כל ערך במערך הממשקים חייב להיות אינדקס חוקי לטבלת constant_pool.
* `fields_count` - הערך של הפריט fields_count נותן את מספר מבני field_info בטבלת השדות.
* `fields[]` - כל ערך בטבלת השדות חייב להיות מבנה field_info המספק תיאור מלא של שדה במחלקה או בממשק זה.
* `methods_count` - הערך של הפריט methods_count נותן את מספר מבני method_info בטבלת המתודות.
* `methods[]` - כל ערך בטבלת המתודות חייב להיות מבנה method_info המספק תיאור מלא של מתודה במחלקה או בממשק זה. אם אף אחד מהדגלים ACC_NATIVE ו-ACC_ABSTRACT לא מוגדר בפריט access_flags של מבנה method_info, מסופקות גם הוראות Java Virtual Machine המיישמות את השיטה.
* `attributes_count` - הערך של הפריט attributes_count נותן את מספר התכונות (§4.7) בטבלת התכונות של מחלקה זו.
* `attributes[]` - כל ערך בטבלת התכונות חייב להיות מבנה attribute_info.




## הפניות

* [פורמט הקובץ של הכיתה](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

