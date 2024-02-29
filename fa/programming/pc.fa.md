{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل PC - فایل کد منبع Pro*C - فایل pc چیست و چگونه آن را باز کنیم؟",
  "description" : "با فایل کد منبع PC Pro*C و نحوه باز کردن آن آشنا شوید.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-fa",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## فایل PC چیست؟

فایل PC یا یک فایل pc. یک فایل کد منبع ProC است. ProC یک پیش کامپایلر است که با پایگاه داده های Oracle برای جاسازی دستورات SQL در کدهای C یا C++ استفاده می شود. هنگامی که فایل Pro*C را کامپایل می کنید، کدهای C یا C++ معمولی را با دستورات SQL تعبیه شده تولید می کند. این به شما امکان می دهد تا به طور یکپارچه عملیات پایگاه داده SQL را با برنامه های C یا C ++ خود یکپارچه کنید.

در اینجا مثالی اساسی از آنچه ممکن است فایل Pro*C به نظر برسد آورده شده است:

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

در این مثال، دستورات SQL با EXEC SQL پیشوند داده می‌شوند تا نشان دهند که عبارت‌های SQL تعبیه‌شده هستند. هنگامی که فایل کامپایل می شود، این عبارات توسط پیش کامپایلر Pro*C پردازش می شود و کد C مناسب برای تعامل با پایگاه داده اوراکل تولید می شود.

## چگونه فایل کامپیوتر را باز کنیم؟

برای باز کردن یک فایل رایانه شخصی، معمولاً به یک ویرایشگر متن یا یک محیط توسعه یکپارچه (IDE) نیاز دارید که از ویرایش کد منبع C یا C++ پشتیبانی کند. در اینجا چند گزینه رایج وجود دارد:

1.  **ویرایشگرهای متن:**
    
- ** دفترچه یادداشت ** (ویندوز)
- **TextEdit** (Mac)
- **gedit** (لینوکس)
- **متن عالی**
- **اتم**
- **کد ویژوال استودیو**
2.  **محیط های توسعه یکپارچه (IDE):**
    
- **Eclipse** با CDT (ابزار توسعه C/C++)
- **Visual Studio** با Visual C++ یا Visual Studio Code با پسوند C++
- **کد::Blocks**
- **NetBeans** با بسته C/C++
  
## منابع
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


