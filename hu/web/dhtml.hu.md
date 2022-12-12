{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml", "dhtml fájl", "dhtml fájlformátum", "dhtml fájltípus", "fájl", "típus", "mi az a dhtml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML – dinamikus HTML fájlformátum",
  "description":"További információ a DHTML fájlformátumról és az API-król, amelyek DHTML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DHTML fájl?

A .dhtml kiterjesztésű fájl egy dinamikus [HTML](/hu/web/html/) fájl, amely egy weboldal dinamikus tartalmának létrehozására szolgál. A DHTML-ben létrehozott webelem eseményvezérelt, és nem szükséges az oldal újratöltése. A legtöbb esetben DHTML-fájlt használnak a weboldal dinamikus tartalmának létrehozására, például legördülő menük, lebegő rétegek, görgetőgombok és egyéb dinamikus tartalom létrehozására. Szinte naponta találkozik dinamikus html elemekkel az életében, amikor egy menüpontra viszi az egeret, és ez további almenüpontokat nyit meg. A DHTML olyan webes technológiákat használ, mint a [HTML](/hu/web/html/), a [Javascript](/hu/web/js/), a HTML DOM, a HTML Events és a [CSS](/hu/web/css/) a dinamika eléréséhez. az elemek viselkedése.

## DHTML fájlformátum

A DHTML fájlok egyszerű szöveges fájlok, amelyek DHTML kódot tartalmaznak a webes elemek dinamikus viselkedésének megvalósításához.


### DHTML DOM

A DHTML Document Object Model (DOM) a HTML DOM-on alapul, amely egy fastruktúra elemekkel, attribútumokkal és szöveggel, ahogy az a következő képen látható.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

A "Dokumentum" csomópont számos függvény meghívására használható különböző funkciók megvalósításához. A következő példa egyszerűen a JavaScript document.write() metódusát használja a DHTML-ben.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Ez a kód a „Hello World” szöveget írja ki a böngészőbe.

### DHTML események

|S.No.|Esemény|Előfordulás|
---|---|---|
|1|onbort|Amikor a felhasználó megszakítja az oldal vagy a médiafájl betöltését.|
|2|onblur|Ez akkor fordul elő, amikor a felhasználó elhagy egy HTML-objektumot.|
|3|onchange|Akkor fordul elő, amikor a felhasználó módosítja vagy frissíti egy objektum értékét.|
|4|onclick|Akkor fordul elő vagy aktiválódik, amikor bármely felhasználó rákattint egy HTML-elemre.|
|5|ondblclick|Ez akkor fordul elő, amikor a felhasználó kétszer egy HTML-elemre kattint.|
|6|onfocus|Ez akkor fordul elő, amikor a felhasználó egy HTML-elemre fókuszál. Ez az eseménykezelő az onblurrel szemben működik.|
|7|onkeydown|Akkor aktiválódik, amikor a felhasználó megnyom egy billentyűt a billentyűzeten. Ez az eseménykezelő az összes kulcshoz működik.|
|8|onkeypress|Akkor aktiválódik, amikor a felhasználók megnyomnak egy billentyűt a billentyűzeten. Ez az eseménykezelő nem aktiválódik minden kulcsnál.|
|9|onkeyup|Ez akkor fordul elő, amikor a felhasználó kiengedett egy billentyűt a billentyűzetről, miután megnyomott egy tárgyat vagy elemet.|
|10|onload|Ez akkor fordul elő, amikor egy objektum teljesen be van töltve.|
|11|onmousedown|Ez akkor fordul elő, amikor a felhasználó egy HTML elem fölé nyomja az egeret.|
|12|onmousemove|Ez akkor fordul elő, amikor a felhasználó egy HTML-objektumra mozgatja a kurzort.|
|13|onmouseover|Ez akkor fordul elő, amikor a felhasználó egy HTML-objektum fölé viszi a kurzort.|
|14|onmouseout|Akkor fordul elő vagy aktiválódik, amikor az egérmutatót kimozdítják egy HTML elemből.|
|15|onmouseup|Ez akkor fordul elő, vagy aktiválódik, amikor az egérgombot felengedik egy HTML elem felett.|
|16|onreset|A felhasználó az űrlap visszaállítására használja.|
|17|onselect|A weboldal tartalom vagy szöveg kiválasztása után következik be.|
|18|onsubmit|A rendszer akkor aktiválódik, amikor a felhasználó az űrlap elküldése után egy gombra kattint.|
|19|onunload|A rendszer akkor aktiválódik, amikor a felhasználó bezár egy weboldalt.|

## Hivatkozások

* [Dinamikus HTML – Wikipédia](https://en.wikipedia.org/wiki/Dynamic_HTML)

