{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File PC - File Kode Sumber Pro*C - Apa itu file .pc dan bagaimana cara membukanya?",
  "description" : "Pelajari tentang File Kode Sumber PC Pro*C dan cara membukanya.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-id",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Apa itu file PC?

File PC atau file .pc adalah file kode sumber ProC. ProC adalah prakompiler yang digunakan dengan database Oracle untuk menyematkan pernyataan SQL dalam kode C atau C++. Saat Anda mengkompilasi file Pro*C, itu menghasilkan kode C atau C++ biasa dengan perintah SQL yang tertanam. Hal ini memungkinkan Anda mengintegrasikan operasi database SQL dengan program C atau C++ secara lancar.

Berikut adalah contoh dasar tampilan file Pro*C:

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

Dalam contoh ini, pernyataan SQL diawali dengan EXEC SQL untuk menunjukkan bahwa pernyataan tersebut adalah pernyataan SQL yang tertanam. Pernyataan ini akan diproses oleh precompiler Pro*C ketika file dikompilasi dan kode C yang sesuai akan dihasilkan untuk berinteraksi dengan database Oracle.

## Bagaimana cara membuka file PC?

Untuk membuka file PC, Anda biasanya memerlukan editor teks atau Lingkungan Pengembangan Terpadu (IDE) yang mendukung pengeditan kode sumber C atau C++. Berikut beberapa opsi umum:

1.  **Editor Teks:**
    
- **Buku Catatan** (Windows)
- **Edit Teks** (Mac)
- **gedit** (Linux)
- **Teks Luhur**
- **Atom**
- **Kode Visual Studio**
2.  **Lingkungan Pengembangan Terpadu (IDE):**
    
- **Eclipse** dengan CDT (Perkakas Pengembangan C/C++)
- **Visual Studio** dengan Visual C++ atau Visual Studio Code dengan ekstensi C++
- **Kode::Blok**
- **NetBeans** dengan paket C/C++
  
## Referensi
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


