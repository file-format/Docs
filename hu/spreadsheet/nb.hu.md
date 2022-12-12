{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "file", "extension", "file format", "Mathematica", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ arról, hogy mik azok az NB fájl API-k, amelyek létrehozhatnak és megnyithatnak NB fájlokat.",
  "title" :"Megjegyzés - Mathematica notebook fájlformátum",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Mi az NB fájl?

Az .nb kiterjesztésű fájl egy Wolfram notebook fájlformátum, amely szöveges fájlba menti a matematikai utasításokhoz szükséges utasításokat. Számos különböző típusú adatot tartalmazhat, például élő számítást, tetszőleges dinamikus interfészt, teljes betűtípusú bevitelt, képbevitelt, automatikus kódjegyzeteket, teljes, magas szintű programozási felületet, valamint több ezer gondosan szervezett funkciót és opciót. A szöveges utasítások a Mathematica bemeneti és kimeneti, amelyek a bemeneti utasítások fájlba kerülésekor generálódnak és frissülnek.

## Wolfram Notebook NB fájlformátum - További információ

A Wolfram Notebook NB fájlok egyszerű szöveges formátumban kerülnek mentésre, amely egy ember által olvasható fájlformátum. A jegyzetfüzet tartalma szakaszokba van rendezve egyszerű szövegként, ahol mindegyik cellacsoportot képvisel, hasonlóan a táblázatokhoz. Ezeknek a csoportoknak a tartományát egy zárójel határozza meg az egyes cellák végén. A cellához rendelt stílus határozza meg annak szerepét a jegyzetfüzetben az alábbiak szerint.

### Notebookok Wolfram nyelvként

Ha a matematikai utasításokból álló Jegyzetfüzetet el kívánjuk menteni a Wolfram Language Kernal által végrehajtandó végrehajtáshoz, a dokumentum cellái automatikusan a "Bevitel" szövegstílushoz lesznek rendelve. Ez arra utasítja a kernalt, hogy ezeket olyan utasításoknak tekintse, amelyek akkor futnak le, amikor a felhasználó a Shift+Return billentyűkombinációt adja ki. A Mathematica jegyzetfüzet a következő példában látható.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram Notebook fájlformátum" >}}

### Jegyzetfüzetek mint dokumentumok

A Mathematica jegyzetfüzetek lehetnek dokumentum formátumúak, hogy áttekintsék azt, amit látsz, amit kapsz (WYSIWYG). Ezek a dokumentumok megegyeznek a képernyőn vagy nyomtatott papíron láthatókkal, és interaktívak. Ehhez a "Szövegstílus" hozzá van rendelve a cellához, hogy a kernel utasításainak végrehajtása nélkül jelenítse meg a tartalmat.

## Mathematica notebookok exportálása

A Mathematica notebookok számos különböző fájlformátumba exportálhatók, például PDF, grafika, GIS, tömörített és táblázatokba.

## Hivatkozások

* [A Mathematica Notebook alapjai](https://reference.wolfram.com/language/guide/NotebookBasics.html)

