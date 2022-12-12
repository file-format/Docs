{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class","mi az osztályfájl","osztályfájl megnyitása", "kiterjesztés", "fájl", "osztályfájl","osztályfájlformátum", ".osztálykiterjesztés", "class file in java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Osztály - Java osztályú fájlformátum",
  "description":"További információ a Class fájlformátumról és az API-król, amelyek Class fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az a Class fájl?

A **Java nyelvű osztályfájl** a [.java](/hu/programming/java/) osztály lefordított kimenete, amelyet valójában egy Java Virtual Machine (JVM) hajt végre. Az osztályfájlok külön-külön is végrehajthatók, valamint részei lehetnek egy [JAR](/hu/programming/jar/) fájlnak csomagként, más csomagfájlokkal együtt. Ezeket a **`javac`** paranccsal lehet létrehozni a parancssori felületről. Egyes Java IDE-k, például az [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) és a NetBeans .class kimeneti fájlokat biztosítanak a projekt Java-jából. fájlokat.

## Osztály fájlformátum

A Java osztályfájl bájtkódból áll, amely a JVM által futtatandó köztes kód. Az osztályfájl 8 bites bájtokból áll, és a többbájtos adatelemek mindig nagy sorrendben tárolódnak.

### ClassFile szerkezet

Az osztályfájl szerkezete az alábbiak szerint látható.
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
ahol:

* u1 = előjel nélküli egybájtos mennyiség
* u2 = előjel nélküli kétbájtos mennyiség
* u4 = előjel nélküli négybájtos mennyiség

A .class fájlszerkezet részleteit, valamint az Oracle [osztályfájlformátum]-ban (https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) ismertetett részleteket, és hivatkozhat rájuk fejlesztők referenciaként. Ezeknek a mezőknek az összefoglalása a következő.

* `magic` – A mágikus elem megadja az osztály fájlformátumát azonosító mágikus számot; ennek értéke 0xCAFEBABE.
* `minor_version`, `major_version` - A minor_version és major_version elemek értékei ennek az osztályfájlnak a kisebb és fő verziószámai.
* `constant_pool_count` - A konstans_pool_számláló elem értéke megegyezik a konstans_pool_számláló táblában lévő bejegyzések számával plusz eggyel. A konstans_készlet index akkor tekinthető érvényesnek, ha nagyobb, mint nulla, és kisebb, mint a konstans_készlet_száma, kivéve a long és double típusú konstansokat.
* `constant_pool[]` - A konstans_készlet egy struktúrák táblázata (4.4. §), amely különféle karakterlánc-konstansokat, osztály- és interfészneveket, mezőneveket és egyéb állandókat jelent, amelyekre a ClassFile struktúrában és annak alstruktúráiban hivatkoznak. Minden konstans_pool táblabejegyzés formátumát az első "tag" bájt jelzi.
* `access_flags` – Az access_flags elem értéke az osztály vagy interfész hozzáférési engedélyeinek és tulajdonságainak jelölésére használt jelzők maszkja.
* `this_class` - A this_class elem értékének érvényes indexnek kell lennie a konstans_pool táblában.
* `super_class` - Osztály esetén a szuper_osztály elem értékének nullának kell lennie, vagy a konstans_pool tábla érvényes indexének kell lennie.
* `interfaces_count` - Az interfaces_count elem értéke megadja az ehhez az osztályhoz vagy interfésztípushoz tartozó közvetlen szuperinterfészek számát.
* `interfaces[]` - Az interfészek tömb minden értékének érvényes indexnek kell lennie a konstans_pool táblában.
* `fields_count` - A fields_count elem értéke megadja a field_info struktúrák számát a mezőtáblázatban.
* `fields[]` - A mezők táblájában minden értéknek egy field_info struktúrának kell lennie, amely teljes leírást ad egy mezőnek ebben az osztályban vagy interfészben.
* `methods_count` - A Methods_count elem értéke megadja a method_info struktúrák számát a metódustáblában.
* `methods[]` - A metódustáblában szereplő minden értéknek egy method_info struktúrának kell lennie, amely teljes leírást ad az ebben az osztályban vagy interfészben található metódusokról. Ha az ACC_NATIVE és az ACC_ABSTRACT jelzők egyike sincs beállítva egy method_info struktúra access_flags elemében, akkor a módszert megvalósító Java Virtual Machine utasítások is rendelkezésre állnak.
* `attributes_count` - Az attribútumok_száma elem értéke megadja az attribútumok számát (§4.7) az osztály attribútumtáblázatában.
* `attributes[]` – Az attribútumtáblázat minden értékének attribútum_info struktúrának kell lennie.




## Hivatkozások

* [Az osztály fájlformátuma](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

