{
  "date" : "2019-10-11",
  "keywords" :[ "md fájl", "md fájl formátum", "mi az md fájl", "fájl", "md példa", "md fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - MarkDown nyelvi fájl",
  "description":"További információ az MD fájlformátumról és az MD-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az MD fájl?

A Markdown nyelvi dialektusokkal létrehozott szövegfájlok **.md** vagy **.MARKDOWN** kiterjesztéssel kerülnek mentésre. Az MD-fájlok egyszerű szöveges formátumban kerülnek mentésre, amely Markdown nyelvet használ, amely szövegközi szimbólumokat is tartalmaz, amelyek meghatározzák a szöveg formázását, például behúzásokat, táblázatformázást, betűtípusokat és fejléceket. Az MD fájlok a Markdown nevű programmal HTML-be konvertálhatók. A Markdown nyelvet John Gruber adta ki.

Az MD fájlok fejlesztői fájlokként is besorolhatók, amelyeket leginkább a Markdown használ szöveges fájlok HTML-verzióvá konvertálására, hogy a felhasználók könnyen olvasható és írható fájlokat készíthessenek. Az alábbi alkalmazások képesek megnyitni egy .md fájlt:

* Microsoft Jegyzettömb
* Jegyzettömb2
* Apple TextEdit
* Microsoft WordPad

Figyelmeztetés, hogy ne nevezze át az .md fájlok kiterjesztését. Ha igen, ez nem fogja megváltoztatni a fájltípust, mert speciális konvertáló szoftverek állnak rendelkezésre a fájlok egyik típusról a másikra történő megváltoztatására. Mint fentebb tárgyaltuk, az .MD fájlok a Markdown nyelvi szoftverrel létrehozott fájlok kiterjesztései. A **Markdown** egy [könnyű jelölőnyelv](https://en.wikipedia.org/wiki/Lightweight_markup_language), amelyet egyetlen célra szántak az interneten lévő szöveg egyszerű szöveges formázási szintaxissal történő formázására. Legyen világos, hogy a Markdown nem helyettesíti a HTML-t, mert a szintaxisa nagyon kicsi, és a HTML-címkék nagyon kis részhalmazát tartalmazza. A Markdown hátterében az áll, hogy megkönnyítse a próza olvasását, írását és szerkesztését. Más szóval azt mondhatjuk, hogy a HTML egy publikációs formátum, míg a Markdown egy írási formátum.

A Markdown mára a világ egyik legnépszerűbb jelölőnyelve. A Microsoft Word használata során a szavak és kifejezések formázása a gombokra kattintva történik, és a változások azonnal láthatóak. De Markdown nem ilyen. A Markdown formázott fájl létrehozásakor a Markdown szintaxis hozzáadódik a szöveghez, hogy jelezze, mely szavak és kifejezések nézhetnek ki eltérően. Például egy címsor megjelenítéséhez egy számjel kerül hozzá (pl. # Heading One). Félkövér mondat készítéséhez két csillagot kell hozzáadni előtte és utána (pl. **ez a szöveg félkövér**). A Markdown szintaxisa a szövegben való tartózkodás után látható.

## Rövid története

John Gruber és Aaron Swartz 2004-ben megalkotta a Markdown nyelvet azzal az ötlettel, hogy lehetővé tegye az emberek számára, hogy „könnyen olvasható és írható egyszerű szöveges formátumban írjanak, és lehetőség legyen XHTML-re vagy HTML-re konvertálni. Kialakításának célja az olvashatóság – a nyelv úgy olvasható, ahogy van, anélkül, hogy úgy nézne ki, mintha fel lett volna címkézve vagy formázási utasításokkal egészítették ki, ahogy az olyan jelölőnyelvekben, mint az RTF vagy a HTML, ahol a címkék és a formázási utasítások nyilvánvalóak. Az alapvető inspiráció a meglévő konvenciók használata az egyszerű szöveg e-mailben történő megjelölésére.

Azóta a Markdown-t mások is újra implementálták, mint egy Perl [modulban](https://en.wikipedia.org/wiki/Modular_programming), amely elérhető a [CPAN] oldalon (https://en.wikipedia.org/ wiki/CPAN) és számos más programozási nyelven. [BSD-stílusú licenc](https://en.wikipedia.org/wiki/BSD_license) alatt terjesztik, és több [tartalomkezelő rendszerhez](https://) tartozik, vagy beépülő modulként érhető el. hu.wikipedia.org/wiki/Content_management_system).

## Műszaki adatok

Amikor valamit Markdown-ban írunk, a szöveg először egyszerű szöveges fájlban kerül tárolásra .md vagy .markdown kiterjesztéssel, majd a Markdown-alkalmazást, például a Dillingert használják a Markdown-fájl feldolgozásához a Markdown-formátumú szöveg HTML-formátumba konvertálásához a weben való megjelenítéshez. böngészők. A Markdown alkalmazások egy //Markdown processzort// (amelyet „elemzőnek” vagy „implementációnak” is neveznek) használnak a Markdown formátumú szöveg átvételéhez és HTML formátumba történő kiadásához. A folyamat folyamatábrája a következő:

Röviden, ez egy négy lépésből álló folyamat, az alábbiak szerint:

1. Először Markdown fájlok létrehozása szövegszerkesztővel vagy Markdown alkalmazással .md vagy .markdown kiterjesztéssel.
1. A Markdown fájl ezután megnyílik egy Markdown alkalmazásban.
1. A Markdown alkalmazás a Markdown fájl HTML-dokumentummá konvertálására szolgál.
1. A HTML-fájl ezután megtekinthető egy webböngészőben, vagy a Markdown alkalmazás segítségével más fájlformátumba, például PDF-be konvertálhatja.

A Markdown segítségével gyorsan és egyszerűen készíthet jegyzeteket, tartalomírást készíthet weboldalakhoz, nyomtatható dokumentumokat készíthet, könyvek kiadásához, prezentációk generálásához és dokumentumok elkészítéséhez.

A leárazásban szereplő verziók némelyike jelentős hatással volt más verziókra, olyannyira, hogy gyakran látni fogjuk őket más verziók részeként idézve. Pl. a könyvtárak említik a CommonMark (GFM) támogatását. Vessünk egy rövid pillantást ezekre.

### GFM
A Markdown annyira népszerű a fejlesztők körében, mert a Github nyílt forráskódú megosztási platform elfogadta és kiterjesztette a nyelvet a Github Flavoured Markup (GFM) nevű verziójával, amely elkerített kódblokkokat, URL-ek linkelést, áthúzást, táblázatokat és teendőket tartalmaz.

### CommonMark
A Markdown fejlesztői a közelmúltban megpróbálták szabványosítani a markdown-t, és összefogtak, hogy elkészítsék a nyelvre vonatkozó verziót, teszteket és dokumentációt, amely erősebb és a CommonMark nevet kapta. Ez a formátum egy kicsit új, és nem támogat sok funkciót, de hamarosan sok MultiMarkdown funkcióval bővül.

### Multi-Markdown
A Multi-Markdown különféle funkciókat adott a nyelvhez, amelyeket más verziók is támogatnak. Eredetileg Perlben írták, de később C-be költöztek. Támogatja az elkerített kódblokkokat, a szintaxis kiemelését, a táblázatokat, a metaadatokat, a töredékeket/kereszthivatkozásokat, a lábjegyzeteket, az áthúzást, a definíciós listákat, a matematikát.

## Hivatkozások

* [Mastering MarkDown](https://guides.github.com/features/mastering-markdown/)

