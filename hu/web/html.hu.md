{
  "date" : "2019-10-11",
  "keywords" :[ "html", "html fájl", "html fájlformátum", "html fájltípus", "fájl", "típus", "mi az a html fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTML fájl formátum",
  "description":"Tudjon meg többet a HTML-fájlformátumról és az API-król, amelyek HTML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a HTML fájl?

A HTML (Hyper Text Markup Language) a böngészőben való megjelenítésre létrehozott weboldalak kiterjesztése. A web nyelveként ismert HTML a weboldalak részeként megjelenítendő új információs követelményekkel fejlődött. A legújabb változat HTML 5 néven ismert, amely nagy rugalmasságot biztosít a nyelvvel való munkavégzéshez. A HTML oldalak vagy a szerverről érkeznek, ahol ezeket tárolják, vagy a helyi rendszerről is betölthetők. Minden HTML-oldal HTML-elemekből áll, például űrlapokból, szövegekből, képekből, animációkból, hivatkozásokból stb. Ezeket az elemeket címkék és számos más jelöli, ahol minden címkének van eleje és vége. Szkriptnyelveken, például JavaScripten és stíluslapokon (CSS) írt alkalmazásokat is beágyazhat az általános elrendezés megjelenítéséhez.

## Rövid története ##

Megalakulása és első szerepvállalása óta a HTML-specifikációkat 1996 óta a World Wide Web Consortium (W3C) tartja karban. 2000-ben nemzetközi szabvánnyá is vált (ISO/IEC 15445:2000). 1999-ben jelent meg a HTML 4.01. 2004-ben a Web Hypertext Application Technology Working Group (WHATWG) elkezdett dolgozni a HTML5 verzión, amely 2008-ban a W3C-vel közös leszállítás lett. 2014. október 28-án készült el és szabványosították.

## HTML fájlformátum szerkezete ##

Egy HTML 4 dokumentum három részből áll:

1. egy sor, amely HTML verzióinformációkat tartalmaz
1. egy deklaratív fejléc szakasz
1. törzs, amely a dokumentum tényleges tartalmát tartalmazza. A törzset megvalósíthatja a BODY elem vagy a FRAMESET elem, hogy a törzset keretekben tartalmazza

Az egyes szakaszokat szóközök, új sorok, tabulátorok és megjegyzések vezethetik vagy követhetik. Az alábbi példa egy egyszerű HTML-dokumentumra látható:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Verzió információ ###

A kód első sora, \<!DOCTYPE html> , az úgynevezett doctype deklaráció, és közli a böngészővel, hogy az oldal melyik HTML-verzióban van írva. A HTML verziójától függően számos különböző doctype deklaráció létezik, amelyek a dokumentumhoz használt dokumentumtípus-definíciót (DTD) nevezik el. Mindegyik DTD különbözik a többitől a támogatott elemekben, és a következőkben különbözik:

* HTML 4.01 Strict – minden olyan elemet és attribútumot tartalmaz, amely nem [elavult](https://www.w3.org/TR/html401/conform.html#deprecated) vagy nem jelenik meg a frameset dokumentumokban
* HTML 4.01 Transitional – mindent tartalmaz a szigorú DTD-ben, valamint elavult elemeket és attribútumokat (amelyek többsége a vizuális megjelenítésre vonatkozik
* HTML 4.01 Frameset – mindent tartalmaz az átmeneti DTD plus keretekben is

A **HTML5** esetében a verzióinformációk egyszerűen az alábbiak szerint vannak megadva.

```
<!DOCTYPE html>
```

### HTML fejléc információ ###

A HTML-dokumentum fejléce számos HTML-elemet tartalmazhat, amelyeket a böngésző nem jelenít meg. Az ilyen elemek vagy metaadatok, amelyek az oldalra vonatkozó információkat írnak le, vagy olyan szakaszokat tartalmaznak, amelyek külső forrásokból, például CSS-stíluslapokból vagy JavaScript-fájlokból való információk lekérésére szolgálnak. Az oldal fejlécét a head címke képviseli.

Az oldal címének beállításához a **cím** elem az egyetlen, amely szükséges az oldalon<head> címkéket. Ugyanezt használják a keresőmotorok az oldal címének azonosítására.

### HTML törzsinformáció ###

Ez a fájl fő része, amely tartalmazza a fájl böngészők által megjelenített összes tartalmát. A HTML törzse jelöléseket tartalmazhat, amelyek címkék formájában utalhatnak különféle építőelemekre. Számos különböző típusú információt tartalmazhat, például szöveget, képeket, színeket, grafikákat stb. Ezen kívül audio- és videoelemek is beágyazhatók a html törzsbe, hogy a böngészők megjelenítsék őket. A vizuális megjelenítést szolgáló modern stíluslap-alkalmazások miatt a BODY megjelenítési attribútumai, például a háttérszín, a hivatkozás színe, a szöveg színe stb. elavultak. Így a stíluslapok használatával ugyanazok a hatások érhetők el, mint az alábbiakban:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

A beágyazott stíluslapok könnyen beágyazhatók, és a vizuális effektusok gyors alkalmazásához a külső stíluslapok kényelmesebbé teszik az egyszeri telepítést és a sok helyen való hozzáférést.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML elemek ###

Amint azt korábban említettük, a HTML-törzs tartalmát címkék, más néven HTML-elemek képviselik. Minden címkéhez további információ is tartozhat attribútumok formájában, amelyek így vannak megírva<tag attribute1#"value1" attribute2#"value2"> , bár nem szükséges, hogy attribútumok legyenek minden címkénél. Ha az attribútumok nincsenek megemlítve, akkor minden esetben alapértelmezett értékek kerülnek felhasználásra. Íme néhány példa az elemekre:

#### Fejléc ####

```
<head>
  <title>The Title</title>
</head>
```

#### Címsorok ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Bekezdések ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Referenciák ##

* [A HTML-dokumentum globális szerkezete](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

