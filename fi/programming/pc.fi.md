{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC File - Pro*C Source Code File - Mikä on .pc-tiedosto ja kuinka avata se?",
  "description" : "Lisätietoja PC Pro*C Source Code File -tiedostosta ja sen avaamisesta.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-fi",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Mikä on PC-tiedosto?

PC-tiedosto tai .pc-tiedosto on ProC-lähdekooditiedosto. ProC on esikääntäjä, jota käytetään Oraclen tietokantojen kanssa SQL-lauseiden upottamiseen C- tai C++-koodiin. Kun käännät Pro*C-tiedoston, se luo tavallisen C- tai C++-koodin upotetuilla SQL-komennoilla. Tämän avulla voit integroida saumattomasti SQL-tietokantatoiminnot C- tai C++-ohjelmiin.

Tässä on perusesimerkki siitä, miltä Pro*C-tiedosto voi näyttää:

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

Tässä esimerkissä SQL-käskyjen etuliitteenä on EXEC SQL, mikä osoittaa, että ne ovat upotettuja SQL-käskyjä. Pro*C-esikääntäjä käsittelee nämä lausunnot, kun tiedosto käännetään, ja asianmukainen C-koodi luodaan vuorovaikutukseen Oracle-tietokannan kanssa.

## Kuinka avata PC-tiedosto?

PC-tiedoston avaamiseen tarvitaan yleensä tekstieditori tai Integrated Development Environment (IDE), joka tukee C- tai C++-lähdekoodin muokkaamista. Tässä on joitain yleisiä vaihtoehtoja:

1.  **Tekstieditorit:**
    
- **Muistio** (Windows)
- **Tekstimuokkaus** (Mac)
- **gedit** (Linux)
-**Ylevä teksti**
-**Atomi**
- **Visual Studio Code**
2.  **Integroidut kehitysympäristöt (IDE:t):**
    
- **Eclipse** CDT:llä (C/C++ Development Tooling)
- **Visual Studio** Visual C++:lla tai Visual Studio Code C++-laajennuksella
- **Koodi::Blocks**
- **NetBeans** C/C++-paketilla
  
## Viitteet
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


