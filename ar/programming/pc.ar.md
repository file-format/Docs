{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ملف الكمبيوتر الشخصي - ملف التعليمات البرمجية المصدر Pro*C - ما هو ملف .pc وكيفية فتحه؟",
  "description" : "ملف الكمبيوتر الشخصي - ملف التعليمات البرمجية المصدر Pro*C - ما هو ملف .pc وكيفية فتحه؟",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## ما هو ملف الكمبيوتر؟

ملف PC أو ملف .pc هو ملف التعليمات البرمجية المصدر ProC. ProC هو مترجم مسبق يستخدم مع قواعد بيانات Oracle لتضمين عبارات SQL داخل كود C أو C++. عندما تقوم بتجميع ملف Pro*C، فإنه يقوم بإنشاء كود C أو C++ عادي باستخدام أوامر SQL المضمنة. يتيح لك ذلك دمج عمليات قاعدة بيانات SQL بسلاسة مع برامج C أو C++ الخاصة بك.
فيما يلي مثال أساسي لما قد يبدو عليه ملف Pro*C:

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

في هذا المثال، تكون عبارات SQL مسبوقة بـ EXEC SQL للإشارة إلى أنها عبارة عن عبارات SQL مضمنة. ستتم معالجة هذه البيانات بواسطة برنامج التحويل البرمجي المسبق Pro*C عند تجميع الملف وسيتم إنشاء رمز C المناسب للتفاعل مع قاعدة بيانات Oracle.
## كيفية فتح ملف الكمبيوتر؟

لفتح ملف كمبيوتر شخصي، تحتاج عادةً إلى محرر نصوص أو بيئة تطوير متكاملة (IDE) تدعم تحرير التعليمات البرمجية المصدر لـ C أو C++. فيما يلي بعض الخيارات الشائعة:

1.  ** محرري النصوص: **
    
- **المفكرة** (ويندوز)
- **تحرير النص** (ماك)
- **تحرير** (لينكس)
- ** نص سامية **
- **ذرة**
- **كود فيجوال ستوديو**
2.  **بيئات التطوير المتكاملة (IDEs):**
    
- **Eclipse** مع CDT (أدوات تطوير C/C++)
- **Visual Studio** مع Visual C++ أو Visual Studio Code مع ملحق C++
- **الكود::كتل**
- **NetBeans** مع حزمة C/C++
  
## مراجع
* [برو*C](https://en.wikipedia.org/wiki/Pro*C)