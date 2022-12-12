{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "file", "file format", "Page Description Language", "Scalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az SVG fájlformátumról és az SVG-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"What is an SVG file?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Mi az SVG fájl? ##

Az SVG-fájl egy skaláris vektorgrafikus fájl, amely XML-alapú szövegformátumot használ a kép megjelenésének leírására. A Scalable szó arra a tényre utal, hogy az SVG különböző méretekre méretezhető anélkül, hogy minősége romlana. Az ilyen fájlok szöveges leírása függetlenné teszi őket a felbontástól. Ez az egyik leggyakrabban használt formátum a weboldal készítésére és a grafikák nyomtatására a méretezhetőség érdekében. A formátum azonban csak kétdimenziós grafikákhoz használható. Az SVG-fájlok szinte minden modern böngészőben megtekinthetők/megnyithatók, beleértve a Chrome-ot, az Internet Explorert, a Firefoxot és a Safarit.

## Rövid története ##

Az SVG specifikációkat 1999 óta nyílt szabványként a World Wide Web Consortium (W3C) bocsátja rendelkezésre. Ezt megelőzően 1998-ig hat különböző formátumú hasonló fájlformátum-specifikációt nyújtottak be a W3C-nek. 2011-ben frissítették a specifikációkat, és 1.1-es verziót kapott . 2016-ban az SVG 2 újabb verzióként jelent meg, amely az SVG 1.1-ben található funkciókon kívül további funkciókat is tartalmaz.

## Fájlformátum specifikációi ##

Az SVG Document Object Model (DOM) lefekteti az összes olyan specifikáció és interfész alapjait, amelyek megfelelnek a specifikációk adott szakaszainak. Az SVG-megtekintőknek megvalósítaniuk kell az SVG DOM interfészt a W3C specifikációiban meghatározottak szerint. DOM-ja több interfészt tesz elérhetővé a különböző adattípusokhoz és elemekhez.

### SVG alakzatok ###

Az SVG-nek van néhány előre definiált alakeleme, amelyeket a fejlesztők használhatnak:

* Téglalap<rect>
* Kör<circle>
* Ellipszis<ellipse>
* Vonal<line>
* Vonallánc<polyline>
* Sokszög<polygon>
* Pálya<path>

Ezen formák és specifikációk alapján az SVG funkcionális területei a következők.

**Paths** – Az útvonalak az egyszerű és összetett alakzatok körvonalainak ábrázolására szolgálnak. A kódolások a művelet jellegének meghatározására szolgálnak. Például az M a Move To, az L a Line To, a Z egy elérési út lezárására és így tovább.

**Alapalakzatok** – Egyenes vonalú pályák és egymáshoz kapcsolódó egyenes szakaszok (polivonalak) sorozatából álló pályák, valamint zárt sokszögek, körök és ellipszisek rajzolhatók. A téglalapok és a lekerekített sarkú téglalapok szintén szabványos elemek.

**Szöveg** – A szövegábrázolás XML-karakteradatként fejeződik ki, ahol számos vizuális effektus alkalmazható a szövegre. A specifikációk lehetővé teszik a kétirányú szövegek, függőleges szövegek és karakterek kezelését egy ívelt útvonal mentén.

**Festés** – A formák kitölthetők és/vagy körvonalazhatók színnel, színátmenettel vagy mintával, ami lehetővé teszi, hogy átlátszatlan legyen, vagy bármilyen fokú átlátszóságot biztosítsanak. A vonalvégi jellemzőket, például a nyílhegyeket vagy a sokszög csúcsaiban megjelenő szimbólumokat Markerek ábrázolják.

**Szín** – Az SVG specifikációk lehetővé teszik a színek alkalmazását az összes látható SVG elemre, akár közvetlenül, akár kitöltéssel, körvonallal és egyéb tulajdonságokkal. Különböző színkódok használhatók a megadáshoz, például fekete vagy kék, hexadecimális ábrázolás, decimális vagy RGB formátum százalékos aránya.

**Szétátmenetek és minták** – Az SVG-fájl alakzatai kitölthetők vagy körvonalazhatók egyszínű színekkel, színátmenetekkel vagy ismétlődő mintákkal.

**Szűrőeffektusok** – Valójában grafikus műveletek sorozata, amelyeket az adott forrás vektorgrafikára alkalmaznak a módosított eredmény elérése érdekében.

**Interaktivitás** – A felhasználók a fókusz megváltoztatásával, az egérkattintással, a kép görgetésével vagy nagyításával interakcióba léphetnek az SVG-fájlokkal. Az interaktivitás lehetővé teszi, hogy az SVG-képek sokféle módon interakcióba lépjenek a felhasználókkal, amint azt fentebb említettük.

**Hivatkozás** – Lehetséges, hogy az SVG-képek hiperhivatkozást tartalmaznak más dokumentumokra. Ez az XML Linking Language vagy az XLink segítségével érhető el. Ez lehetővé teszi speciális nézetállapotok létrehozását, amelyek egy adott terület nagyítására/kicsinyítésére vagy a nézet egy adott elemre való korlátozására szolgálnak.

**Szkriptek** – A HTML-hez hasonlóan az SVG-dokumentumok minden aspektusa elérhető a szkriptek használatával történő manipulációhoz. Az SVG DOM objektumok útmutatást adnak ennek eléréséhez az SVG elem és attribútum használatával. A szkriptek `script' címkeelemekbe vannak zárva, és szükség szerint mutató-, billentyűzet- vagy dokumentumeseményekre adott válaszként futhatnak.

**Animáció** – A DOM elemek<animate> ,<animateMotion> és<animateColor> lehetővé teszi animáció felvételét az SVG-tartalomhoz. Természetesen ez nem érhető el szkriptek és beépített időzítők használata nélkül. Ezek az animációk lehetnek folyamatosak, ciklusba helyezhetők, illetve ismétlődnek, ugyanakkor reagálnak a felhasználói eseményekre.

**Betűtípusok** – Az SVG-ben lévő szöveg külső betűtípus-fájlokra, például rendszer-betűtípusokra hivatkozhat. Ilyen betűtípusok hiányában az SVG-ben lévő szöveg nem jelenik meg a kimeneten. Ezt úgy lehet kiküszöbölni, ha a szükséges karakterjeleket beépítjük egy ilyen fájlba betűtípusként, amelyet aztán a<text> elem.

## Példák ##
A következő sorok azt mutatják, hogyan ábrázolják a kört az SVG-szkript használatával.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

A következő kódsorok bemutatják, hogyan kell használni a<text> blokk a szöveg SVG formátumba történő megjelenítéséhez.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Hivatkozások ##

* [W3C SVG specifikációk](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG – Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

