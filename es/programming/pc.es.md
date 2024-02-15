{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Archivo PC - Archivo de código fuente Pro*C - ¿Qué es el archivo .pc y cómo abrirlo?",
  "description" : "Obtenga información sobre el archivo de código fuente de PC Pro*C y cómo abrirlo.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-es-pc",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## ¿Qué es un archivo de PC?

Un archivo PC o un archivo .pc es un archivo de código fuente ProC. ProC es un precompilador que se utiliza con bases de datos Oracle para incrustar declaraciones SQL en código C o C++. Cuando compila un archivo Pro*C, genera código C o C++ normal con comandos SQL integrados. Esto le permite integrar perfectamente las operaciones de la base de datos SQL con sus programas C o C++.
A continuación se muestra un ejemplo básico de cómo podría verse un archivo Pro*C:

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

En este ejemplo, las sentencias SQL tienen el prefijo EXEC SQL para indicar que son sentencias SQL incorporadas. Estas declaraciones serán procesadas por el precompilador Pro*C cuando se compila el archivo y se generará el código C apropiado para interactuar con la base de datos Oracle.
## ¿Cómo abrir un archivo de PC?

Para abrir un archivo de PC, normalmente necesita un editor de texto o un entorno de desarrollo integrado (IDE) que admita la edición de código fuente C o C++. Aquí hay algunas opciones comunes:

1.  **Editores de texto:**
    
- **Bloc de notas** (Windows)
- **Edición de texto** (Mac)
- **gedit** (Linux)
- **Texto sublime**
- **Átomo**
- **Código de Visual Studio**
2.  **Entornos de desarrollo integrados (IDE):**
    
- **Eclipse** con CDT (herramientas de desarrollo C/C++)
- **Visual Studio** con Visual C++ o Visual Studio Code con extensión C++
- **Código::Bloques**
- **NetBeans** con paquete C/C++
  
## Referencias
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


