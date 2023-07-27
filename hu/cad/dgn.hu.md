{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "File", "Format", "Open", "Read", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD tervezési fájlformátum",
  "description" :"További információ a DGN-fájlformátumról és az API-król, amelyek DGN-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Mi az a DGN fájl?

A .dgn (Design) kiterjesztésű fájl egy rajzfájl, amelyet CAD-alkalmazások (például MicroStation és Intergraph Interactive Graphics Design System) hoztak létre és támogatnak. Építési projektek, például autópályák, hidak és épületek terveinek létrehozására és mentésére használják. A formátum hasonló az Autodesk [DWG](/hu/cad/dwg/) fájlformátumához, és versenytársának tekinthető. A DNG-fájlok Intergraph szabványos fájlformátumként vagy V8 DGN-ként menthetők. A DGN számos más formátumba konvertálható, például DWG, [BMP](/hu/image/bmp/), [JPEG](/hu/image/jpeg/), [PDF](/hu/pdf/), [GIF](/hu/image/) gif/) és mások. Megnyitható az Autodesk AutoCAD, a Bentley View és a Bentley Systems MicroStation programmal, valamint más szoftveralkalmazásokkal, mint például a Corel PaintShop Photo Pro és az IMSI TurboCAD Deluxe verziókkal.

## V8 DGN fájlformátum

A MicroStation V8 DGN fájl egy vagy több modellből áll. A modell egy tároló az elemek számára. A V8 DGN eltávolítja az összes fájlformátum-alapú megszorítást, amely a MicroStation korábbi verzióiban volt. Az alábbiakban felsoroljuk a DGN fájlformátum fejlesztéseit.

* A DGN-fájl szintek számának korlátozása megszűnt, és minden szint elemként kerül elnevezésre és tárolásra.
* A DGN fájl maximális fizikai méretére nincs korlátozás, és csak az operációs rendszer korlátozza (például az NT korlátja 4 GB)
* Egyetlen elem maximális mérete 128 KB.
* A cellák maximális méretére nincs korlátozás.
* A cellanevek legfeljebb 500 karakterből állhatnak.
* A DGN-fájlhoz csatolható hivatkozások száma nincs korlátozva.
* Egy vonalláncnak, alakzatnak vagy pontgörbének legfeljebb 5000 csúcsa lehet.
* Egy összetett láncban vagy összetett alakzatban nincs korlátozva a komponensek száma.
* Egy DGN-fájlban nincs korlátozva a grafikus csoportok száma.
* A kerítés párhuzamos a kilátással, amelyben elhelyezték.
* Egy sor szöveg 65 535 karaktert tartalmazhat.
* A szövegcsomópontok maximális méretére nincs korlátozás.
* Egy DGN-fájlban nincs korlátozva a szöveges csomópontok száma.
* Minden elemnek egyedi 64 bites azonosítója van, amely nem változik az elem életciklusa során.
* Minden elemhez tartozik egy időbélyeg, amely a legutóbbi módosítás időpontját jelzi.

## Hivatkozások

* [DNG – a Wikipedia által](https://en.wikipedia.org/wiki/DGN)
* [MicroStation V8 DGN fájlformátum](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

