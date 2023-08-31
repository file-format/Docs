{
  "date" : "2019-10-11",
  "keywords" :[ "rtf fájl", "rtf fájl formátum", "mi az rtf fájl", "fájl", "rtf példa", "rtf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Rich Text Format",
  "description":"További információ az RTF fájlformátumról és az RTF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az RTF fájl?

A Microsoft által bevezetett és dokumentált Rich Text Format (**RTF**) a formázott szöveg és grafika kódolási módszere alkalmazásokon belül. A formátum megkönnyíti a platformok közötti dokumentumcserét más Microsoft-termékekkel, így az interoperabilitást szolgálja. Ez a képesség szabványossá teszi a szövegszerkesztő szoftverek közötti adatátvitelt, és így a tartalom átvihető egyik operációs rendszerről a másikra anélkül, hogy elveszítené a dokumentum formázását. A fájlformátum-specifikációkat a Microsoft nyilvános [letöltésre](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) teszi elérhetővé, és a fejlesztő szemszögéből is hivatkozni lehet rájuk.

## Az RTF fájlformátum rövid története ##

Az RTF fájlformátum megjelenése óta több felülvizsgálaton ment keresztül. A hivatalos írási/olvasási verzióját a Microsoft Word 3.0 for Macintosh részeként tették közzé, az 1.0-s verzió specifikációival. A specifikációk végleges, 1.9.1-es verzióját a Microsoft 2008 márciusában tette közzé. Ezt követően a specifikáción nem történik további fejlesztés. Jelenleg szinte minden operációs rendszer rendelkezik több funkcióban gazdag alkalmazással, amelyek minimálisra csökkentették/felszámolták az RTF fájlformátum használatát.

## RTF fájlformátum specifikációi ##

Az RTF szabványként szolgál a szövegszerkesztő szoftverek és a tartalom egyik operációs rendszerről a másikra történő átvitelére. Ez a Microsoft Office Word által 2007-ig bevezetett vezérlőszavak használatával érhető el. A szabványos RTF-fájlok ASCII-ből állnak a formázott szöveg megjelenítésére, és nem ASCII-karaktereket tartalmaznak, amelyeket megfelelő kódértékekké alakítanak át. A Word újabb verziói képesek olvasni a korábbi verziókkal generált RTF-fájlokat, míg a régebbi verziók figyelmen kívül hagyják az általuk nem értett vezérlőszavakat és csoportokat.

### Az RTF alapjainak megértése ###

Az RTF fájlok 7 bites ASCII egyszerű szöveget használnak, amely a következőkből áll:

* ellenőrző szavak
* vezérlő szimbólumok és
* csoportok.

Ezek az RTF adatok érthető szövegként és karakterkódolásként való megjelenítésének építőkövei.

#### Vezérlőszó ####

Ezek speciálisan formázott parancsok, amelyek a karakterek megjelenítésre való megjelölésére szolgálnak, és nem lehetnek hosszabbak 32 betűnél. A vezérlőszót a következők határozzák meg:

\<ASCII Letter Sequence> //<//Delimiter//> //

Minden vezérlőszó megkülönbözteti a kis- és nagybetűket, és fordított perjellel kezdődik. Az ASCII betűsor tartalmazhat ASCII ábécét (a-tól z-ig és A-tól Z-ig). Az<Delimite> a vezérlőszó nevének végét jelöli, és a következők egyike lehet:

* Egy tér. Ez csak az ellenőrző szó elhatárolására szolgál, és figyelmen kívül hagyja a későbbi feldolgozás során.
* Numerikus számjegy vagy ASCII mínuszjel, amely azt jelzi, hogy egy numerikus paraméter van társítva a vezérlőszóhoz. A következő digitális sorozatot ezután az ASCII számjegyen kívül bármilyen karakter választja el (általában egy másik vezérlőszó, amely fordított perjellel kezdődik). A paraméter lehet pozitív vagy negatív decimális szám. A szám értékeinek tartománya névlegesen –32768 és 32767 között van, azaz egy előjeles 16 bites egész szám. Néhány vezérlőszó a ‌ –2 147 483 648 és 2 147 483 647 (32 bites előjelű egész) tartományba esik. Ezek a vezérlőszavak tartalmazzák a **\binN**, **\revdttmN//**, **\rsidN** kapcsolódó vezérlőszavakat és néhány képtulajdonságot, például a **\bliptagN**. Itt az **N** a numerikus paramétert jelöli. Az RTF-elemzőnek legfeljebb 10 számjegyet kell engedélyeznie, amelyet opcionálisan mínusz jel előz meg. Ha a határoló szóköz, akkor el kell dobni, vagyis nem kerül bele a későbbi feldolgozásba.
* Betűtől vagy számjegytől eltérő karakter. Ebben az esetben a határoló karakter befejezi a vezérlőszót, és nem része a vezérlőszónak. Például egy fordított perjel „\”, ami azt jelenti, hogy új vezérlőszó vagy vezérlőszimbólum következik.

#### Ellenőrző szimbólum ####

A vezérlőszimbólum egy különleges eseményt jelöl, amelynek sajátos jelentése van a tartalmától függően. Ez egy fordított perjelből áll, amelyet egy speciális karakter követ (nem alfabetikus karakter), és nem tartalmaz elválasztójeleket.

#### Csoport ####

Egy csoport állhat szövegből, vezérlőszavakból vagy kapcsos zárójelekbe zárt vezérlőszimbólumokból (**{ }**). A nyitó kapcsos zárójel (**{** ) a csoport kezdetét, a záró kapcsos zárójel (**}**) pedig a csoport végét jelzi. Minden csoport meghatározza a csoport által érintett szöveget és a szöveg különböző attribútumait.

### RTF fájlszerkezet ###

Az RTF fájl a következő szabványos szintaxissal rendelkezik:

A Microsoft által bevezetett és dokumentált Rich Text Format (**RTF**) a formázott szöveg és grafika kódolási módszere alkalmazásokon belül. A formátum megkönnyíti a platformok közötti dokumentumcserét más Microsoft-termékekkel, így az interoperabilitást szolgálja. Ez a képesség szabványossá teszi a szövegszerkesztő szoftverek közötti adatátvitelt, és így a tartalom átvihető egyik operációs rendszerről a másikra anélkül, hogy elveszítené a dokumentum formázását. A fájlformátum-specifikációkat a Microsoft nyilvános [letöltésre](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) teszi elérhetővé, és a fejlesztő szemszögéből is hivatkozni lehet rájuk.

#### RTF fejléc ####

Az RTF fejlécnek a következő ábrázolása van.

|Mező|Leírás
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

A fejléctáblázatoknak ebben a sorrendben kell megjelenniük, ha vannak. Az RTF fájl tartalmazhat csoportokat a betűtípusokhoz, stílusokhoz, képernyőszínekhez, képekhez, lábjegyzetekhez, megjegyzésekhez (annotációk), fejlécekhez és láblécekhez, összefoglaló információkhoz, mezőkhöz, könyvjelzőkhöz, dokumentum-, szakasz-, bekezdés- és karakterformázási tulajdonságokhoz, matematikához, képeket és tárgyakat. Ha a fájl tartalmazza a betűtípust, a fájlt, a stílust, a színt, a revíziójelet és az összefoglaló információs csoportokat és a dokumentum formázási tulajdonságait, akkor ezeknek az RTF törzsét megelőző RTF fejlécben kell megjelenniük. Ha valamelyik csoport tartalmát nem használjuk fel, a csoport elhagyható. Minden olyan csoportnak, amely egy másik csoportban meghatározott tulajdonságokat használja, a tulajdonságokat meghatározó csoport után kell megjelennie. Például a szín és a betűtípus tulajdonságainak meg kell előzniük a stíluscsoportot.

#### RTF verzió ####

Az RTF-dokumentumnak a következő hat karakterrel kell kezdődnie:

```
{\rtf1
```
ahol az 1 az RTF verziószámot mutatja.

#### Karakterkészlet ####

Az {\rtf1 után a dokumentumnak deklarálnia kell, hogy milyen karakterkészletet használ. A karakterkészlet deklarálása az alábbi parancsok egyikével történik:

`\ansi` – A dokumentum az ANSI karakterkészletben, más néven Code Page 1252-ben található, a szokásos MSWindows karakterkészletben.

`\mac` – A dokumentum a MacAscii karakterkészletben található, amely a Mac OS régi (10 előtti) verzióiban szokásos karakterkészlet.

`\pc` - A dokumentum a DOS Code Page 437-ben található, amely az MS-DOS alapértelmezett karakterkészlete. A jó izommemóriával rendelkező gépírók észreveszik, hogy ez az a karakterkészlet, amelyet még mindig használnak az „Alt numerikus” kódok értelmezésére – azaz ha lenyomva tartja az Alt billentyűt és beírja a „130”-at a numerikus billentyűzeten, az é betűt produkál, mert a karakter A 130 a CP437-ben egy é. Manapság ez az egyetlen használat, amelyet a CP437 lát.

`\pca` – A dokumentum a DOS Code Page 850-ben található, más néven MS-DOS többnyelvű kódoldal.

#### Betűtípus parancs ####

A karakterkészlet definícióját a `\deffN` parancs követi. Ez határozza meg, hogy az N betűtípus az alapértelmezett betűtípus ehhez a dokumentumhoz. Az N betűszámra a betűtípustáblázatból hivatkozunk. A `\deffN` parancs technikailag nem kötelező, de ott kell lennie, hogy biztonságos legyen, mint egy gyakori prolog, például a következő a 0 betűtípust választja alapértelmezett betűtípusnak.

`{\rtf1\ansi\deff0`

#### Betűtábla ####

A dokumentumban használható összes betűtípus megjelenik egy betűtípus-táblázatban, ahol minden betűtípust egy betűtípus-szám jelöl. A dokumentumnak rendelkeznie kell betűkészlet-táblázattal, bár egyes programok e nélkül is működnek.

A betűtípustáblázat szintaxisa: {\fonttbl //...declarations//...}, amelyben minden deklaráció a következő alapvető szintaxissal rendelkezik:

`{\fnumber\familycommand Fontname;}`

A négy deklarációt tartalmazó betűkészlet táblázat a következő:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Az ilyen betűtípus-táblázattal rendelkező dokumentumokban a `{\f2 cucc}` „cuccot” nyomtat a Courier New-ban. Egy betűtípus nem használható a dokumentumban, amíg nem szerepel a betűtípustáblázatban.

### Dokumentum vége ###

Minden RTF-dokumentumnak }-re kell végződnie, hogy bezárja a csoportot, amelyet a dokumentum első karaktereként megnyitott {. Semmi sem követheti az utolsó }-t, kivéve esetleg egy újsort.

## Hivatkozások ##

* [RTF 1.9.1 specifikációi](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)
* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)

