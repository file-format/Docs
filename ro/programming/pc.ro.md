{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier PC - Fișier cod sursă Pro*C - Ce este fișierul .pc și cum îl deschideți?",
  "description" : "Aflați despre fișierul cod sursă PC Pro*C și despre cum să îl deschideți.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-ro",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Ce este un fișier PC?

Fișierul PC sau un fișier .pc este un fișier cu cod sursă ProC. ProC este un precompilator folosit cu bazele de date Oracle pentru a încorpora instrucțiuni SQL în codul C sau C++. Când compilați fișierul Pro*C, acesta generează cod C sau C++ obișnuit cu comenzi SQL încorporate. Acest lucru vă permite să integrați fără probleme operațiunile bazei de date SQL cu programele dvs. C sau C++.

Iată un exemplu de bază despre cum ar putea arăta fișierul Pro*C:

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

În acest exemplu, instrucțiunile SQL sunt prefixate cu EXEC SQL pentru a indica faptul că sunt instrucțiuni SQL încorporate. Aceste declarații vor fi procesate de precompilatorul Pro*C atunci când fișierul este compilat și va fi generat codul C corespunzător pentru a interacționa cu baza de date Oracle.

## Cum se deschide fișierul PC?

Pentru a deschide un fișier PC, aveți nevoie de obicei de un editor de text sau de un mediu de dezvoltare integrat (IDE) care acceptă editarea codului sursă C sau C++. Iată câteva opțiuni comune:

1.  **Editori de text:**
    
- **Notepad** (Windows)
- **TextEdit** (Mac)
- **gedit** (Linux)
- **Text sublim**
- **Atom**
- **Visual Studio Code**
2.  **Medii de dezvoltare integrate (IDE):**
    
- **Eclipse** cu CDT (C/C++ Development Tooling)
- **Visual Studio** cu Visual C++ sau Visual Studio Code cu extensia C++
- **Cod::Blocuri**
- **NetBeans** cu pachet C/C++
  
## Referințe
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


