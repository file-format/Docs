{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST File Format-reStructuredText File",
  "description":"További információ az RST-fájlformátumról és az RST-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## Mi az RST fájl?

Az RST-fájl egy műszaki dokumentációs fájlformátum, amelyet elsősorban a Python programozói közösség használ. Ez egy reStructuredText jelölőnyelven írt szövegfájl, amely stílusokat és formázást alkalmaz a sima szöveges dokumentumokhoz a dokumentáció generálásához. Az RST-fájlok a Python programkódban található megjegyzéseket és egyéb információkat használják fel az alkalmazás műszaki dokumentációjának létrehozásához. Ezek azonban olyan szöveget is tartalmazhatnak, amely egyszerű weboldalakká és [e-könyvekké](/hu/ebook/) konvertálható. Az olyan szövegszerkesztők, mint a Github Atom, a GNU Emacs (cross-platform), a Microsoft Notepad (Windows), az Apple TextEdit (Mac) és a Vim (Linux) használhatók az RST fájlok megnyitásához.

## RST fájlformátum

Az RST-fájlok reStructuredText jelölőnyelven írt kódot tartalmaznak. A Python Doc-SIG (Documentation Special Interest Group) Docutils projektjének része, amely a Javadoc for Java-hoz hasonló eszközkészletet biztosít Python számára. Az RST-fájlformátum elemzője be van ágyazva a Docutils-ba, és információkat tud kinyerni a Python-programokból a programdokumentációba való formázáshoz.

### reStructuredText RST Példa

Vegyünk egy RST fájlformátumban írt példaszöveget az alábbiak szerint.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Ha ezt a szöveget egy rST processzorba, például a Docutilsba viszi be, a kimenet a következő.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Hivatkozási szám

* [reStructuredText – Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

