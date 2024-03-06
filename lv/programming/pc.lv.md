{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC fails — Pro*C avota koda fails — kas ir .pc fails un kā to atvērt?",
  "description" : "Uzziniet par PC Pro*C avota koda failu un to, kā to atvērt.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Kas ir datora fails?

PC fails vai .pc fails ir ProC pirmkoda fails. ProC ir priekškompilators, ko izmanto kopā ar Oracle datu bāzēm, lai iegultu SQL paziņojumus C vai C++ kodā. Kompilējot Pro*C failu, tas ģenerē parasto C vai C++ kodu ar iegultām SQL komandām. Tas ļauj nemanāmi integrēt SQL datu bāzes darbības ar C vai C++ programmām.

Šeit ir pamata piemērs tam, kā varētu izskatīties Pro*C fails:

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

Šajā piemērā SQL priekšrakstiem ir pievienots prefikss EXEC SQL, lai norādītu, ka tie ir iegulti SQL priekšraksti. Kad fails tiks kompilēts, šos paziņojumus apstrādās Pro*C priekškompilators un tiks ģenerēts atbilstošs C kods, lai mijiedarbotos ar Oracle datu bāzi.

## Kā atvērt datora failu?

Lai atvērtu datora failu, parasti ir nepieciešams teksta redaktors vai integrētā izstrādes vide (IDE), kas atbalsta C vai C++ pirmkoda rediģēšanu. Tālāk ir norādītas dažas izplatītas iespējas.

1.  **Teksta redaktori:**
    
- **Piezīmju grāmatiņa** (Windows)
- **Teksta rediģēšana** (Mac)
- **gedit** (Linux)
- **Izcils teksts**
-**Atoms**
- **Visual Studio Code**
2.  **Integrētās izstrādes vides (IDE):**
    
- **Eclipse** ar CDT (C/C++ izstrādes rīki)
- **Visual Studio** ar Visual C++ vai Visual Studio kodu ar C++ paplašinājumu
- **Kods::Bloki**
- **NetBeans** ar C/C++ pakotni
  
## Atsauces
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


