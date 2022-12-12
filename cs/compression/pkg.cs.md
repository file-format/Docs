{
  "date" : "2021-04-08",
  "keywords" :[ "soubor pkg", "formát souboru pkg", "co je soubor pkg", "soubor", "příklad pkg", "přípona souboru pkg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Extensible Archive File Format",
  "description":"Další informace o formátu souboru PKG a rozhraních API, která mohou vytvářet a otevírat soubory PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Co je soubor PKG?

Soubor s příponou .pkg je soubor instalačního balíčku, který se používá k instalaci softwaru na macOS. Kromě počítačů Macintosh se používá také na iPhone. K instalaci obsahu souboru PKG lze použít vestavěnou instalační aplikaci Apple. Soubor PKG je podobný souboru MSI používanému v operačním systému Windows k instalaci softwaru. Během instalace mohou tyto soubory balíčků zaznamenávat zprávy, které vám dávají představu, jaké další věci jsou tímto balíčkem nainstalovány.

## Formát souboru PKG

PKR jsou binární soubory, které jsou komprimovány, aby se zmenšila celková velikost souboru. Od OSX 10.5 byly společností Apple představeny ploché balíčky s jedním instalačním souborem. Liší se od dřívějších formátů balení, které byly dodávány jako balíčky, nikoli jako jednotlivé soubory. Tyto přibalené balíčky obsahovaly strukturovanou hierarchii adresářů, která ukládala soubory způsobem, který usnadňuje jejich načítání prostřednictvím nějakého indexového souboru. Plochý formát souboru PKG je ve skutečnosti archiv [XAR](/cs/compression/xar/), který má:

* Záhlaví – Definuje velikost, kontrolní součet a informace o verzi
* Obsah – XML dokument, který je (a musí) být kódován jako UTF-8 a je uložen na začátku souboru, což usnadňuje skenování archivu a extrahování jednotlivých souborů
* Halda – nestrukturovaná halda dat, na kterou odkazuje TOC

## Reference

* [Formát souboru plochého balíčku](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG – Wikipedie](https://en.wikipedia.org/wiki/.pkg)

