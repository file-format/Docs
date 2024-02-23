{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC-fil - Pro*C-källkodsfil - Vad är .pc-fil och hur öppnar man den?",
  "description" : "Lär dig om PC Pro*C källkodsfil och hur du öppnar den.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-sv",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Vad är en PC-fil?

PC-fil eller .pc-fil är en ProC-källkodsfil. ProC är en förkompilator som används med Oracle-databaser för att bädda in SQL-satser i C- eller C++-kod. När du kompilerar Pro*C-fil genererar den vanlig C- eller C++-kod med inbäddade SQL-kommandon. Detta gör att du sömlöst kan integrera SQL-databasoperationer med dina C- eller C++-program.

Här är ett grundläggande exempel på hur Pro*C-filen kan se ut:

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

I det här exemplet har SQL-satser prefixet EXEC SQL för att indikera att de är inbäddade SQL-satser. Dessa uttalanden kommer att bearbetas av Pro*C-förkompilatorn när filen kompileras och lämplig C-kod kommer att genereras för att interagera med Oracle-databasen.

## Hur öppnar man en PC-fil?

För att öppna en PC-fil behöver du vanligtvis en textredigerare eller en Integrated Development Environment (IDE) som stöder redigering av C eller C++ källkod. Här är några vanliga alternativ:

1.  **Textredigerare:**
    
- **Anteckningsblock** (Windows)
- **Textredigering** (Mac)
- **gedit** (Linux)
- **Sublim text**
- **Atom**
- **Visual Studio Code**
2.  **Integrerade utvecklingsmiljöer (IDE):**
    
- **Eclipse** med CDT (C/C++ Development Tooling)
- **Visual Studio** med Visual C++ eller Visual Studio Code med C++-tillägg
- **Kod::Blockar**
- **NetBeans** med C/C++-paket
  
## Referenser
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


