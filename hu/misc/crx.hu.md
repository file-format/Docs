{
"dátum": "2023-06-08",
  "keywords": [
"crx fájl",
"mi az a crx fájl",
"hogyan kell telepíteni a crx fájlt a google chrome-ba",
"hogyan kell megnyitni a crx fájlt",
"mit tartalmaz a crx fájl",
"mi a crx fájl formátuma",
"fájl",
"crx fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CRX fájlformátum - Google Chrome kiterjesztés",
  "description":"További információ a CRX formátumról és az API-król, amelyek CRX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"lastmod": "2023-06-08"
}

## Mi az a CRX fájl?

A CRX fájlformátum a Google Chrome böngészőbővítményeihez van társítva. A CRX-fájl lényegében egy tömörített csomag, amely szükséges fájlokat és metaadatokat tartalmaz egy bővítmény telepítéséhez és futtatásához a Google Chrome-ban. Extra funkcióval vagy témával javítja a webböngésző funkcionalitását vagy megjelenését.

Amikor egy CRX-fájlt letöltenek és telepítenek a Google Chrome-ba, a böngésző nyilvános kulcs és aláírás segítségével ellenőrzi a bővítmény integritását. Ha az ellenőrzés sikeres, a Chrome kibontja a CRX-fájl tartalmát, és telepíti a kiterjesztést, így elérhetővé teszi azt. A felhasználók a Chrome-bővítmények oldalon kezelhetik bővítményeiket, amely lehetővé teszi a telepített bővítmények engedélyezését, letiltását vagy eltávolítását.

## Hogyan telepítsem a CRX fájlt a Google Chrome-ba?

Ha CRX-fájlt szeretne telepíteni a Google Chrome-ba, kövesse az alábbi lépéseket:

1. Nyissa meg a Chrome böngészőt.
2. Írja be a „chrome://extensions” kifejezést a címsorba, és nyomja meg az Enter billentyűt.
3. Engedélyezze a „Fejlesztői mód” kapcsolót a Bővítmények oldal jobb felső sarkában.
4. Kattintson a "Kicsomagolt betöltés" gombra.
5. Keresse meg és válassza ki a CRX fájl kicsomagolt tartalmát tartalmazó mappát (vagy egyszerűen válassza ki magát a CRX fájlt).
6. Kattintson a „Megnyitás” gombra a bővítmény telepítéséhez.

## Mit tartalmaz a CRX fájl?

A CRX fájl tartalmazza a Google Chrome bővítményhez szükséges fájlokat és metaadatokat. Íme a CRX-fájlban található tipikus tartalmak lebontása:

- **Manifest fájl (manifest.json):** Ez a fájl egy JSON-formátumú fájl, amely információkat tartalmaz a kiterjesztésről, például a névről, a verzióról, a leírásról, az engedélyekről és a háttérszkriptekről. Meghatározza a kiterjesztés szerkezetét és viselkedését.
- **JavaScript fájlok:** Ezek a fájlok tartalmazzák a kiterjesztés funkcióját meghatározó kódot. Tartalmazhatnak szkripteket események kezelésére, weboldalak módosítására vagy a Chrome API-kkal való interakcióra.
- **HTML-, CSS- és képfájlok:** A bővítmények gyakran tartalmaznak felhasználói felület elemeket, például felugró ablakokat vagy beállítási oldalakat. A HTML fájlok határozzák meg ezen felületek szerkezetét, míg a CSS fájlok szabályozzák a megjelenésüket. A képfájlokat ikonokhoz vagy más grafikus elemekhez használják.
- **Opcionális forrásfájlok:** A bővítmények további forrásokat is tartalmazhatnak, például lokalizációs fájlokat több nyelv támogatásához. Ezek a fájlok a bővítmény felhasználói felületén használt szöveg fordítását tartalmazzák.
- **Háttérszkriptek:** Ha egy kiterjesztésnek vannak háttérfolyamatai vagy olyan szkriptek, amelyek az aktív weboldaltól függetlenül futnak, ezek a szkriptek bekerülnek a CRX-fájlba.
- **Tartalomszkriptek:** A tartalomszkriptek olyan szkriptek, amelyeket be lehet illeszteni a weboldalakba, hogy módosítsák azok viselkedését vagy interakcióba lépjenek a tartalommal. Ha a kiterjesztés tartalomszkripteket használ, a szkriptekhez szükséges fájlok jelen lesznek a CRX fájlban.
- **Egyéb eszközök:** A kiterjesztés speciális követelményeitől függően további fájlok, például audio- vagy videofájlok, betűtípusok vagy adatfájlok is szerepelhetnek benne.

A CRX fájlformátum lényegében egy tömörített csomag, amely ezeket a fájlokat és mappákat strukturált módon tartalmazza. Amikor a CRX fájlt telepíti a Google Chrome-ba, a böngésző kicsomagolja a tartalmat, és a megfelelő helyekre helyezi, lehetővé téve a bővítmény betöltését és futtatását a böngészőben.

## Mi a CRX fájl formátuma?

A CRX fájlformátum egy speciális formátum a Google Chrome-bővítmények csomagolására és terjesztésére. Ez lényegében egy tömörített ZIP-archívum, különböző fájlkiterjesztésekkel. A CRX fájl alapvető szerkezete a következő:

- **Fájl aláírása:** A fájl első 4 bájtja a "Cr24" mágikus számot tartalmazza (hexadecimális: 43 72 32 34), amely aláírásként szolgál a fájl CRX fájlként történő azonosításához.
- **Verziószám:** A következő 4 bájt a CRX formátum verziószámát jelenti.
- **Nyilvános kulcs hossza:** A következő 4 bájt a kiterjesztés aláírásának ellenőrzéséhez használt kódolt nyilvános kulcs hosszát jelzi.
- **Aláírás hossza:** A következő 4 bájt határozza meg a kiterjesztés aláírásának hosszát.
- **Nyilvános kulcs:** Ez a szakasz a kiterjesztés integritásának ellenőrzésére használt kódolt nyilvános kulcsot tartalmazza.
- **Aláírás:** Ez a szakasz a kiterjesztés aláírását tartalmazza, amely a bővítmény tartalmának a fent említett nyilvános kulcsnak megfelelő privát kulccsal történő aláírásával jön létre.
- **ZIP archívum:** A CRX fájl fennmaradó bájtjai egy tömörített ZIP archívumot tartalmaznak. Ez az archívum tartalmazza az összes szükséges kiterjesztésű fájlt és mappát, beleértve a jegyzékfájlt, JavaScript fájlokat, HTML fájlokat, CSS fájlokat, képeket és minden egyéb erőforrást.

## Hivatkozások
* [CRX formátum specifikáció](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

