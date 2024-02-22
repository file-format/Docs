{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC File - Pro*C Source Code File - Co je soubor .pc a jak jej otevřít?",
  "description" : "Přečtěte si o PC Pro*C Source Code File a jak jej otevřít.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-cs",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Co je to PC soubor?

Soubor PC nebo soubor .pc je soubor zdrojového kódu ProC. ProC je předkompilátor používaný s databázemi Oracle k vkládání příkazů SQL do kódu C nebo C++. Když kompilujete soubor Pro*C, vygeneruje běžný kód C nebo C++ s vloženými příkazy SQL. To vám umožní bezproblémově integrovat operace databáze SQL s vašimi programy v C nebo C++.

Zde je základní příklad toho, jak může soubor Pro*C vypadat:

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

V tomto příkladu mají příkazy SQL předponu EXEC SQL, což znamená, že se jedná o vložené příkazy SQL. Tyto příkazy budou zpracovány předkompilátorem Pro*C při kompilaci souboru a bude vygenerován příslušný kód C pro interakci s databází Oracle.

## Jak otevřít soubor PC?

K otevření souboru na PC obvykle potřebujete textový editor nebo integrované vývojové prostředí (IDE), které podporuje úpravy zdrojového kódu C nebo C++. Zde jsou některé běžné možnosti:

1.  **Textové editory:**
    
- **Poznámkový blok** (Windows)
- **TextEdit** (Mac)
- **gedit** (Linux)
- **Vznešený text**
- **Atom**
- **Visual Studio Code**
2.  **Integrovaná vývojová prostředí (IDE):**
    
- **Eclipse** s CDT (C/C++ Development Tooling)
- **Visual Studio** s Visual C++ nebo Visual Studio Code s rozšířením C++
- **Kód::Blocks**
- **NetBeans** s balíčkem C/C++
  
## Reference
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


