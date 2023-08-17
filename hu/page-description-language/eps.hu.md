{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "file", "extension", "file format", "Page Layout", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az EPS fájlformátumról és az API-król, amelyek EPS-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"EPS fájlformátum - Encapsulated PostScript fájl",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az EPS fájl?

Az .eps fájl egy képfájl, amely Encapsulated Postscript fájlformátumban kerül a lemezre mentésre. Szöveg, grafika és kép bármilyen kombinációját tartalmazhatja. Az EPS-fájlok tartalmazhatnak egy bittérképes előnézeti képet is, amelyet az ilyen fájlokat megnyitni képes alkalmazások megjeleníthetnek.

## Az EPS fájlformátum rövid története

Egy gyors pillantás az EPS fájlformátumra az előzmények szemszögéből a következő információkat tárja fel:

* Az EPS első verzióját az Adobe adta ki valamikor 1985 és 1988 között
* Az EPS specifikáció 2.0-s verziója 1989 januárjában jelent meg
* Az EPS 3.0-s verziójának specifikációja külön dokumentumként jelent meg 1992-ben; ez a legújabb közzétett verzió.

Az EPS az Adobe PostScript Language Document Structuring Conventions Specifikációjának 9. szakaszában leírt Open Structuring Conventions kiterjesztési mechanizmussal együtt képezte az Adobe Illustrator Artwork fájlformátum korai verzióinak alapját.

## EPS fájlformátum

Az EPS egy védett, de nyilvánosan dokumentált formátum, és az EPS fájlformátum specifikációi nyilvánosan elérhetők a fejlesztők számára. Az EPS egy [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Dokumentumszerkezeti Egyezmény) megfelelő fájlformátum, és betartja a DSC által meghatározott összes szabályt. A DSC egy speciális fájlformátum az Adobe PostScript dokumentumokhoz. Minden olyan alkalmazásnak, amely azt állítja, hogy képes olvasni az EPS fájlokat, DSC-kompatibilisnek kell lennie.

Az EPS-fájl két fő részből áll, az alábbiak szerint.

### Előnézet kép ###

Egy tipikus EPS-fájl előnézeti képet tartalmaz olyan formátumban, amely kényelmesen használható egy több rendszert vagy alkalmazást érintő munkafolyamatban. Az előnézet célja, hogy a kép olyan formátumban legyen, amelyet a legtöbb grafikus alkalmazás képes megjeleníteni; az előnézet általában kisebb felbontású, pixelméretben és/vagy bitmélységben. Az előnézeti fájl többféle formátumban lehet. Az EPS_3 specifikációja három „eszköz-specifikus” előnézeti formátumot sorol fel:

* Apple Macintosh esetén a QuickDraw alkalmazás által használt PICT kép
* DOS számítógépek esetén TIFF bittérkép
* Windows Metafile.

A PICT és a Windows Metafile bittérképes adatokat és vektorgrafikát egyaránt tartalmazhat. Ezenkívül a specifikáció egy nagyon egyszerű, eszközfüggetlen ábrázolást határoz meg egy beágyazott bittérképes előnézeti képhez. Ez az ábrázolás Encapsulated PostScript Interchange Format (EPSI) néven ismert.

Az EPSI előnézet egy ASCII hexadecimális bittérkép, amely néhány PostScript megjegyzés közé van csomagolva azonosítás céljából, és célja, hogy egyszerű és könnyen szállítható legyen. A különböző előnézeti formátumú EPS-fájlok megkülönböztetése érdekében az EPS-specifikációban különböző DOS-fájlkiterjesztéseket és Macintosh-fájltípusokat javasoltak.

### PostScript kód

Az EPS fájlformátumnak legalább a következőket kell tartalmaznia:

* egy fejléc megjegyzés, %!PS-Adobe-3.0 EPSF-3.0
* és egy határolódoboz megjegyzés, %%BoundingBox: llx lly urx ury, amely leírja az illusztráció határait. Ez a négy argumentum a határolókeret bal alsó (llx, lly) és jobb felső (urx, ury) sarkának felel meg.

Egy EPS-fájl nem használhatja a következő operátorok egyikét sem:

* sávos eszköz,
* cleardictstack
* oldal másolása
* törlésoldal
* exitserver
* keretes eszköz
* grestoreall
* initclip
* initgrafika
* initmátrix
* Kilépés
* rendersávok
* setglobal
* oldaleszköz beállítása
* megosztott
* munkakezdés.

## EPS konvertálása más fájlformátumokba

Az EPS-fájlok szabványos képformátumokká konvertálhatók, például [JPG](/hu/image/jpeg/), [PNG](/hu/image/png/), [TIFF](/hu/image/tiff/) és [PDF](/hu/pdf) /) különböző alkalmazásokkal, pl. Adobe Illustrator, Photoshop és PaintShop Pro.

[Biztonsági rés](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) az EPS-fájlokban, az Office 2016, Office 2013, Office 2010 és Office 365 kikapcsolta az EPS-fájlok Office-dokumentumokba való beszúrásának lehetőségét.

## Hivatkozások

* [Encapsulated PostScript – Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

