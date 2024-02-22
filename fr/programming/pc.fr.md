{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier PC - Fichier de code source Pro*C - Qu'est-ce que le fichier .pc et comment l'ouvrir ?",
  "description" : "Découvrez le fichier de code source PC Pro*C et comment l'ouvrir.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-fr",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Qu'est-ce qu'un fichier PC ?

Un fichier PC ou un fichier .pc est un fichier de code source ProC. ProC est un précompilateur utilisé avec les bases de données Oracle pour intégrer des instructions SQL dans du code C ou C++. Lorsque vous compilez un fichier Pro*C, il génère du code C ou C++ standard avec des commandes SQL intégrées. Cela vous permet d'intégrer de manière transparente les opérations de base de données SQL à vos programmes C ou C++.

Voici un exemple de base de ce à quoi pourrait ressembler le fichier Pro*C :

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

Dans cet exemple, les instructions SQL portent le préfixe EXEC SQL pour indiquer qu'il s'agit d'instructions SQL incorporées. Ces instructions seront traitées par le précompilateur Pro*C lorsque le fichier sera compilé et le code C approprié sera généré pour interagir avec la base de données Oracle.

## Comment ouvrir le fichier PC ?

Pour ouvrir un fichier PC, vous avez généralement besoin d'un éditeur de texte ou d'un environnement de développement intégré (IDE) prenant en charge l'édition du code source C ou C++. Voici quelques options courantes :

1.  **Éditeurs de texte :**
    
- **Bloc-notes** (Windows)
- **TexteEdit** (Mac)
- **gedit** (Linux)
- **Texte sublime**
- **Atome**
- **Code de Visual Studio**
2.  **Environnements de développement intégrés (IDE) :**
    
- **Eclipse** avec CDT (outils de développement C/C++)
- **Visual Studio** avec Visual C++ ou Visual Studio Code avec extension C++
- **Code ::Blocs**
- **NetBeans** avec pack C/C++
  
## Les références
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


