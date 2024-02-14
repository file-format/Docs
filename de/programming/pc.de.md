{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC-Datei – Pro*C-Quellcodedatei – Was ist eine .pc-Datei und wie öffnet man sie?",
  "description" : "PC-Datei – Pro*C-Quellcodedatei – Was ist eine .pc-Datei und wie öffnet man sie?",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Was ist eine PC-Datei?

Eine PC-Datei oder eine .pc-Datei ist eine ProC-Quellcodedatei. ProC ist ein Precompiler, der mit Oracle-Datenbanken verwendet wird, um SQL-Anweisungen in C- oder C++-Code einzubetten. Wenn Sie eine Pro*C-Datei kompilieren, wird regulärer C- oder C++-Code mit eingebetteten SQL-Befehlen generiert. Dadurch können Sie SQL-Datenbankoperationen nahtlos in Ihre C- oder C++-Programme integrieren.

Hier ist ein einfaches Beispiel dafür, wie eine Pro*C-Datei aussehen könnte:

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

In diesem Beispiel wird den SQL-Anweisungen EXEC SQL vorangestellt, um anzuzeigen, dass es sich um eingebettete SQL-Anweisungen handelt. Diese Anweisungen werden beim Kompilieren der Datei vom Pro*C-Precompiler verarbeitet und der entsprechende C-Code für die Interaktion mit der Oracle-Datenbank generiert.

## Wie öffnet man eine PC-Datei?

Zum Öffnen einer PC-Datei benötigen Sie normalerweise einen Texteditor oder eine integrierte Entwicklungsumgebung (IDE), die das Bearbeiten von C- oder C++-Quellcode unterstützt. Hier sind einige gängige Optionen:

1.  **Texteditoren:**
    
- **Notizblock** (Windows)
- **TextEdit** (Mac)
- **gedit** (Linux)
- **Erhabener Text**
- **Atom**
- **Visual Studio-Code**
2.  **Integrierte Entwicklungsumgebungen (IDEs):**
    
- **Eclipse** mit CDT (C/C++ Development Tooling)
- **Visual Studio** mit Visual C++ oder Visual Studio Code mit C++-Erweiterung
- **Code::Blocks**
- **NetBeans** mit C/C++-Paket
  
## Verweise
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


