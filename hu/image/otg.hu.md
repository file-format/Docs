{
  "date" : "2020-01-10",
  "keywords" :[ "otg fájl", "otg fájlformátum", "mi az otg fájl", "fájl", "otg példa", "otg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument rajzsablon fájlformátum",
  "description":"További információ az OTG fájlformátumról és az API-król, amelyek OTG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Mi az OTG fájl?

Az OTG-fájl egy rajzsablon, amelyet az OpenDocument szabvány használatával hoznak létre, amely követi az OASIS Office Applications [1.0 specifikációját](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Ez a vektorkép rajzelemeinek alapértelmezett elrendezését jelenti, amely felhasználható a fájl tartalmának továbbfejlesztésére. Az OTF fájlok olyanok, mint bármely más OpenDocument formátum alapú fájlok, amelyek XML formátumon alapulnak a dokumentum tartalmának megjelenítésére. Az OTF-fájlok bármely szöveges vagy szabványos XML-szerkesztőben megtekinthetők.

## OTG fájlformátum specifikációi ##

Az OTG fájlformátum az OpenDocument XML formátumon alapul, amely jól bevált sémával rendelkezik. Az OpenDocument formátum egyes összetevőinek szerkezetét egy olyan elem képviseli, amely társított attribútumokkal rendelkezik, és minden dokumentumtípusban, például szöveges dokumentumban, táblázatban vagy rajzfájlban közös. Az OTG rajzsablonként széles körben használja a grafikus tartalom specifikációit, amelyek a következőket tartalmazzák:

* Továbbfejlesztett oldalfunkciók grafikus alkalmazásokhoz
* Alakzatok rajza
* Keretek
* 3D formák
* Egyedi forma
* Bemutató formák
* Bemutató animációk
* SMIL bemutató animációk
* Bemutató események
* Jelen szövegmezők
* Prezentációs dokumentum tartalma

### Továbbfejlesztett oldalfunkciók grafikus alkalmazásokhoz ###
#### Kiosztó mester ####

A Handout Master elem egy sablon a szórólapok automatikus létrehozásához az ilyen oldalak nyomtatását támogató alkalmazásokhoz.
Az attribútumok, amelyek a `<style:handout-master>` elemek a következők:

|Elrendezés|Attribútum|Leírás
---|---|---|
|Prezentációs oldal elrendezése|presentation:presentation-page-layout-name|Hivatkozások ide: `<style:presentation-page-layout>`  attribútum
|Oldalelrendezés|`style:page-layout-name` | Meghatároz egy oldalelrendezést, amely tartalmazza a szóróanyag mesteroldalának méretét, szegélyét és tájolását.
|Oldalstílus|`draw:style-name`|További formázási attribútumokat rendel a tájékoztató mesteroldalhoz egy rajzoldalstílus hozzárendelésével.|
|Fejléc nyilatkozat| `presentation:use-header-name`| Megadja annak a fejlécmező-deklarációnak a nevét, amely a tájékoztató mesteroldalon megjelenő összes fejlécmezőhöz használatos.
|Lábléc nyilatkozat| display:use-footer-name|Meghatározza a láblécmező-deklaráció nevét, amely a tájékoztató mesteroldalán megjelenő összes láblécmezőhöz használatos.
|Dátum és idő deklaráció|use-date-time-name|Meghatározza a dátum-idő meződeklaráció nevét, amely a tájékoztató mesteroldalán megjelenő összes dátum-idő mezőhöz használatos.

### Alakzatok rajzolása ###
Az OpenDocument formátum számos rajzi formát támogat, amelyeket bármilyen típusú dokumentum használhat.

|Alak|Kapcsolódó attribútumok| elemeket
---|---|---|
Téglalap - `<draw:rect>` |Pozíció, méret, stílus, réteg, Z-index, azonosító, feliratazonosító, szöveghorgony, táblázat háttere, rajz végpozíciója, lekerekített sarkok|cím, hosszú leírás, eseményfigyelők, ragasztópontok, szöveg
Vonal `<draw:line>` |Stílus, Réteg, Z-index, azonosító, feliratazonosító és átalakítás, szöveghorgony, táblázat háttere, rajzolás végpontja, kezdőpont, végpont|cím, hosszú leírás, eseményfigyelők, ragasztópontok, szöveg
Vonallánc `<draw:polyline> `| Pozíció, Méret, Nézetmező, Stílus, Réteg, Z-index, ID, Feliratazonosító és átalakítás, Szöveghorgony, táblázat háttere, rajzolás végpozíciója, Pontok| Cím, hosszú leírás, eseményfigyelők, ragasztópontok, szöveg
Sokszög `<draw:polygon> `|Pozíció, Méret, Nézetmező, Stílus, Réteg, Z-index, ID, Feliratazonosító és átalakítás, Szöveghorgony, táblázat háttér, rajzolás végpontja, Pontok|Cím, Hosszú leírás, Eseményfigyelők, Ragasztópontok, Szöveg
|Szabályos sokszög `<draw:regular-polygon> `|Pozíció, méret, stílus, réteg, Z-index, azonosító, feliratazonosító és átalakítás, szöveghorgony, táblázat háttere, rajz végpontja, konkáv, sarkok, élesség|cím, hosszú leírás, eseményfigyelők, ragasztópontok, szöveg
|Paht `<draw:path> `|Pozíció, Méret, Nézetmező, Stílus, Réteg, Z-index, ID, Feliratazonosító és átalakítás, Szöveghorgony, táblázat háttere, rajzolás végpozíciója, Útvonal adatok| Cím, hosszú leírás, eseményfigyelők, ragasztópontok, szöveg

### Keretek ###
A keret a rajzdokumentumban egy téglalap alakú tároló, amely szövegdobozokat, képeket vagy objektumokat tartalmaz. A keretek további funkciókat is támogatnak, például kontúrokat, képtérképeket és hiperhivatkozásokat. Egy keret egy objektumot és egy képet is tartalmazhat, így lehetővé válik egy objektum többszöri megjelenítése. Az alkalmazások a megfelelő elemet a legjobb támogatás alapján jelenítik meg.

A keretek a következőket tartalmazhatják:
* Szövegdobozok
* OpenDocument formátumban vagy objektumspecifikus bináris formátumban megjelenített objektumok
* Képek
* Kisalkalmazások
* Beépülő modulok
* Lebegő keretek

A dokumentumban egy keret található az alábbiak szerint.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Hivatkozások ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

