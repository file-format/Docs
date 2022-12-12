{
  "date" : "2019-10-11",
   "keywords" :[ "apkg", "apkg fájl", "apkg fájlformátum", "apkg fájltípus", "fájl", "típus", "Mi az APKG fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard Deck File Format",
  "description" :"További információ arról, hogy mi az APKG fájl és az API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Mi az APKG fájl?

Az .apkg kiterjesztésű fájl kártyacsomag, amelyet az [Anki](https://ankiweb.net/about) szoftveralkalmazásban való használatra hoztak létre, amely egy tanulókártya-alapú tanulási program. Tartalmaz [HTML](/hu/web/html/) szöveget, amelyet betölthet és megjeleníthet az Anki alkalmazásban, valamint képekkel és hangokkal is rendelkezhet vizuális és hallható tanuláshoz. Az Anki lehetővé teszi a felhasználók számára, hogy létrehozzák saját Anki-tanulókártya-paklijukat, valamint importálják más felhasználók tanulókártya-csomagjaikat.

## APKG fájlformátum

Az Anki kártyacsomagok olyan sablonokból készülnek, amelyeket HTML-ben írnak, amely egy híres és gyakori nyelv a weboldalak létrehozásához. A pakli kártyák stílusa a CSS segítségével történik, amely a weboldalak stílusának kialakítására használt nyelv. A stílus a következő módosításokat tartalmazza:

* font-family – A kártyán használandó betűtípus neve.
* font-size – A betűméret pixelben.
* text-align – Meghatározza, hogy a szöveget középre, balra vagy jobbra kell-e igazítani.
* szín - Meghatározza a szöveg színét, amely lehet egyszerű színnevek, például "kék", "piros" stb. vagy HTML színkódok.
* background-color – Meghatározza a kártya háttérszínét

A stílusinformáció megosztásra kerül az összes kártya között, ami minden kártyára hatással lesz, amikor változás történik. A következő példa az első kivételével minden kártyán sárga hátteret használ:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Az Anki kártyán lévő képek átméretezése a következőképpen vezérelhető.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascript beágyazása Anki kártyákba

A kártyasablonok segítségével a [Javascript](/hu/web/js/) Anki kártyába ágyazható. A Javascript haladó szintje miatt azonban nem biztosított a támogatása. Ezen túlmenően a renderelő eszközök eltérően mutathatják meg a Javascript kártyán lévő megvalósítási hatásait, ami azt eredményezi, hogy a megvalósítást minden eszközön tesztelni kell. Bizonyos Javascript-funkciók, például a window.alert, megnehezítik az Ön által írt Javascript-kód hibakeresését.

## Hivatkozások ##

* [Anki-dokumentáció](https://docs.ankiweb.net/intro.html)

