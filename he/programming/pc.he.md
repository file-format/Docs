{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "קובץ PC - קובץ קוד מקור Pro*C - מהו קובץ .pc וכיצד פותחים אותו?",
  "description" : "למד על קובץ קוד המקור של PC Pro*C וכיצד לפתוח אותו.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-he",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## מהו קובץ PC?

קובץ PC או קובץ .pc הוא קובץ קוד מקור של ProC. ProC הוא Precompiler המשמש עם מסדי נתונים של Oracle כדי להטמיע הצהרות SQL בתוך קוד C או C++. כאשר אתה קומפילציה של קובץ Pro*C, הוא יוצר קוד C או C++ רגיל עם פקודות SQL משובצות. זה מאפשר לך לשלב בצורה חלקה פעולות מסד נתונים של SQL עם תוכניות C או C++ שלך.

הנה דוגמה בסיסית לאיך יכול להיראות קובץ Pro*C:

```
#include <stdio.h>
#include <sqlca.h>

EXEC SQL INCLUDE sqlca;

int main() {
    EXEC SQL BEGIN DECLARE SECTION;
    int emp_id;
    char emp_name[50];
    EXEC SQL END DECLARE SECTION;

    /* Connect to database */
    EXEC SQL CONNECT :user IDENTIFIED BY :password;

    /* Fetch employee details */
    EXEC SQL SELECT employee_id, employee_name INTO :emp_id, :emp_name FROM employees WHERE employee_id = :input_id;

    /* Print fetched details */
    printf("Employee ID: %d\n", emp_id);
    printf("Employee Name: %s\n", emp_name);

    /* Disconnect from database */
    EXEC SQL COMMIT WORK RELEASE;
    return 0;
}
```

בדוגמה זו, קידומת של משפטי SQL עם EXEC SQL כדי לציין שהן הצהרות SQL מוטמעות. הצהרות אלו יעובדו על ידי Pro*C precompiler כאשר הקובץ יודר וייווצר קוד C מתאים לאינטראקציה עם מסד הנתונים של Oracle.

## איך פותחים קובץ PC?

כדי לפתוח קובץ PC, אתה בדרך כלל צריך עורך טקסט או סביבת פיתוח משולבת (IDE) התומכת בעריכת קוד מקור C או C++. להלן מספר אפשרויות נפוצות:

1.  **עורכי טקסט:**
    
- **פנקס רשימות** (Windows)
- **עריכת טקסט** (Mac)
- **gedit** (לינוקס)
- **טקסט נשגב**
- **אטום**
- **קוד סטודיו ויזואלי**
2.  **סביבות פיתוח משולבות (IDEs):**
    
- **Eclipse** עם CDT (כלי פיתוח C/C++)
- **Visual Studio** עם Visual C++ או Visual Studio Code עם סיומת C++
- **קוד::בלוקים**
- **NetBeans** עם חבילת C/C++
  
## הפניות
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


