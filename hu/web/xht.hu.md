{
  "date" : "2021-05-24",
  "keywords" :["xht", "File", "Extension", "File Format", "File Extension", "extended hypertext markup language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHT",
  "description":"További információ az XHT-fájlformátumról és az XHT-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Mi az XHT fájl?

Az .xht kiterjesztésű fájl az [XHTML](/hu/web/xhtml/) (Extended Hypertext Markup Language) fájltípushoz társított webfájl, amely maga egy [XML](/hu/web/xml/) alapú jelölőfájl. Mindkét fájl hasonló a HTML-hez, de szigorúbb XML-szerű szintaxisuk van. Az XHT-fájlok strukturáltabbak, kevesebb szkriptet igényelnek, és általánosak az XML meglévő lehetőségeinek felhasználása mellett.

## XHT fájlformátum

Az XHT-fájl alapértelmezés szerint egyszerű szöveges fájlként jön létre és tárolódik UTF-8 kódolással. Egy XHTML-dokumentum teljes forráskódját tartalmazza, amely bármely Unicode kódolást támogató szövegszerkesztővel megnyitható és szerkeszthető. Az XHT fájlformátum a szövegszerkesztők mellett a legtöbb modern webböngésző számára érthető, és ezekkel is megnyitható.

## XHT példa

Az XHT-dokumentum következő példája határozza meg az XML-deklarációkat.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## Referenciák ##

* [Az XHTML története: az 1990-es évektől napjainkig](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

