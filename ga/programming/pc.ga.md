{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad PC - Comhad Cód Foinse Pro*C - Cad é an comhad .pc agus conas é a oscailt?",
  "description" : "Foghlaim faoi Chomhad Cód Foinse PC Pro*C agus conas é a oscailt.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-ga",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Cad is comhad PC ann?

Is comhad cód foinse ProC é comhad PC nó comhad .pc. Is réamhthiomsóir é ProC a úsáidtear le bunachair shonraí Oracle chun ráitis SQL a leabú laistigh de chód C nó C++. Nuair a thiomsaíonn tú comhad Pro * C, gineann sé cód rialta C nó C ++ le horduithe SQL leabaithe. Ligeann sé seo duit oibríochtaí bunachar sonraí SQL a chomhtháthú gan uaim le do chláir C nó C++.

Seo sampla bunúsach den chuma a bheadh ar chomhad Pro*C:

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

Sa sampla seo, déantar ráitis SQL a réamhshocrú le EXEC SQL chun a chur in iúl gur ráitis SQL leabaithe iad. Déanfaidh réamhthiomsaitheoir Pro*C na ráitis seo a phróiseáil nuair a bheidh an comhad curtha le chéile agus ginfear cód C cuí chun idirghníomhú le bunachar sonraí Oracle.

## Conas comhad PC a oscailt?

Chun comhad PC a oscailt, is gnách go mbíonn eagarthóir téacs nó Timpeallacht Chomhtháite Forbartha (IDE) uait a thacaíonn le heagarthóireacht cód foinse C nó C++. Seo roinnt roghanna coitianta:

1.  **Eagarthóirí Téacs:**
    
- ** Notepad** (Windows)
- **TextEdit** (Mac)
- **gedit** (Linux)
- **Téacs sublime**
- **Adamh**
- **Cód Stiúideo Amhairc**
2.  **Timpeallacht Chomhtháite Forbartha (IDEanna):**
    
- **Eclipse** le CDT (Uirlisiú Forbartha C/C++)
- **Amharc-Stiúideo** le Visual C++ nó Cód Stiúideo Amharc le síneadh C++
- **Cód::Bloic**
- **NetBeans** le pacáiste C/C++
  
## Tagairtí
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


