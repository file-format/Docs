{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC failas - Pro*C šaltinio kodo failas - Kas yra .pc failas ir kaip jį atidaryti?",
  "description" : "Sužinokite apie PC Pro*C šaltinio kodo failą ir kaip jį atidaryti.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Kas yra kompiuterio failas?

PC failas arba .pc failas yra ProC šaltinio kodo failas. ProC yra išankstinis kompiliatorius, naudojamas su Oracle duomenų bazėmis SQL sakiniams įterpti į C arba C++ kodą. Kai kompiliuojate Pro*C failą, jis generuoja įprastą C arba C++ kodą su įterptomis SQL komandomis. Tai leidžia sklandžiai integruoti SQL duomenų bazės operacijas su C arba C++ programomis.

Štai pagrindinis pavyzdys, kaip gali atrodyti Pro*C failas:

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

Šiame pavyzdyje SQL sakiniai yra su EXEC SQL priešdėliu, nurodant, kad jie yra įterptieji SQL sakiniai. Šiuos teiginius apdoros Pro*C išankstinis kompiliatorius, kai bus sukompiliuotas failas, ir bus sugeneruotas atitinkamas C kodas sąveikai su Oracle duomenų baze.

## Kaip atidaryti kompiuterio failą?

Norint atidaryti kompiuterio failą, paprastai reikia teksto rengyklės arba integruotos kūrimo aplinkos (IDE), kuri palaiko C arba C++ šaltinio kodo redagavimą. Štai keletas įprastų parinkčių:

1.  **Teksto redaktoriai:**
    
– **Notepad** (Windows)
– **Teksto redagavimas** (Mac)
- **gedit** (Linux)
- **Pakilnus tekstas**
-**Atomas**
- **Visual Studio Code**
2.  **Integruotos kūrimo aplinkos (IDE):**
    
- **Eclipse** su CDT (C/C++ kūrimo įrankiai)
- **Visual Studio** su Visual C++ arba Visual Studio Code su C++ plėtiniu
- **Kodas::Blocks**
- **NetBeans** su C/C++ paketu
  
## Nuorodos
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


