{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC Faylı - Pro*C Mənbə Kodu Faylı - .pc faylı nədir və onu necə açmaq olar?",
  "description" : "PC Pro*C Mənbə Kodu Faylı və onu necə açmaq barədə məlumat əldə edin.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-az",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## PC faylı nədir?

PC faylı və ya .pc faylı ProC mənbə kodu faylıdır. ProC, SQL ifadələrini C və ya C++ kodu daxilində yerləşdirmək üçün Oracle verilənlər bazası ilə birlikdə istifadə edilən ilkin tərtibçidir. Pro*C faylını tərtib etdiyiniz zaman o, daxil edilmiş SQL əmrləri ilə müntəzəm C və ya C++ kodu yaradır. Bu, SQL verilənlər bazası əməliyyatlarını C və ya C++ proqramlarınızla problemsiz şəkildə inteqrasiya etməyə imkan verir.

Pro*C faylının necə görünə biləcəyinə dair əsas nümunə budur:

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

Bu misalda, SQL ifadələrinə daxil edilmiş SQL ifadələri olduğunu göstərmək üçün EXEC SQL ilə prefiks qoyulur. Fayl tərtib edildikdə bu ifadələr Pro*C prekompilyatoru tərəfindən işlənəcək və Oracle verilənlər bazası ilə qarşılıqlı əlaqə yaratmaq üçün müvafiq C kodu yaradılacaq.

## PC faylını necə açmaq olar?

PC faylını açmaq üçün sizə adətən mətn redaktoru və ya C və ya C++ mənbə kodunu redaktə etməyi dəstəkləyən İnteqrasiya edilmiş İnkişaf Mühiti (IDE) lazımdır. Budur bəzi ümumi seçimlər:

1.  **Mətn Redaktorları:**
    
- ** Notepad** (Windows)
- **TextEdit** (Mac)
- **gedit** (Linux)
- **Mükəmməl Mətn**
- **Atom**
- **Visual Studio Kodu**
2.  **İnteqrasiya edilmiş İnkişaf Mühitləri (İDE):**
    
- CDT ilə **Eclipse** (C/C++ İnkişaf Alətləri)
- Visual C++ ilə **Visual Studio** və ya C++ genişləndirilməsi ilə Visual Studio Kodu
- **Kod::Bloklar**
- C/C++ paketi ilə **NetBeans**
  
## İstinadlar
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


