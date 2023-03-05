{
  "date" : "2021-01-21",
  "keywords" :[ "ai fájl", "ai fájlformátum", "mi az ai fájl", "fájl", "ai példa", "ai fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI – Adobe Illustrator grafikai fájl",
  "description":"További információ az AI fájlformátumról és az API-król, amelyek AI-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Mi az AI fájl?

Az .ai kiterjesztésű fájl egy Adobe Illustrator Artwork fájl, amely egyetlen oldalon vektorgrafikát tartalmaz. pontokat használ a képadatok megjelenítéséhez szükséges útvonalak létrehozásához, így megóvja a képminőség elvesztését a nagyításkor. Az AI fájlformátum alapja a PGF fájlformátum, amely hasonló az AI fájlokhoz. Az AI formátumot főként logók és nyomtatott médiák esetében használják, és eredeti verzióit az [EPS](/hu/image/eps/) fájlokhoz hasonlónak tekintették. Az AI-fájlok megnyithatók az Adobe Illustrator, az Adobe Acrobat DC, a PaintShop Pro és a CorelDraw Graphics eszközökkel.

## AI fájlformátum

A mesterséges intelligencia az Adobe Illustrator szabadalmaztatott fájlformátuma, és a PGF-hez hasonló kettős elérési utat alkalmaz az EPS-kompatibilis fájlok mentésére. Az [Adobe Illustrator fájlformátum specifikációi](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) részletes leírást adnak fejlesztői hivatkozás a fájlformátum belső részleteihez. Minden Az Adobe Illustrator által létrehozott dokumentumok (fájlok) PostScript nyelvű dokumentumok, és két fő részük van, amelyek megfelelnek a Dokumentumszerkezeti Egyezményeknek: egy "prolog" és egy "script".

### Prolog

A prolog szakasz a fájl értelmezéséhez szükséges információkat tartalmazza. Példa erre a határolókeret, amely az oldalon lévő összes jelet tartalmazza. Erőforrás-információkat is tartalmaz, például betűtípusokat és eljárásdefiníciókat. Ezek az erőforrások logikailag procset-nek nevezett halmazokba vannak csoportosítva, és explicit metódusokat tartalmaznak az eljárások inicializálására és leállítására.

### Szkript

Az oldalon található grafikai elemeket a szkript írja le. A szkript hivatkozásokat tartalmaz a prolog operátoraira és eljárásaira, valamint operandusokat és adatokat. A szkript három logikai része a következőket tartalmazza:

* Setup Sequence – amely inicializálja és aktiválja a prologban meghatározott erőforrásokat
* Leíró operátorok sorozata
* Előzetes, amely deaktiválja az erőforrásokat

A szkript operátorai a prologban a procsetek által meghatározott nyelven írt grafikus elemek sorozatai. Ezek a sorozatok adatelemek gyűjteményeiből, grafikus attribútum-definíciókból és a procsetekben definiált eljárások hívásaiból állnak.

### Objektumcímkék

Az objektumcímkék egyéni információk csatolására szolgálnak egy Adobe Illustrator művészeti objektumhoz. A címkék a következőkből állnak:

* Címkeazonosító
* Címke típusa
* Adatok

## Hivatkozások
* [Az Adobe Illustrator fájlformátum specifikációi](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [AI fájlformátum a PaintShopPro által](https://www.paintshoppro.com/en/pages/ai-file/)

