{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "XSL formázási objektumok", "Fájl", "Kiterjesztés", "Fájlformátum", "Bővíthető stíluslap nyelv"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"További információ az XSLFO fájlformátumról és az API-król, amelyek XSLFO fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Mi az XSL-FO fájl? ##

Az XSL-FO (XSL Formatting Objects) egy hatékony stíluslapnyelv az XML dokumentumok formázásához. A papír és a nyomat korlátos formájának szemantikáját az XSL-FO fejezi ki, ha a méretek rögzítettek. Ellentétben a HTML-lel, amely egy változó méretű böngészőablak határtalan formájának szemantikáját reprezentálja. Az XSL-FO által formázott XML dokumentumokat többnyire PDF fájlok generálására használják. Az XSL (Extensible Stylesheet Language) a funkciókat teljes körű W3C-technológiák halmaza, amelyek célja az XML-dokumentumok formázására és cseréjére való tervezés, valamint a nyelv XSL-FO része. Az XSLT és az XPath szintén az XSL egyéb részei.

Javasoljuk, hogy az XML dokumentumokat először XSL-FO-ba kell átalakítani, a PDF erre a kritériumra példa. A PDF-ben az eredmények az XSLTfirst, majd az XSL-FO formázó használatával jelennek meg. Ily módon az XML dokumentumok véletlenszerűen formázhatók. Bár az XSL-FO kihasználja a Cascading Style Sheet (CSS) tulajdonságok használatának előnyeit, és ott, ahol a valódi formátumhoz szükséges, kiterjeszti azokat, az XSL-FO terminológiája szerint oldalsablonokat tartalmaz, amelyeket oldalmestereknek neveznek. Az XSL-FO a meglehetősen kifinomult dokumentumok formázását is biztosítja, és támogatja az indexgenerálást.

## Történelem és alapfogalmak ##

Utoljára 2012 januárjában frissítették az XSL-FO munkatervezetét, 2013 novemberében pedig bezárták a munkacsoportját. Az XSL-stíluslap az XML-dokumentumok egy osztályának megjelenítését határozza meg azáltal, hogy leírja, hogy az osztály egy példánya hogyan alakul át a formázási szókincset használó XML-dokumentummá. Az XSL-FO egy integrált prezentációs nyelv, és nem tartalmaz HTML-ben használt szemantikai jelöléseket. Ezenkívül ez a nyelv a dokumentum összes adatát magában tárolja, ellentétben a CSS-sel, amely megváltoztatja a külső HTML vagy XML dokumentumok alapértelmezett beállításait.

Az XSL-FO használatának általános kritériuma, hogy a felhasználó XML nyelven írjon egy dokumentumot, ne pedig FO-ban írjon. Ezt követően XSLT transzformáció történik. Ez az XSLT transzformáció felelős az XML XSL-FO-vé való átalakításáért. Amint az XSL-FO dokumentum létrejön, átadják egy FO processzornak nevezett alkalmazásnak. Az FO-feldolgozók felelősek azért, hogy ezt a dokumentumot olvashatóvá és nyomtathatóvá alakítsák. A PDF-fájlok vagy a PS-ek példák az XSL-FO leggyakoribb kimenetére. De ez nem jelenti azt, hogy az FO processzor csak ezt a két formátumot tudja előállítani kimenetként. Egyes FO processzorok kiadhatnak RTF fájlokat, vagy akár egy ablak is megjelenhet a felhasználó grafikus felületén, ez az ablak az oldal sorrendjét és azok tartalmát jeleníti meg.

Az XSL-FO dokumentum abban az értelemben különbözik a PDF-től vagy a PS-től, hogy végső soron nem határozza meg a szöveg elrendezését a különböző oldalakon. Talán stílust ad az oldalaknak, és meghatározza a tartalom megjelenítési helyeit. Ezenkívül egy FO processzor a szöveget az FO dokumentumban meghatározott határokon belül rendezi. Ez a specifikáció még azt is lehetővé teszi, hogy a különböző FO processzorok az eredményül létrehozott oldalaknak megfelelően viselkedjenek. Ilyen viselkedés például az elválasztás, kevés FO processzor képes elválasztani a szavakat, hogy helyet takarítson meg egy sor szakadása esetén, míg egyes processzorok nem választják ezt a lehetőséget. A processzoroktól függ, hogy a követelményeknek megfelelő különböző elválasztási algoritmusokat választanak-e. Ezek az elválasztási algoritmusok nagyon egyszerűek vagy bonyolultabbak lehetnek. Egyes helyzetekben az XSL-FO specifikáció kifejezetten tiltja az FO processzorokat, bizonyos fokú választási lehetőséget az elrendezéssel összefüggésben.

Az FO processzorok közötti eltérések eltérő eredményeket generálnak, amivel a processzorok gyakran nem foglalkoznak. Mivel az XSL-FO általános fókusza a lapozott/nyomtatott dokumentumok előállítása. Maguk az XSL-FO dokumentumok jellemzően közvetítőként működnek, fő funkciójuk a PDF fájlok vagy a terjesztendő kimenetként nyomtatható dokumentum létrehozása. A HTML/CSS vagy XSL-FO esetén a PDF-nek végeredményként való szétosztása a formázási nyelv bevitele helyett azt jelzi, hogy a fogadókat nem érinti a sokoldalúság, amely a formázási nyelv értelmezői közötti különbségek miatt jön létre. Másrészt nyilvánvaló, hogy nincs egyszerű módja annak, hogy egy dokumentum ki tudja elégíteni a címzettek különböző igényeit, például változó oldalméretet vagy kívánt betűméretet, vagy oldalra vagy nyomtatásra szabva.

## XSLFO fájlformátum ##

Az SL-FO dokumentumok alapvetően XML dokumentumok, de nem követnek semmilyen sémát. Helyette az SL-FO dokumentumok a saját nyelvük specifikációjában meghatározott szintaxist követik. Minden XSL-FO dokumentumban két rész szükséges:

1. Egy szakasz, amely megadja a címkézett oldalelrendezések listáját.
1. Egy szakasz a dokumentumadatok minden részletével, jelöléssel, amely meghatározza a tartalom megjelenítését a különböző oldalakon különböző oldalelrendezéseken keresztül.

Az oldal tulajdonságait az oldalelrendezések említik, amelyek meghatározhatják a szöveg szervezetét, hogy megfeleljenek az adott nyelvre vonatkozó konvencióknak. Továbbá az oldal mérete, margói és oldalsorrendje (amely a páratlan és páros oldalak különböző tulajdonságait szankcionálja) szintén az oldalelrendezések által meghatározott.

A dokumentum adatrésze folyamatok sorozatára van felosztva, ahol mindegyik folyamat egy oldalelrendezéshez kapcsolódik. A folyamatok egy listát tartalmaznak a blokkokról. Ez a blokkok listája tartalmazhat soron belüli jelölési funkciókat vagy szöveges adatok listáját, esetleg mindkettőt egyszerre. A dokumentum margóin az oldalszámok vagy a fejezetek címsorai is megjelenhetnek. Mind a blokkok, mind a beágyazott elemek funkcionalitása ugyanaz marad, mint a CSS-ben, de bizonyos kitöltési és margószabályok eltérnek az FO és a CSS között.

Az oldaltájolás iránya teljes egészében a blokkok és sorközök kiterjesztésére van megadva, így az FO dokumentumok az angoltól eltérő nyelveken is működnek. Az FO specifikáció nyelve a kezdő és vége szavakat használja, nem pedig balra és jobbra az irányok leírásához. Az XSL-FO alapvető tartalomjelölési és lépcsőzetes szabályai a CSS-ből származnak. Az XSL-FO nyelve elfogadja a következő specifikációkat.

## Több oszlop ##

Egy oldalnak több oszlopa és blokkja is lehet, és alapértelmezés szerint egyik oszlopról a másikra terjedhet. Több oldal eltérő szélességű és oszlopszámú lehet. Minden FO-jellemző követi a többoszlopos oldal korlátait.

### Listák ###

Az XSL-FO listát két blokkkészlet alkotja, amelyek pofa szerint vannak elrendezve. Koncepcionálisan a listában a bal oldali blokk egy számot, egy felsorolást vagy egy szövegsort jelöl, míg a jobb oldali blokk a várt módon működhet. Az XSL-FO listák számozását általában az XSLT végzi.

### Táblázatok ###

Az FO-tábla hasonló a HTML/CSS-táblához. A felhasználó minden egyes cellához kiválaszthatja az adatsorokat, a stílusinformációkat és a háttérszínt. Különálló stílusinformációk felhasználásával a felhasználónak jogában áll az első sort táblázatfejlécként kiválasztani. Az FO processzor explicit módon tájékozódhat az egyes oszlopok helymeghatározásáról, vagy automatikusan beillesztheti a szöveget a táblázatba.

### Indexelés ###

Az XSL-FO 1.1 olyan funkciókkal rendelkezik, amelyek segítik az index létrehozását a megfelelően megjelölt elemekre való hivatkozással.

### Előnyök ###

* Tartalmi alapú közzétételhez megfelelő
* Egyszerű használat
* Alacsony költségű

## Referenciák ##

* [Mi az XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [XSL-formátumú objektumok](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

