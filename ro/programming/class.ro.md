{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class", "ce este un fișier de clasă", "cum se deschide un fișier de clasă", "extensie", "fișier", "fișier de clasă", "format de fișier de clasă", "extensie de clasă", "fișier de clasă în java"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Class - Java Class File Format",
  "description":"Aflați despre formatul de fișier Class și despre API-urile care pot crea și deschide fișiere Class.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier Class?

Un **Fișier de clasă în Java** este rezultatul compilat al clasei [.java](/ro/programming/java/) care este de fapt executat de o mașină virtuală Java (JVM). Fișierele de clasă pot fi executate individual, precum și pot face parte dintr-un fișier [JAR](/ro/programming/jar/) ca un pachet împreună cu alte fișiere pachet. Acestea pot fi create folosind comanda **`javac`** din interfața liniei de comandă. Unele IDE-uri Java, cum ar fi [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) și NetBeans oferă crearea de fișiere de ieșire .class din Java a proiectului fișiere.

## Format de fișier de clasă

Un fișier de clasă Java constă dintr-un bytecode care este cod intermediar care trebuie rulat de JVM. Un fișier de clasă constă dintr-un flux de octeți de 8 biți, iar elementele de date pe mai mulți octeți sunt întotdeauna stocate în ordine big-endian.

### Structura fișierului de clasă

Structura fișierului de clasă este așa cum se arată mai jos.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
Unde:

* u1 = cantitate nesemnată de un octet
* u2 = cantitate nesemnată de doi octeți
* u4 = cantitate nesemnată de patru octeți

Detalii despre structura fișierului .class sunt explicate în Oracle [formatul fișierului de clasă](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) și pot fi trimise de către dezvoltatori pentru referință. Un rezumat al acestor câmpuri este după cum urmează.

* `magic` - Elementul magic furnizează numărul magic care identifică formatul de fișier al clasei; are valoarea 0xCAFEBABE.
* `minor_version`, `major_version` - Valorile elementelor minor_version și major_version sunt numerele de versiune minoră și majoră ale acestui fișier de clasă.
* `constant_pool_count` - Valoarea elementului constant_pool_count este egală cu numărul de intrări din tabelul constant_pool plus unu. Un index constant_pool este considerat valid dacă este mai mare decât zero și mai mic decât constant_pool_count, cu excepția constantelor de tip long și double.
* `constant_pool[]` - Constant_pool este un tabel de structuri (§4.4) reprezentând diverse constante de șir, nume de clase și interfețe, nume de câmpuri și alte constante la care se face referire în structura ClassFile și substructurile sale. Formatul fiecărei intrări de tabel constant_pool este indicat de primul octet „etichetă”.
* `access_flags` - Valoarea elementului access_flags este o mască de steaguri folosită pentru a indica permisiunile de acces și proprietățile acestei clase sau interfețe.
* `this_class` - Valoarea elementului this_class trebuie să fie un index valid în tabelul constant_pool.
* `super_class` - Pentru o clasă, valoarea elementului super_class fie trebuie să fie zero, fie trebuie să fie un index valid în tabelul constant_pool.
* `interfaces_count` - Valoarea elementului interfaces_count oferă numărul de super-interfețe directe din această clasă sau tip de interfață.
* `interfaces[]` - Fiecare valoare din tabloul interfețe trebuie să fie un index valid în tabelul constant_pool.
* `fields_count` - Valoarea elementului fields_count oferă numărul de structuri field_info din tabelul de câmpuri.
* `fields[]` - Fiecare valoare din tabelul fields trebuie să fie o structură field_info care oferă o descriere completă a unui câmp din această clasă sau interfață.
* `methods_count` - Valoarea elementului methods_count oferă numărul de structuri method_info din tabelul de metode.
* `methods[]` - Fiecare valoare din tabelul de metode trebuie să fie o structură method_info care oferă o descriere completă a unei metode din această clasă sau interfață. Dacă niciunul dintre steagurile ACC_NATIVE și ACC_ABSTRACT nu sunt setate în elementul access_flags al unei structuri method_info, instrucțiunile Java Virtual Machine care implementează metoda sunt de asemenea furnizate.
* `attributes_count` - Valoarea elementului attributes_count oferă numărul de atribute (§4.7) din tabelul de atribute al acestei clase.
* `attributes[]` - Fiecare valoare a tabelului de atribute trebuie să fie o structură attribute_info.




## Referințe

* [Format de fișier de clasă](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

