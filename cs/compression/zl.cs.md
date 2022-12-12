{
  "date" : "2019-12-09",
  "keywords" :[ "soubor zl", "formát souboru zl", "co je soubor zl", "soubor", "příklad zl", "přípona souboru zl", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP komprimovaný formát souboru",
  "description":"Další informace o formátu souboru ZL a rozhraních API, která mohou vytvářet a otevírat soubory ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Co je soubor ZL?

Soubor s příponou .zl je komprimovaný formát souboru ZLIP, který pro kompresi souborů používá variantu kompresního algoritmu DEFLATE. Je nezávislý na typu CPU, operačním systému, systému souborů a znakové sadě, a proto může být použit pro výměnu informací. Technické specifikace komprese ZLIP jsou k dispozici na [stránce IETF](https://tools.ietf.org/html/rfc1950) a lze na ně odkazovat z pohledu vývojáře.

## Formát souboru ZL

Stream zlib má následující strukturu:

* `CMF (Metoda komprese a příznaky)` - Tento bajt je rozdělen na 4bitovou metodu komprese a 4bitové informační pole v závislosti na metodě komprese.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Metoda komprese)` - Identifikuje metodu komprese použitou v souboru. Jeho hodnoty a odpovídající způsob komprese jsou následující.

| Hodnota CM| Komprese|
|---|---|
|CM = 8|DEFLATE s velikostí okna do 32 kB|
|CM = 15|Vyhrazeno|

* `CINFO (Informace o kompresi)` - Pro CM = 8 je CINFO 2-základní logaritmus velikosti okna LZ77 mínus osm (CINFO=7 označuje velikost okna 32 kB).

* „FLG (FLaGs)“ – Tento příznakový bajt je rozdělen takto:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Reference ##

* [Specifikace formátu souboru Zlib](https://tools.ietf.org/html/rfc1950)

