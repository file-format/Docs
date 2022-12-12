{
  "date" : "2021-04-08",
  "keywords" :[ "soubor rpm", "formát souboru rpm", "co je soubor rpm", "soubor", "příklad rpm", "přípona souboru rpm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat Package Manager File",
  "description":"Další informace o formátu souboru RPM a rozhraních API, která mohou vytvářet a otevírat soubory RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Co je soubor RPM?

Soubor s příponou .rpm je balíček operačního systému Red Hat Linux pro instalace programů v systémech Linux. Red Hat Package Manager používá formát souboru RPM a je to bezplatný a open-source systém správy balíčků. I když lze soubory RPM použít k instalaci programů, lze je převést do jiných formátů balíčků, jako je [DEB](/cs/compression/deb/) pomocí programu Debian s názvem Alien.

## Formát souboru RPM

Soubor RPM je binární soubor, který může obsahovat sadu souborů. Ve většině případů jsou soubory RPM „binární RPM“, což jsou kompilované spustitelné soubory softwaru. Soubor RPM může obsahovat zdrojové RPM (SRPM), které lze použít k sestavení balíčku ze zdrojového kódu. Formát souboru RPM se skládá ze čtyř částí.

* Vedení – identifikuje soubor jako soubor RPM
* Podpis – lze jej použít k zajištění integrity a/nebo pravosti
* Záhlaví – Obsahuje metadata včetně názvu balíčku, verze, architektury, seznamu souborů atd.
* Archiv souborů – také známý jako užitečné zatížení, které je obvykle ve formátu cpio, komprimované pomocí [GZIP](/cs/compression/gz/)

## Reference

* [RPM – Wikipedia](https://rpm.org)
* [Dokumentace RPM](https://rpm.org/documentation.html)

