{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PC Dosyası - Pro*C Kaynak Kodu Dosyası - .pc dosyası nedir ve nasıl açılır?",
  "description" : "PC Pro*C Kaynak Kodu Dosyası ve nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-tr",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## PC dosyası nedir?

PC dosyası veya .pc dosyası bir ProC kaynak kodu dosyasıdır. ProC, SQL ifadelerini C veya C++ koduna gömmek için Oracle veritabanlarıyla birlikte kullanılan bir ön derleyicidir. Pro*C dosyasını derlediğinizde, yerleşik SQL komutlarıyla normal C veya C++ kodu üretir. Bu, SQL veritabanı işlemlerini C veya C++ programlarınızla sorunsuz bir şekilde entegre etmenize olanak tanır.

Pro*C dosyasının nasıl görünebileceğine dair temel örnek:

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

Bu örnekte, SQL ifadelerine gömülü SQL ifadeleri olduklarını belirtmek için EXEC SQL ön eki eklenmiştir. Bu ifadeler, dosya derlendiğinde Pro*C ön derleyicisi tarafından işlenecek ve Oracle veritabanıyla etkileşime geçmek için uygun C kodu üretilecektir.

## PC dosyası nasıl açılır?

Bir PC dosyasını açmak için genellikle bir metin düzenleyiciye veya C veya C++ kaynak kodunu düzenlemeyi destekleyen bir Tümleşik Geliştirme Ortamına (IDE) ihtiyacınız vardır. İşte bazı yaygın seçenekler:

1.  **Metin Editörleri:**
    
- **Not Defteri** (Windows)
- **Metin Düzenleme** (Mac)
- **gedit** (Linux)
- **Yüce metin**
- **Atom**
- **Görsel Stüdyo Kodu**
2.  **Entegre Geliştirme Ortamları (IDE'ler):**
    
- **Eclipse** ile CDT (C/C++ Geliştirme Aracı)
- **Visual Studio** ile Visual C++ veya C++ uzantılı Visual Studio Code
- **Kod::Bloklar**
- **NetBeans** C/C++ paketiyle
  
## Referanslar
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


