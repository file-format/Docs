{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PC File - Pro*C Source Code File - What is .pc file and how to open it?",
  "description" : "Learn about PC Pro*C Source Code File and how to open it.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc",
      "parent" : "programming"
    }
  },
  "lastmod" : "2024-02-08"
}

## What is a PC file?

PC file	or a .pc file is a ProC source code file. ProC is a precompiler used with Oracle databases to embed SQL statements within C or C++ code. When you compile Pro*C file, it generates regular C or C++ code with embedded SQL commands. This allows you to seamlessly integrate SQL database operations with your C or C++ programs.

Here is basic example of what Pro*C file might look like:

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

In this example, SQL statements are prefixed with EXEC SQL to indicate that they are embedded SQL statements. These statements will be processed by Pro*C precompiler when file is compiled and appropriate C code will be generated to interact with Oracle database.

## How to open PC file?

To open a PC file, you typically need a text editor or an Integrated Development Environment (IDE) that supports editing C or C++ source code. Here are some common options:

1.  **Text Editors:**
    
    -   **Notepad** (Windows)
    -   **TextEdit** (Mac)
    -   **gedit** (Linux)
    -   **Sublime Text**
    -   **Atom**
    -   **Visual Studio Code**
2.  **Integrated Development Environments (IDEs):**
    
    -   **Eclipse** with CDT (C/C++ Development Tooling)
    -   **Visual Studio** with Visual C++ or Visual Studio Code with C++ extension
    -   **Code::Blocks**
    -   **NetBeans** with C/C++ pack
  
## References
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)
