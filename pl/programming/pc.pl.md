{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik PC - Plik kodu źródłowego Pro*C - Co to jest plik .pc i jak go otworzyć?",
  "description" : "Dowiedz się o pliku kodu źródłowego PC Pro*C i o tym, jak go otworzyć.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-pl",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Co to jest plik komputerowy?

Plik PC lub plik .pc to plik kodu źródłowego ProC. ProC to prekompilator używany z bazami danych Oracle do osadzania instrukcji SQL w kodzie C lub C++. Kiedy kompilujesz plik Pro*C, generuje on zwykły kod C lub C++ z osadzonymi poleceniami SQL. Pozwala to na bezproblemową integrację operacji na bazach danych SQL z programami C lub C++.

Oto podstawowy przykład tego, jak może wyglądać plik Pro*C:

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

W tym przykładzie instrukcje SQL są poprzedzone przedrostkiem EXEC SQL, aby wskazać, że są to wbudowane instrukcje SQL. Instrukcje te zostaną przetworzone przez prekompilator Pro*C podczas kompilacji pliku i wygenerowany zostanie odpowiedni kod C w celu interakcji z bazą danych Oracle.

## Jak otworzyć plik PC?

Aby otworzyć plik PC, zazwyczaj potrzebny jest edytor tekstu lub zintegrowane środowisko programistyczne (IDE), które obsługuje edycję kodu źródłowego C lub C++. Oto kilka typowych opcji:

1.  **Redaktorzy tekstu:**
    
- **Notatnik** (Windows)
- **Edycja tekstu** (Mac)
- **gedit** (Linux)
- **Wzniosły tekst**
- **Atom**
- **Kod Visual Studio**
2.  **Zintegrowane środowiska programistyczne (IDE):**
    
- **Eclipse** z CDT (narzędzia programistyczne C/C++)
- **Visual Studio** z Visual C++ lub Visual Studio Code z rozszerzeniem C++
- **Kod::Bloki**
- **NetBeans** z pakietem C/C++
  
## Bibliografia
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


