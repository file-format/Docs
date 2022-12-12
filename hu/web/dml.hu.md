{
  "date" : "2021-05-25",
  "keywords" :[ "DML", "DML fájl", "DML fájlformátum", "DML fájltípus", "fájl", "típus", "mi az a DML fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML – DynaScript HTML fájl",
  "description":"További információ a DML fájlformátumról és az API-król, amelyek DML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Mi az a DML fájl?

A .dml kiterjesztésű fájl egy DyanScript segítségével létrehozott web-szkriptoldal kódfájlja. A DynaScript egy dinamikus [HTML](/hu/web/html/) szkriptnyelv, amely kompatibilis az ECMAScript-szel, és ugyanazokat a szolgáltatásokat nyújtja, mint a többi szkriptnyelv. Hasonló a ColdFusion kódhoz és a Microsoft Active Server Pages (ASP) kódhoz. A DML-fájlok más HTML-oldalakhoz hasonlóan szabványos webböngészőkben is megnyithatók és megtekinthetők.

## DML fájl formátum

A DML fájlok egyszerű szöveges fájlformátumban jönnek létre, és szövegszerkesztővel megnyithatók a kód megtekintéséhez. A DML szkriptnyelvet használó kódírás használható HTML dinamikus generálására a szerveroldali DML oldalakon. A DynaScriptek a következő nyelvi elemekből épülnek fel:


* SCRIPT címke – Ezek HTML megjegyzésként vannak beágyazva a dokumentumokba. A HTML megjegyzést egy \ jelöli <!-- tag.
* Literálok – Ezek rögzített értékek a DynaScript fájlokban. Példák ezekre az egész számok, például s 123 , 0x3F , 0123, lebegőpontos számok, például 456.789 , 3.2e-8, logikai, például igaz vagy hamis, és karakterlánc, például "Az eső Spanyolországban".
* Változók – A DynaScript változókat nem kell definiálni, és nem kell rögzített adattípushoz rendelni. A változónak értékkel kell rendelkeznie, mielőtt egy kifejezésben használná; ellenkező esetben futásidejű figyelmeztetés generálódik.
* Kifejezések – Változók, literális értékek, operátorok és egyéb kifejezések kombinációi. A hozzárendelési utasítás jobb oldala egy kifejezés.
* Operátorok – Ezek egy vagy több, operandusnak nevezett kifejezéssel működnek. Ezek lehetnek ternárisok, binárisok vagy unárisak: a hármas operátorok három kifejezésre, a bináris operátorok két kifejezésre, az unáris operátorok pedig egyre hatnak.
* Nyilatkozatok – Ezek vezérlik a szkriptfolyamatot, manipulálják az objektumokat és általános programozást. Általában ezek az utasítások szabványos C és Java szintaxist követnek. Példák az if-else, do-while ciklusok, váltás, szünet, folytatás stb., mint bármely más szkriptnyelv.
* Funkciók – A függvények, mint bármely más szkriptnyelv, lehetővé teszik, hogy egy utasításkészletet egyszer beépítsünk egy dokumentumba függvényként, majd többször használjuk a dokumentumban (a függvény meghívásával). A DynaScript funkciókat is támogat.
* Objektumok – A DynaScript objektum-orientált, és támogatja az "objektumokat", valamint a beágyazás, a polimorfizmus és az öröklődés alapvető objektum-orientált fogalmait.

