{
"dátum": "2023-05-16",
  "keywords": [
"sámi fájl",
"mi az a szami fájl",
"példa szami fájlra",
"fájl",
"sami fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SAMI fájlformátum - feliratok és metaadatcsere fájl",
  "description":"További információ a SAMI formátumról és az API-król, amelyek SAMI fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"lastmod": "2023-05-16"
}

## Mi az a SAMI fájl?

A „.sami” kiterjesztésű fájlok általában egy SAMI (Subtitles And Metadata Interchange) fájlra utalnak. A SAMI egy feliratozási formátum, amelyet feliratok vagy feliratok megjelenítésére használnak a videókban. Eredetileg a Microsoft fejlesztette ki a Windows Media Player számára.

A SAMI fájlok időzítési információkat és szöveges tartalmat tartalmaznak a feliratokhoz, lehetővé téve azok szinkronizálását a videó lejátszásával. A formátum támogatja az alapvető formázási beállításokat, például a betűstílust, a színt és a feliratok elhelyezését a képernyőn.

A SAMI fájlok általában egyszerű szöveges fájlok, amelyeket szövegszerkesztővel lehet megnyitni és szerkeszteni. A SAMI-fájlok tartalma általában tartalmaz egy fejlécet, amely információkat tartalmaz a fájlról, majd az egyes feliratokat a megfelelő időzítéssel és szöveggel.

Íme egy példa arra, hogyan nézhet ki egy SAMI fájl:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

A SAMI fájlokat általában olyan videolejátszókkal vagy médialejátszókkal együtt használják, amelyek támogatják a feliratok megjelenítését, mint például a Windows Media Player vagy a VLC Media Player. A lejátszó beolvassa a SAMI fájlt, és szinkronizálja a feliratokat a videótartalommal, így a nézők a videó megtekintése közben elolvashatják a feliratokat.

## Támogatott HTML címkék

A SAMI (Subtitles And Metadata Interchange) fájlok korlátozott számú HTML-szerű címkét támogatnak a feliratok formázásához és stílusához. Íme néhány a SAMI által támogatott, gyakran használt címkék közül:

- ``<SAMI> :`` A gyökérelem, amely a teljes SAMI fájlt beágyazza.
- ``<HEAD> :`` A SAMI fájl fejlécinformációit tartalmazza.
<html>- ``<TITLE> :`` Megadja a SAMI fájl címét. </html>
- ``<BODY> :`` A felirat bejegyzéseket és azok időzítési információit tartalmazza.
- ``<SYNC> :`` Egy szinkronizálási pontot jelöl a felirathoz. Meghatározza az időzítést, amikor a feliratot meg kell jeleníteni.
- ``<P> :`` A felirat tényleges szöveges tartalmát tartalmazza. Általában a<SYNC> Blokk.
<html>- `` <FONT>:`` Meghatározza a zárt szöveg betűtípus-tulajdonságait. Az olyan attribútumok, mint a Color, Face, Size és Style használhatók a betűtípus megjelenésének módosítására.</font>
- ``<BR> :`` Sortörést szúr be a feliratba.
<html>- `` <B>:`` A mellékelt szöveget félkövéren jeleníti meg.</b>
<html>- `` <I>:`` A mellékelt szöveget dőlt betűvel jeleníti meg.</i>
<html>- `` <U>:`` A mellékelt szöveget aláhúzva jeleníti meg.</u>
- ``<C> :`` Meghatározza a felirat szövegének helyét vagy igazítását a képernyőn. Támogatja az olyan attribútumokat, mint a középső, középső, bal, jobb, felső, alsó és ezek kombinációi.
- ``<LANG> :`` Megadja a felirat szövegének nyelvi kódját. Segít a feliratok nyelvének azonosításában.

Ezek a SAMI-fájlok által támogatott alapvető címkék. Fontos megjegyezni, hogy a SAMI nem támogatja a HTML címkék és attribútumok teljes skáláját. A támogatott címkék elsősorban a feliratok stílusára és elhelyezésére összpontosítanak, nem pedig kiterjedt dokumentumstrukturálásra vagy interaktivitásra.

## Hivatkozások
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

