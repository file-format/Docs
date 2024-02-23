{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC-bestand - Pro*C-broncodebestand - Wat is een .pc-bestand en hoe kunt u het openen?",
  "description" : "Lees meer over het PC Pro*C-broncodebestand en hoe u dit kunt openen.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-nl",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Wat is een pc-bestand?

PC-bestand of een .pc-bestand is een ProC-broncodebestand. ProC is een precompiler die wordt gebruikt met Oracle-databases om SQL-instructies in C- of C++-code in te sluiten. Wanneer u het Pro*C-bestand compileert, genereert het reguliere C- of C++-code met ingebedde SQL-opdrachten. Hierdoor kunt u SQL-databasebewerkingen naadloos integreren met uw C- of C++-programma's.

Hier is een eenvoudig voorbeeld van hoe het Pro*C-bestand eruit zou kunnen zien:

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

In dit voorbeeld worden SQL-instructies voorafgegaan door EXEC SQL om aan te geven dat het ingebedde SQL-instructies zijn. Deze instructies worden verwerkt door de Pro*C-precompiler wanneer het bestand wordt gecompileerd en de juiste C-code wordt gegenereerd voor interactie met de Oracle-database.

## Hoe PC-bestand openen?

Om een pc-bestand te openen, hebt u doorgaans een teksteditor of een Integrated Development Environment (IDE) nodig die het bewerken van C- of C++-broncode ondersteunt. Hier zijn enkele veelvoorkomende opties:

1.  **Teksteditors:**
    
- **Kladblok** (Windows)
- **Tekstbewerking** (Mac)
- **gedit** (Linux)
- **Sublieme tekst**
- **Atoom**
- **Visuele studiocode**
2.  **Geïntegreerde ontwikkelomgevingen (IDE's):**
    
- **Eclipse** met CDT (C/C++ ontwikkelingstools)
- **Visual Studio** met Visual C++ of Visual Studio Code met C++-extensie
- **Code::Blokken**
- **NetBeans** met C/C++-pakket
  
## Referenties
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


