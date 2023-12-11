{
"dátum": "2023-03-28",
  "keywords": [
"pmp fájl",
"mi az a pmp fájl",
"hogyan kell pmp fájlt létrehozni",
"fájl",
"pmp fájl kiterjesztése",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "PMP fájlformátum - AutoCAD Plot Model Parameter File",
  "description":"További információ a PMP formátumról és az API-król, amelyek PMP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "PMP",
  "menu": {
    "docs": {
      "identifier": "settings-pmp",
      "parent": "settings"
}
},
"lastmod": "2023-03-28"
}

## Mi az a PMP fájl?

Az AutoCAD a ".pmp" fájlkiterjesztést használja a Plot Model Parameter File-hoz. Amikor egy rajzot nyomtat az AutoCAD programban, a Plot Model Parameter (PMP) fájl tartalmazza a nyomtatási folyamathoz használt nyomtatóspecifikus beállításokat és konfigurációt. Ez a fájl automatikusan létrejön, amikor személyre szabja a nyomtatási beállításokat az AutoCAD programban, és elnevezett nyomtatási stílusként menti azokat.

A PMP fájl a plotter konfigurációjának tárolására szolgál, mint például a papírméret, a nyomtatási lépték, a nyomtatási terület és a nyomtatási eltolás, valamint egyéb beállítások, például vonalvastagságok, vonaltípusok és toll-hozzárendelések. Ha ezeket a beállításokat PMP-fájlba menti, egyszerűen alkalmazhatja őket a jövőbeni nyomtatási munkákhoz anélkül, hogy minden alkalommal manuálisan kellene konfigurálnia a nyomtatóbeállításokat.

A PMP-fájl szerkesztésével módosíthatja a plotter beállításait, vagy új nyomtatási stílusokat hozhat létre különböző konfigurációkkal. A PMP-fájl megosztható más AutoCAD-felhasználókkal vagy számítógépekkel a következetes nyomtatási eredmények biztosítása érdekében.

## PMP fájlformátum – További információ

A PMP-fájl egy egyszerű szöveges fájl, amely bármely szövegszerkesztővel megnyitható és szerkeszthető, például a Jegyzettömb vagy a Wordpad segítségével. A nyomtatóspecifikus beállításokon kívül a PMP-fájl tartalmazhat nyomtatási stílusbeállításokat is, például színleképezéseket, szűrést és vonalvastagságot. Az AutoCAD támogatja a rendszernyomtatási stílusokat és az elnevezett nyomtatási stílusokat is. A rendszernyomtatási stílusok előre meghatározott nyomtatási konfigurációk, amelyek az AutoCAD-hez tartoznak, míg az elnevezett nyomtatási stílusok a felhasználó által definiált nyomtatási konfigurációk, amelyek egy PMP-fájlba kerülnek.

Az AutoCAD-ben testreszabhatja a nyomtatási beállításokat az Oldalbeállítás-kezelő megnyitásával, amely lehetővé teszi nyomtatási konfigurációk beállítását különböző típusú kimenetekhez, például nyomtatáshoz, PDF-fájlba történő nyomtatáshoz vagy DWF-fájlban való közzétételhez. Amikor egy rajzot nyomtat az AutoCAD programban, kiválaszthatja a használni kívánt nyomtatási stílust a rendelkezésre álló nyomtatási stílusok listájából. A nyomtatási stílus határozza meg, hogy a rajzban lévő objektumok hogyan legyenek ábrázolva tulajdonságaik, például szín, vonaltípus vagy vonalvastagság alapján.

## Hogyan készítsünk PMP fájlt?

Ha PMP fájlt szeretne létrehozni az AutoCAD programban, kövesse az alábbi lépéseket:

1. Nyissa meg a nyomtatni kívánt rajzfájlt, és lépjen az "Elrendezés" fülre.
2. Válassza az "Oldalbeállítás-kezelő" lehetőséget az "Oldalbeállítás" csoportban az "Elrendezés" lapon.
3. Az "Oldalbeállítás-kezelő" párbeszédpanelen válassza az "Új" lehetőséget egy új oldalbeállítás létrehozásához.
4. Az "Új oldalbeállítás" párbeszédpanelen adja meg az új oldalbeállítás beállításait, például a nyomtatót, a papírméretet, a nyomtatási léptéket és a nyomtatási területet. Kiválaszthatja az új oldalbeállításhoz használandó nyomtatási stílust is.
5. Kattintson az "OK" gombra az új oldalbeállítás mentéséhez és az "Új oldalbeállítás" párbeszédpanelből való kilépéshez.
6. Az "Oldalbeállítás-kezelő" párbeszédpanelen válassza ki az új oldalbeállítást, és kattintson a "Módosítás" gombra a nyomtatási beállítások vagy a nyomtatási stílus további módosításához.
7. Miután elvégezte az összes szükséges módosítást, kattintson a "Bezárás" gombra az "Oldalbeállítás-kezelő" párbeszédpanelből való kilépéshez.
8. A nyomtatási beállítások és a nyomtatási stílus PMP-fájlként való mentéséhez válassza a "Plot Style Manager" lehetőséget a "Kimenet" lap "Plot" csoportjából.
9. A "Plot Style Manager" párbeszédpanelen válassza ki a PMP-fájlként menteni kívánt nyomtatási stílust, majd kattintson az "Exportálás" gombra.
10. Az "Export Plot Style Table" párbeszédpanelen adja meg a PMP-fájl fájlnevét és helyét, majd kattintson a "Mentés" gombra.
11. A PMP fájl most mentésre került, és felhasználható a jövőbeni nyomtatási feladatokhoz.

## Hivatkozások
* [AutoCAD szoftver](https://en.wikipedia.org/wiki/AutoCAD)

