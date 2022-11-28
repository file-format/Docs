
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript Byte Code File",
  "description":"למד מה זה פורמט קובץ ABC עם דוגמה וממשקי API שיכולים ליצור ולפתוח קובצי ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## מהו קובץ ABC?

קובץ עם סיומת .abc הוא קובץ ActionScript Byte Code שנוצר על ידי מהדר Flash כתוצאה מהידור של קובצי הסקריפט של ActionScript. קוד הבתים הכלול בקובץ ABC מבוצע על ידי ActionScript Virtual Machine (AVM ו-AVM2). קוד הבתים מורכב מנתונים קבועים, הוראות מערך ההוראות של AVM2 וסוגים שונים של מטא נתונים. כאשר קובץ ABC נטען לתוך AVM או AVM2, הוא עובר אימות. אם הוא אינו תואם את הסקירה הכללית של AVM2, הוא נדחה. ניתן לפתוח קבצי ABC ב-Adobe Flash Player שהופסק מזמן.

## פורמט קובץ ABC - מידע נוסף

קבצי ABC נשמרים על דיסק בפורמט קובץ בינארי הניתנים לקריאה על ידי מכונות וירטואליות AVM או AVM2. מבנה הקבצים הפנימי שלו מייצג בלוק קוד בר הפעלה עם כל הנתונים הקבועים שלו, מתארי הסוג, הקוד והמטא נתונים.

## מבנה קובץ ABC

מבנה קובץ ABC הוא כפי שמוצג להלן.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### שדות קובץ ABC

|שם שדה|תיאור|
---|---|
|minor_version, major_version|הערכים של major_version ו-minor_version הם מספרי הגרסה הראשית והמינורית של פורמט abcFile.|
|constant_pool|ה-constant_pool הוא מבנה באורך משתנה המורכב ממספרים שלמים, כפולים, מחרוזות, מרחבי שמות, קבוצות מרחבי שמות ורב-שמות.|
|method_count, method|הערך ofmethod_count הוא מספר הערכים במערך המתודה. כל ערך במערך המתודה הוא מבנה method_info באורך משתנה.|
|metadata_count, metadata|הערך של metadata_count הוא מספר הערכים במערך המטא נתונים. כל ערך מטא נתונים הוא metadata_infostructure הממפה שם לקבוצה של ערכי מחרוזת. |
|class_count, instance, class|הערך של class_count הוא מספר הערכים במערך המופע והמחלקה. |
|script_count, script|הערך של script_count הוא מספר הערכים במערך הסקריפטים. כל ערך סקריפט הוא מבנה script_info המגדיר את המאפיינים של סקריפט בודד בקובץ זה. |
|method_body_count, method_body|הערך של method_body_count הוא מספר הערכים במערך method_body. כל method_bodyentry מורכב ממבנה method_body_info באורך משתנה המכיל את ההוראות עבור שיטה או פונקציה בודדת.|

## הפניות

* [ABC חזק (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

