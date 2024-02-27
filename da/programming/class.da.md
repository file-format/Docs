{
  "date": "2019-10-11",
  "keywords": [
"klasse",
".klasse",
"hvad er en klassefil",
"hvordan man åbner en klassefil",
"udvidelse",
"fil",
"klasse fil",
"klasse filformat",
".klasse udvidelse",
"klasse fil i java"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Klasse - Java-klasse filformat",
  "description": "Lær om klassefilformat og API'er, der kan oprette og åbne klassefiler.",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-clas-das"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en klassefil?

En **Klassefil i Java** er det kompilerede output af klassen [.java](/programming/java/), der faktisk udføres af en Java Virtual Machine (JVM). Klassefiler kan udføres individuelt såvel som kan være en del af en [JAR](/programming/jar/)-fil som en pakke sammen med andre pakkefiler. Disse kan oprettes ved hjælp af kommandoen **`javac`** fra kommandolinjegrænsefladen. Nogle Java IDE'er som [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) og NetBeans giver oprettelse af .class outputfiler fra projektets Java-filer.

## Klasse filformat

En Java-klassefil består af bytekode, der er mellemkode, der skal køres af JVM. En klassefil består af en strøm af 8-bit bytes og multibyte dataelementer gemmes altid i big-endian rækkefølge.

### Klassefilstruktur

Klassefilstrukturen er som vist nedenfor.
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
hvor:

* u1 = én-byte-mængde uden fortegn

* u2 = usigneret to-byte-mængde

* u4 = fire-byte uden fortegn


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `magic` - Det magiske element leverer det magiske nummer, der identificerer klassens filformat; den har værdien 0xCAFEBABE.

* `minor_version`, `major_version` - Værdierne for minor_version og major_version elementerne er mindre og større versionsnumre for denne klassefil.

* `constant_pool_count` - Værdien af constant_pool_count-elementet er lig med antallet af poster i constant_pool-tabellen plus én. Et constant_pool-indeks anses for gyldigt, hvis det er større end nul og mindre end constant_pool_count, med undtagelse af konstanter af typen lang og dobbelt.

* `constant_pool[]` - Konstant_puljen er en tabel af strukturer (§4.4), der repræsenterer forskellige strengkonstanter, klasse- og grænsefladenavne, feltnavne og andre konstanter, der henvises til i ClassFile-strukturen og dens understrukturer. Formatet for hver konstant_pool-tabelpost er angivet med dens første "tag"-byte.

* `access_flags` - Værdien af access_flags elementet er en maske af flag, der bruges til at angive adgangstilladelser til og egenskaber for denne klasse eller grænseflade.

* `this_class` - Værdien af this_class-elementet skal være et gyldigt indeks i constant_pool-tabellen.

* `super_class` - For en klasse skal værdien af super_class elementet enten være nul eller skal være et gyldigt indeks i constant_pool tabellen.

* `interfaces_count` - Værdien af elementet interfaces_count angiver antallet af direkte supergrænseflader af denne klasse eller grænsefladetype.

* `interfaces[]` - Hver værdi i interfaces-arrayet skal være et gyldigt indeks i constant_pool-tabellen.

* `fields_count` - Værdien af fields_count elementet angiver antallet af field_info strukturer i felttabellen.

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `methods_count` - Værdien af methods_count elementet giver antallet af method_info strukturer i metodetabellen.

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `attributes_count` - Værdien af attributes_count elementet angiver antallet af attributter (§4.7) i attributtabellen for denne klasse.

* `attributes[]` - Hver værdi i attributtabellen skal være en attribute_info-struktur.





## Referencer

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

