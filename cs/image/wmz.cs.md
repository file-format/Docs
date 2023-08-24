{
  "date" : "2019-10-11",
  "keywords" :[ "soubor wmz", "formát souboru wmz", "co je soubor wmz", "soubor", "příklad wmz", "přípona souboru wmz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru WMZ - komprimovaný metasoubor Windows",
  "description":"Další informace o formátu souboru WMZ a rozhraních API, která mohou vytvářet a otevírat soubory WMZ.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Co je soubor WMZ?

Soubor s příponou .wmz je komprimovanou verzí [WMF](/cs/image/wmf/) a používá se k ukládání metasouborů. Jedná se o soubor střední úrovně generovaný staršími verzemi aplikací Microsoft Office a není příliš populární. Soubory WMZ se generují při ukládání dokumentů do formátu [HTML](/cs/web/html/). Ty mohou být také generovány při odesílání dokumentů, které obsahují vložené kliparty, rovnice atd., e-mailem. Mezi aplikace, které mohou otevírat soubory WMZ, patří (ale nejen) Corel Winzip a Apple Archive Utility.

## Formát souboru WMZ

Soubory WMZ jsou komprimovány [Gzip](/cs/compression/gz/) a obsahují uvnitř [WMF](/cs/image/wmf/). Gzip používá pro kompresi archivu algoritmus DEFLATE. GZIP se liší od formátu archivu [ZIP](/cs/compression/zip/), protože aplikuje kompresní algoritmus na kompletní archiv, nikoli na jednotlivé soubory. Formát souboru se skládá z:

* Záhlaví souboru
* Volitelné záhlaví
* Komprimovaná data
* Zápatí souboru

Formát souboru GZIP [specifikace verze 4.3](https://datatracker.ietf.org/doc/html/rfc1952) publikovaný organizací Internet Engineering Task Force (IETF) obsahuje podrobné informace o formátu souboru.

## Reference

* [RFC1952: Specifikace formátu souboru GZIP](https://datatracker.ietf.org/doc/html/rfc1952), od [IETF](https://www.ietf.org)
* [Windows MetaFile – Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

