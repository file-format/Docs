{
  "date" : "2019-10-11",
  "keywords" :[ "soubor emz", "formát souboru emz", "co je soubor emz", "soubor", "příklad emz", "přípona souboru emz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ File Format - Windows Compressed Enhanced Meta file",
  "description":"Další informace o formátu souboru EMZ a rozhraních API, která mohou vytvářet a otevírat soubory EMZ.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Co je soubor EMZ?

Soubor s příponou .emz je komprimovaný kontejner Enhanced Metafile (soubor [EMF](/cs/image/emf/)). Tyto jsou komprimovány pomocí kompresní techniky [GZIP](/cs/compression/gz/), což je běžně používaná metoda komprese v operačních systémech UNIX a LINUX. Odpojení ZIP (/cs/compression/zip/), GZIP komprimuje archiv jako celek namísto komprimace jednotlivých souborů. Soubory EMZ jsou menší ve srovnání se soubory EMF a pomáhají při rychlém přenosu během online sdílení souborů. Některé z aplikací, které mohou otevřít soubory EMZ, zahrnují Microsoft Visio 2019, Microsoft Office 2019, XnView MP a File Viewer Plus.

## Formát souboru EMZ

Soubory EMZ jsou komprimovány [Gzip](/cs/compression/gz/) a obsahují uvnitř [EMF](/cs/image/emf/). Gzip používá pro kompresi archivu algoritmus DEFLATE a liší se v použití komprese. Soubor EMZ lze dekomprimovat pomocí komprimačních nástrojů GZip, jako je GNU Zip. Formát souboru se skládá z:

* Záhlaví souboru
* Volitelné záhlaví
* Komprimovaná data
* Zápatí souboru

Formát souboru GZIP [specifikace verze 4.3](http://tools.ietf.org/html/rfc1952) publikovaný organizací Internet Engineering Task Force (IETF) obsahuje podrobné informace o formátu souboru.

## Reference

* [RFC1952: Specifikace formátu souboru GZIP](http://tools.ietf.org/html/rfc1952), od [IETF](https://www.ietf.org/)
* [Windows MetaFile – Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

