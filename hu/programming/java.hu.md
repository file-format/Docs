---
date: 2019-10-11
keywords: java, .java, java fájlformátum, java fájlok megnyitása, java fájlok futtatása, java fájl, java mintakód
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java fájl formátum
linktitle: Java
description: "Ismerje meg a Java fájlformátumot és az API-kat, amelyek Java-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Mi az a Java fájl? ##
A Java forráskódot tartalmazó és .java kiterjesztéssel mentett fájl Java fájlként ismert. A Java az egyik legszélesebb körben használt technológia játékok, mobil, webes és asztali alkalmazások fejlesztésére. Mivel a Java platformfüggetlen, hibátlanul működik Windowson, Macen, Linuxon, Raspberry Pi-n stb. A Java nagyon hasonlít a C#-ra és a C++-ra, így könnyebb váltani ezek között a nyelvek között.

## Rövid története ##

A Java projektet 1991 júniusában kezdeményezte James Gosling, Mike Sheridan és Patrick Naughton. A Java kezdetben Tölgynek nevezték. Később átnevezték Greenre és végül Java-ra. James Gosling a Java-t a C/C++-hoz hasonló szintaxissal tervezte. A Java első nyilvános verzióját 1996-ban adta ki a Sun Microsystems. Az összes népszerű rendszeren futhatott, ami miatt a Java gyorsan népszerűvé vált. A Java 2 1998 decemberi kiadásával többféle konfiguráció készült a különböző típusú platformokhoz. A verziók a következők voltak

- J2EE (Java EE): Vállalati megoldásokhoz
- J2ME (Java ME): Mobil alkalmazásokhoz
- J2SE (Java SE): Asztali alkalmazásokhoz

2006. november 19-én a Sun kiadta a Java Virtual Machine-t (JVM) ingyenes és nyílt forráskódú szoftverként. Miután az Oracle Corporation 2009–2010-ben felvásárolta a Sun Microsystemst, James Gosling 2010. április 2-án lemondott az Oracle-től.

## A ## Java kód futtatása/végrehajtása

A Java kód végrehajtásához először le kell fordítani. Ehhez Java SDK szükséges. A Java SDK a Java kódot bájtkód osztályfájlba fordítja. Vannak olyan IDE-k, mint az Eclipse és az IntelliJ Idea, amelyek megkönnyítik a Java fájlokkal való munkát azáltal, hogy kódkiegészítést és könnyen használható felületet biztosítanak a Java kód fordításához és végrehajtásához.

## Java fájlformátum ##

A Java szintaxisát nagymértékben befolyásolta a C és a C++, de a C++-tól eltérően a Java szinte kizárólag objektum-orientált nyelvként készült. A Java-ban az összes kód osztályokba van írva, és minden adatelem egy objektum. A C++-szal ellentétben a Java nem támogatja az operátor túlterhelését vagy többszörös öröklődését.

### Java mintakód ###

Az alábbiakban egy példa a Java szintaxisra.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
A fenti kódban a **public** kulcsszó a hozzáférésmódosítót jelöli. Kimondja, hogy ehhez az osztályhoz az osztályhierarchián kívüli osztályok is hozzáférhetnek. A hozzáférés módosító lehet **védett** (ugyanabban a csomagban érhető el) vagy **privát** (a metódusokhoz csak ugyanaz az osztály férhet hozzá). A metódus előtti **static** azt jelzi, hogy a metódus az osztály konkrét példánya nélkül is meghívható. A **void** azt jelzi, hogy a metódus nem ad vissza semmit. A karakterlánc kinyomtatása a konzolra. A System.out.println parancsot használjuk. Ebben a parancsban a *System* osztály egy statikus *out* mezővel rendelkezik, amely a *println* metódust tartalmazó *PrintStream* osztály példánya.

A Java fájlok fájlnevének meg kell egyeznie az osztály nevével. Tehát a példakódhoz tartozó Java fájl neve *ExampleApp.java* lesz.

## Hivatkozások ##

- [Java (programozási nyelv) - Wikipédia](https://en.wikipedia.org/wiki/Java_(programozási_nyelv))

