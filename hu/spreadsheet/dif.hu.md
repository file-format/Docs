{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "file", "extension", "file format", "Data Interchange File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az a DIF fájlkiterjesztés és API-k, amelyekkel DIF fájlokat hozhat létre és nyithat meg.",
  "title" :"DIF - Adatcsere fájlformátum",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az a DIF fájl?

A DIF a Data Interchange Format rövidítése, amely táblázatos adatok importálására/exportálására szolgál a különböző alkalmazások között. Ezek közé tartozik a Microsoft Excel, az OpenOffice Calc, a StarCalc és még sokan mások. Egyetlen táblázatban tárolja az adatokat, ami ennek a fájlformátumnak az egyetlen korlátozása.

## A DIF fájlformátum rövid története ##

A DIF fájlformátumot a Software Arts, Inc. fejlesztette ki az 1980-as évek elején. A DIF fájlformátum-specifikációit a VisiCalc tartalmazza, amely az első táblázatkezelő program volt személyi számítógépekhez. Ezek a specifikációk szerzői jogvédelem alatt állnak 1981-ben, és a Software Arts Products Corp. bejegyzett védjegyei voltak.

## DIF fájlformátum ##

A DIF a táblázat tartalmát ASCII szövegfájlban tárolja, amely lehetővé teszi a megtekintését és a szövegszerkesztővel történő szerkesztését. A formátum az adatcsere jellemzői miatt elfoglalja helyét az adatsorosító formátumok listáján. A DIF fájl 2 részből áll; fejléc és adat.

A DIF-ben mindent egy 2 vagy 3 soros darab képvisel. A fejlécek 3 soros darabot kapnak; adatok, 2.

* A fejlécdarabok olyan szövegazonosítóval kezdődnek, amely csupa nagybetűs, csak alfabetikus karakterekből áll, és kevesebb, mint 32 betűből áll. A következő sornak egy számpárnak, a harmadik sornak pedig egy idézőjeles karakterláncnak kell lennie.
* Az adatdarabok számpárral kezdődnek, a következő sor pedig egy idézőjeles karakterlánc vagy egy kulcsszó.

### Értékek ###

Egy érték két sort foglal el, az első egy számpár, a második pedig egy karakterlánc vagy egy kulcsszó. A pár első száma a típust jelöli:

* −1 – direktíva típusa, a második szám figyelmen kívül marad, a következő sor az egyik ilyen kulcsszó:
** BOT – sor eleje (sor eleje)
** EOD – adatok vége
* 0 – numerikus típus, az érték a második szám, a következő sor az egyik kulcsszó:
** V – érvényes
** NA – nem elérhető
** ERROR – hiba
** TRUE – valódi logikai érték
** FALSE – hamis logikai érték
* 1 – karakterlánc típusa, a második szám figyelmen kívül marad, a következő sor a karakterlánc dupla idézőjelben

### DIF fejléc darab ###

A DIF-fájl fejlécrésze egy azonosító sorból áll, amelyet egy érték két sora követ. A fejlécdarabokban lévő számértékek csak egy üres karakterláncot használnak az érvényességi kulcsszavak helyett. Ezeknek a fejlécdaraboknak a részletei a következők.

* TÁBLÁZAT - a verziót numerikus érték követi, az érték használaton kívüli második sora generátor megjegyzést tartalmaz
* VEKTOROK – az oszlopok száma numerikus értékként következik
* TUPLES - a sorok száma numerikus értékként következik
* ADATOK – a 0-s ál-számérték után a táblázat adatai következnek, minden sor előtt egy BOT-érték, a teljes táblázat EOD-értékkel zárul

### DIF példa ###

A következő példa egy egyszerű munkalap tartalmát és annak megfelelő DIF-ábrázolását mutatja be.


|Név|Kor
---|---|
|Bob|34
|Lap|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Hivatkozások ##

* [ DIF – a Wikipedia által](https://en.wikipedia.org/wiki/Data_Interchange_Format)

