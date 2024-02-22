{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Файл PC - файл вихідного коду Pro*C - що таке файл .pc і як його відкрити?",
  "description" : "Дізнайтеся про файл вихідного коду PC Pro*C і як його відкрити.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-uk",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Що таке файл ПК?

Файл PC або файл .pc є файлом вихідного коду ProC. ProC — це прекомпілятор, який використовується з базами даних Oracle для вбудовування операторів SQL у код C або C++. Коли ви компілюєте файл Pro*C, він генерує звичайний код C або C++ із вбудованими командами SQL. Це дозволяє бездоганно інтегрувати операції з базою даних SQL у ваші програми C або C++.

Ось основний приклад того, як може виглядати файл Pro*C:

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

У цьому прикладі оператори SQL мають префікс EXEC SQL, щоб вказати, що вони є вбудованими операторами SQL. Ці оператори будуть оброблені прекомпілятором Pro*C під час компіляції файлу, і буде створено відповідний код C для взаємодії з базою даних Oracle.

## Як відкрити файл ПК?

Щоб відкрити файл ПК, зазвичай потрібен текстовий редактор або інтегроване середовище розробки (IDE), яке підтримує редагування вихідного коду C або C++. Ось кілька типових варіантів:

1.  **Текстові редактори:**
    
- **Блокнот** (Windows)
- **TextEdit** (Mac)
- **gedit** (Linux)
- **Високий текст**
- **Атом**
- **Код Visual Studio**
2.  **Інтегровані середовища розробки (IDE):**
    
- **Eclipse** з CDT (інструменти розробки C/C++)
- **Visual Studio** з Visual C++ або Visual Studio Code з розширенням C++
- **Код::Блоки**
- **NetBeans** із пакетом C/C++
  
## Список літератури
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


