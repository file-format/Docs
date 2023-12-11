{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON Fájl - Fogalomalkalmazás-forrásfájl formátum",
  "description" :"További információ arról, hogy mi az a CON-fájl és az API-k, amelyek CON-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Mi az a CON fájl?

A CON fájl a **Concept Application Server** számára fejlesztett alkalmazás forráskód-fájlja. A szerver és a felhasználó közötti adatcserét szolgáló alkalmazások írására szolgál. A szerveren tárolt CON fájlok webböngészővel érhetők el, feltéve, hogy a Concept Client telepítve van a felhasználó oldalon. Koncepció Az alkalmazásszerver egy kis léptékű programozási nyelvű webszerver, amely [SQL](/hu/database/sql/) részhalmaz adatbázis-motorral (TinDB) is rendelkezhet.

A CON fájlok megnyithatók/futhatók a RadGs Concept Application Server segítségével.

## CON fájlformátum - További információ

A CON fájlok a szerveren vannak tárolva, és a felhasználói gép webböngészőjével érhetők el. Az [URL-ek](/hu/web/url/) fogalma eltér a normál HTTP URL-ektől, és a **concept://** előtaggal kezdődik.

### CON fájl URL Példa

A Concept Application Server kiszolgálón tárolt CON-fájl webböngészőn keresztül érhető el, például:

```
concept://domain.server.com/web_application/main.con.
```
## Hivatkozások

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

