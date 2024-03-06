{
  "date": "2019-10-11",
  "keywords": [
"klasē",
".klase",
"kas ir klases fails",
"kā atvērt klases failu",
"pagarinājumu",
"failu",
"klases fails",
"klases faila formātā",
".klases paplašinājums",
"klases fails java"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Klase — Java klases faila formāts",
  "description": "Uzziniet par Class failu formātu un API, kas var izveidot un atvērt Class failus.",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-clas-lvs"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir klases fails?

**Klases fails Java** ir [.java](/programming/java/) klases kompilētā izvade, ko faktiski izpilda Java virtuālā mašīna (JVM). Klases failus var izpildīt atsevišķi, kā arī tie var būt daļa no [JAR](/programming/jar/) faila kā komplekts kopā ar citiem pakotnes failiem. Tos var izveidot, izmantojot komandu **`javac`** no komandrindas saskarnes. Daži Java IDE, piemēram, [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) un NetBeans, nodrošina .class izvades failu izveidi no projekta Java failiem.

## Klases faila formāts

Java klases fails sastāv no baitkoda, kas ir starpposma kods, kas jāizpilda JVM. Klases fails sastāv no 8 bitu baitu straumes, un vairāku baitu datu vienumi vienmēr tiek glabāti lielā secībā.

### ClassFile struktūra

Klases faila struktūra ir tāda, kā parādīts zemāk.
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
kur:

* u1 = neparakstīts viena baita daudzums

* u2 = neparakstīts divu baitu daudzums

* u4 = neparakstīts četru baitu daudzums


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `magic` — burvju vienums nodrošina maģisko numuru, kas identificē klases faila formātu; tā vērtība ir 0xCAFEBABE.

* `minor_version`, `major_version` — vienumu minor_version un major_version vērtības ir šīs klases faila mazās un galvenās versijas numuri.

* `constant_pool_count` — vienuma konstante_pool_skaits vērtība ir vienāda ar ierakstu skaitu tabulā konstante_pulks plus viens. Konstantes_pūles indekss tiek uzskatīts par derīgu, ja tas ir lielāks par nulli un mazāks par konstantes_pūles_skaits, izņemot konstantes, kuru tips ir long un double.

* `constant_pool[]` — konstante_pūle ir struktūru tabula (4.4. punkts), kas attēlo dažādas virkņu konstantes, klašu un saskarņu nosaukumus, lauku nosaukumus un citas konstantes, uz kurām ir atsauce ClassFile struktūrā un tās apakšstruktūrās. Katras konstantes_pool tabulas ieraksta formāts ir norādīts ar tā pirmo "taga" baitu.

* `access_flags` — vienuma access_flags vērtība ir karogu maska, ko izmanto, lai apzīmētu šīs klases vai saskarnes piekļuves atļaujas un rekvizītus.

* `this_class` — šī_klase vienuma vērtībai ir jābūt derīgam indeksam tabulā konstante_pūle.

* `super_klase` — klasei super_class vienuma vērtībai ir jābūt nullei vai derīgam indeksam tabulā konstante_pulks.

* `interfeisu_skaits` — vienuma interfaces_count vērtība norāda šīs klases vai saskarnes veida tiešo supersaskarņu skaitu.

* `interfeiss[]` — katrai vērtībai interfeisu masīvā ir jābūt derīgam indeksam tabulā konstante_pūle.

* `fields_count` — vienuma fields_count vērtība norāda lauka_informācijas struktūru skaitu lauku tabulā.

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `methods_count` — vienuma method_count vērtība norāda metodi_info struktūru skaitu metožu tabulā.

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `attributes_count` — elementa atribūti_skaits vērtība norāda atribūtu skaitu (§4.7) šīs klases atribūtu tabulā.

* `attributes[]` — katrai atribūtu tabulas vērtībai ir jābūt atribūtu_info struktūrai.





## Atsauces

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

