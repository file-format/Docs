{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Файл ПК — файл исходного кода Pro*C — что такое файл .pc и как его открыть?",
  "description" : "Узнайте о файле исходного кода PC Pro*C и о том, как его открыть.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-ru",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## .PC вариант №

Файл ПК или файл .pc представляет собой файл исходного кода ProC. ProC — это прекомпилятор, используемый с базами данных Oracle для встраивания операторов SQL в код C или C++. Когда вы компилируете файл Pro*C, он генерирует обычный код C или C++ со встроенными командами SQL. Это позволяет вам легко интегрировать операции с базой данных SQL с вашими программами на C или C++.

Вот базовый пример того, как может выглядеть файл Pro*C:

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

В этом примере инструкции SQL имеют префикс EXEC SQL, чтобы указать, что они являются встроенными инструкциями SQL. Эти операторы будут обработаны прекомпилятором Pro*C при компиляции файла и будет сгенерирован соответствующий код C для взаимодействия с базой данных Oracle.

## Как открыть файл ПК?

Чтобы открыть файл ПК, вам обычно нужен текстовый редактор или интегрированная среда разработки (IDE), которая поддерживает редактирование исходного кода C или C++. Вот несколько распространенных вариантов:

1.  **Текстовые редакторы:**
    
- **Блокнот** (Windows)
- **TextEdit** (Mac)
- **gedit** (Linux)
- **Великолепный текст**
- **Атом**
- **Код Visual Studio**
2.  **Интегрированные среды разработки (IDE):**
    
- **Eclipse** с CDT (средства разработки C/C++)
- **Visual Studio** с Visual C++ или Visual Studio Code с расширением C++.
- **Код::Блоки**
- **NetBeans** с пакетом C/C++.
  
## Рекомендации
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


