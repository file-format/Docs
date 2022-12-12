{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "fájl", "kiterjesztés", "formátum", "E-könyv", "digitális könyv" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az EPUB-fájlformátumról és az EPUB-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"What is an EPUB file?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Mi az EPUB fájl?

Az .epub kiterjesztésű fájlok egy e-könyv fájlformátum, amely szabványos digitális kiadványformátumot biztosít a kiadók és a fogyasztók számára. A formátum mára annyira elterjedt, hogy számos e-olvasó és szoftveralkalmazás támogatja. Például Mac OS rendszeren az előre telepített **Books** szoftver támogatja az ilyen fájlok megnyitását. Ezen kívül számos kompatibilis szoftver áll rendelkezésre okostelefonokhoz, táblagépekhez és számítógépekhez. Az EPUB fájlszabványokat az [International Digital Publishing Forum ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF) karbantartja. Az EPUB 3 verziót a Book Industry Study Group (BISG) is támogatja, amely a szabványosított legjobb gyakorlatok, kutatások, információk és események, valamint a tartalomcsomagolás vezető könyvkereskedelmi szövetsége.

## Az EPUB fájlformátum rövid története

* **2007. október** – Az EPUB 2.0 jóváhagyva
* **2010. szeptember** - Karbantartási frissítés megjelent
* **2011. október** – Az EPUB 3.0 specifikációi hatályba léptek
* **2014. június** – Kisebb karbantartási frissítés jelent meg a 3.0-s verzió helyébe lépő
* **2017. január** – Az EPUB 3.1 hatályba lépett

## EPUB fájl formátum

Az EPUB fájlformátum egy olyan archívum, amely átnevezhető [ZIP](/hu/compression/zip/) kiterjesztésre, és a tartalma megtekinthető az archívum kibontásával bármely archívumkivonó segítségével. Ez egy nyílt XML-alapú formátum, amely HTML-fájlokból, képekből, CSS-stíluslapokból és egyéb elemekből áll. Számos szoftveralkalmazáson és API-n keresztül PDF, Mobi és számos más fájlformátumba konvertálható.

{{< figure src="../epub.png" alt="EPUB fájl formátum" >}}

**EPUB E-Book megnyitva a Mac OS Books alkalmazással**

Az EPUB fájlformátum a következő három nyílt szabványon alapul.

### Nyílt nyilvános struktúra (OPS) ###

Az EPUB 2.0 fájl XHTML 1.1-et használ a kiadvány tartalmának összeállításához. Ez lényegében azt jelenti, hogy egy EPUB-fájl egy vagy több weboldalból áll. Annak ellenére, hogy egy könyv vagy újság teljes tartalmát egyetlen oldalon is elhelyezheti, jobb, ha egy ilyen fájl nem haladja meg a 300 KB-ot, mind teljesítmény, mind kompatibilitási okokból. Csakúgy, mint a hagyományos weboldalak esetében, a stílust és az elrendezést lépcsőzetes stíluslapok (CSS) határozzák meg. Az EPUB-fájlokban a CSS2 egy részhalmazát (korlátozott számú parancssort) kell használni. A CSS3 számos új funkciója, például a lekerekített dobozok vagy a vetett árnyékok még nem érhető el. A visszamenőleges kompatibilitás érdekében az alkotó a DTBook-ot is használhatja az XHTML helyett a tartalom kódolásához.

### Nyitott csomagolási formátum (OPF) ###

A specifikáció ezen része olyan szerkezeti információkkal foglalkozik, mint például a metaadatok (ki a szerző és a kiadó, mi a cím,...), a manifest (az epub-fájlban található összes fájl listája) és a tartalomjegyzék. Ezek az adatok XML használatával vannak beágyazva.

### Tárolóformátum megnyitása (OCF) ###

Ahogy a fenti leírásoknak egyértelművé kellett tenniük, egy EPUB-dokumentum fájlsorozatból áll. Az OCF specifikációi meghatározzák, hogy ezek a fájlok hogyan kerüljenek egyetlen tárolófájlba. Ehhez ZIP tömörítést használnak.

## Támogatott képfájlformátumok ##

Az EPUB fájlformátum a következő képfájlformátumokat támogatja.

* [GIF](/hu/image/gif/)
* [JPG](/hu/image/jpeg/)
* [PNG](/hu/image/png/)
* [SVG](/hu/page-description-language/svg/)

## Referenciák ##

* [EPUB – a Wikipedia által](https://en.wikipedia.org/wiki/EPUB)

