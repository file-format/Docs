{
  "date" : "2019-10-11",
  "keywords" :[ "chm", "chm fájl", "chm fájlformátum", "chm fájltípus", "fájl", "típus", "mi az a chm fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - Összeállított HTML súgófájl formátum",
  "description" :"További információ arról, hogy mi az a CHM-fájl és az API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a CHM fájl?

A CHM fájlformátum a Microsoft **[HTML](/hu/web/html/)** súgófájlja, amely HTML-oldalak gyűjteményéből áll. Indexet biztosít a témakörök gyors eléréséhez és a súgódokumentum különböző részeihez való navigáláshoz. A CHM fájl tartalma a megadott keresési opcióval kereshető. A CHM a Microsoft által védett online súgófájl formátum, amelyet gyakran használnak szoftverdokumentációhoz. Ezenkívül számos más alkalmazásban is használják, például képzési útmutatókban, interaktív könyvekben és elektronikus hírlevelekben. A legtöbb modern Microsoft fejlesztői környezet támogatja a CHM-dokumentáció létrehozását az alkalmazásban elérhető információkból.

A CHM fájlformátum egyedülálló képessége, hogy kombinált tartalomjegyzéket és indexet valósítson meg, megkülönbözteti a többi szabványos HTML oldaltól. Az előállított CHM fájl viszonylag kis méretű, ezért könnyen terjeszthető szoftvercsomagokkal. A súgószerkesztő eszköz, a HTML Help Workshop könnyen használható rendszert biztosít a súgóprojektek és a kapcsolódó fájlok létrehozásához és kezeléséhez. A CHM-fájlok szöveget, képeket és hivatkozásokat tartalmazhatnak; megtekinthető webböngészőben; a Windows és más programok online súgóként használják.

## CHM fájlformátum

A generált CHM-fájl végleges formája a súgórendszer kialakításától függ, és attól, hogy egy alkalmazáshoz vagy egy webhelyhez szánják-e. A CHM-fájl támogatja az adattömörítést LZX-tömörítéssel a tömörített HTML-fájlok létrehozásához. Beépített keresőmotorral rendelkezik a tartalom gyors kereséséhez, valamint több .CHM fájl egyesítésére is. A CHM-fájl HTML-fájlok készletéből, egy hivatkozott tartalomjegyzékből és egy indexfájlból áll.

### HTML fájlok

Akár egy programmal, akár a weben hoz létre súgótémákat a terjesztéshez, az Ön által készített dokumentumok egy speciális formázási nyelven, a Hypertext Markup Language (HTML) néven jönnek létre. A HTML témafájlok .htm vagy .html kiterjesztésűek.

Bár minden általad készített súgótémakör vagy weboldal szöveget, grafikát vagy animált képeket tartalmazó dokumentumnak tűnik, a .htm fájlok valójában szöveges dokumentumok, amelyek speciális HTML formázási kódokkal rendelkeznek. Ezek a kódok, az úgynevezett címkék, megmondják a böngészőnek, hogyan jelenítse meg az egyes oldalakat. Csak a témában vagy weboldalon megjelenő szöveg van ténylegesen a .htm fájlban. A megjelenő grafika, hangok, animált képek vagy egyéb elemek külön fájlok, amelyekre a HTML-fájl mutat. A böngésző lemásolja vagy letölti a grafikákat, hangokat vagy más elemeket, amikor látja az erre felszólító címkéket.

### Tartalomjegyzék (TOC)
A súgó tartalomjegyzék (.hhc) fájl egy HTML-fájl, amely tartalmazza a tartalomjegyzék témacímeit. Amikor a felhasználó megnyitja a tartalomjegyzéket egy összeállított súgófájlban (vagy egy weboldalon), és rákattint egy témakör címére, megnyílik az adott címhez tartozó HTML-fájl.

### Indexfájl
Az indexfájl (.hhk) egy HTML-fájl, amely tartalmazza az indexhez tartozó indexbejegyzéseket (kulcsszavakat). Amikor a felhasználó megnyitja az indexet egy összeállított súgófájlban vagy egy weboldalon, és rákattint egy kulcsszóra, megnyílik a kulcsszóhoz társított HTML-fájl.

## HTML Súgó komponensek

A HTML Help több összetevőből áll. Ezek a következők:

* `HTML Help Workshop`: egy könnyen használható grafikus felülettel rendelkező súgószerkesztő eszköz projektfájlok, HTML-témafájlok, tartalomfájlok, indexfájlok és minden egyéb létrehozásához, ami egy online súgórendszer vagy webhely összeállításához szükséges. .
* `HTML Help ActiveX-vezérlő`: egy kicsi, moduláris program, amellyel a súgónavigációt és a másodlagos ablakfunkciókat HTML-fájlba illesztheti.
* `The HTML Help Viewer`: egy teljesen működőképes és testreszabható, három ablaktáblás ablak, amelyben online súgótémak jelenhetnek meg.
* "Microsoft HTML Help Image Editor": egy online grafikus eszköz képernyőképek készítéséhez; valamint képfájlok konvertálására, szerkesztésére és megtekintésére.
* `The HTML Help Java Applet`: egy kicsi, Java-alapú program, amely ActiveX-vezérlő helyett használható súgónavigáció beillesztésére egy HTML-fájlba.
* "A HTML súgó futtatható programja": az a program, amely megjeleníti és futtatja a súgót, ha rákattint egy lefordított súgófájlra.
* `The HTML Help compiler`: az a program, amely a projektet, a tartalmat, az indexet, a témakört és más fájlokat egy lefordított súgófájlba fordítja.
* `The HTML Help Authoring Guide`: egy online útmutató, amelynek célja, hogy segítse a szerzőket a HTML Súgó használatában a súgórendszer kialakításában. Az útmutató egy teljes HTML-súgó-referenciát is tartalmaz a fejlesztők számára, és egy HTML-címke hivatkozást a szerzők számára.

## Hivatkozások

* [Microsoft HTML súgó](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

