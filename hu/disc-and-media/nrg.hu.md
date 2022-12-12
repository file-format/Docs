{
  "date" : "2021-08-16",
  "keywords" :[ "nrg fájl", "nrg fájl formátum", "mi az nrg fájl", "fájl", "nrg példa", "nrg fájl kiterjesztése", "kiterjesztés", "formátum", "nrg lábléc", "fájl nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ az NRG fájlformátumról és az API-król, amelyek NRG-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"NRG - Lemezképfájl formátum",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Mi az NRG fájl?

Az optikai lemez használatával létrehozott képfájlformátum NRG-fájlformátumnak minősül. Ezt a formátumot a Nero kifejezetten a Nero Burning Rom segédprogramjához készítette. A lemezképek tárolására ezt a formátumot tekintik használtnak, mivel az adott fájlokhoz megfelelő. Ezek a fájlok lehetnek CD vagy DVD pontos másolatai, vagy tartalmazhatnak több fájlt, amelyek lemezként csatlakoztathatók. Más népszerűbb fájlformátumok, például az [ISO](/hu/compression/iso/) fájlformátumok azok, amelyekbe ezeket a fájlokat néhány alapvető segédprogramra lehet konvertálni. Leggyakrabban az NRG-fájlokat biztonsági mentések vagy másolatok készítésére használják néhány fontos adatról vagy lemezről.

## NRG fájlformátum ##

Ezt a fájlformátumot a Nero AG fejlesztette ki lemezképformátumként. A Nero Burning Rom segédprogram sajátos tulajdonságával rendelkezett, mivel lemezképek tárolására fejlesztették ki. Az első verziót úgy határozták meg, hogy az értékeket 32 bites egész számként tárolja. A második verzió azonban elindult, és a 64 bites egész számok támogatását tartalmazza.

## Műszaki specifikáció ##

A fájl elején ez a formátum nem tárolja fejlécként az adatait. Mint egy lábléc, a fájl végére van csatolva. A kép információi IFF darabok formájában tárolódnak. Az első csonk eltolása az NRG lábléc beolvasásával érhető el a fájl utolsó 8-12 byte-jánál. Az NRG fájlformátum minden verziója tartalmaz darabokat, DAOI-t, CD-szöveget, munkamenet-információs adathordozó típusát, lemezinformációkat, Relo-t és a láncvéget. A bájtsorrend nagyméretű, és a tároláskor minden egész érték előjel nélküli.

### Fő darabok ###

#### Jelzőlap ####

Ez a jelzőlap könnyen elérhető az összes NRG fájlformátum verziójában. A **CUEX** darabja a rögzített méretű összefűzés blokkjait jelenti, és ezek mindegyike a jelzőpontot jelenti.

#### DAO információ ####

Ez az információ az összes NRG formátumú verzióban is megtalálható. A **DAOI** darabjai 2 részben tárolják a releváns információkat. Ennek első része csak a munkamenet-specifikus adatokat tartalmazza. A második része csak megismétli a követéssel kapcsolatos szürke információkat, és minden sávnál csak egyszer.

#### CD-szöveg ####

Ez elérhető az NRG második verziójában. A **CDTX** darabja a CD-text csomag nyers összefűzéséből áll, mindegyik 18 bájttal.

#### Kibővített pályainformáció ####

Ez az NRG fájlformátumának minden verziójában elérhető. Ezeket a darabokat az egyszerre munkamenetek nyomkövetési információinak tárolására használják. Ez az adat minden sáv esetében csak egyszer ismétlődik.

#### Munkamenet információ ####

Ez is elérhető az NRG fájlformátumának minden verziójában. A munkamenet-darabok információit fel kell használni a munkamenet képének gyors beolvasásához, majd a sávok számának követéséhez.

#### Lánc vége ####

A végdarab azt jelenti, hogy most már nincs több olvasnivaló darab, és ez az NRG összes verziójában is elérhető.


## Hivatkozások ##

* [NRG – a Wikipedia által](https://en.wikipedia.org/wiki/NRG_(file_format))


