{
  "date" : "2021-01-21",
  "keywords" :[ "soubor ai", "formát souboru ai", "co je soubor ai", "soubor", "příklad ai", "přípona souboru ai", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Adobe Illustrator Artwork File",
  "description":"Další informace o formátu souborů AI a rozhraních API, která mohou vytvářet a otevírat soubory AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Co je soubor AI?

Soubor s příponou .ai je soubor uměleckého díla Adobe Illustrator, který obsahuje vektorovou grafiku na jedné stránce. používá body k vytvoření cest pro zobrazení obrazových dat, čímž je chráněno před ztrátou kvality obrazu, pokud je zvětšen. Formát souboru AI je základem formátu souboru PGF, který je podobný souborům AI. Formát AI nachází své hlavní použití pro loga a tištěná média a jeho počáteční verze byly považovány za podobné jako u souborů [EPS](/cs/page-description-language/eps/). Soubory AI lze otevřít pomocí nástrojů Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro a CorelDraw Graphics.

## Formát souboru AI

AI je proprietární formát souboru aplikace Adobe Illustrator a pro ukládání souborů kompatibilních s EPS používá přístup duální cesty podobný PGF. [Specifikace formátu souboru Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) poskytují podrobné odkaz vývojáře pro interní podrobnosti o tomto formátu souboru. Vše Dokumenty (soubory) vytvořené aplikací Adobe Illustrator jsou dokumenty v jazyce PostScript a mají dvě hlavní části, které odpovídají konvencím strukturování dokumentu: „prolog“ a „skript“.

### Prolog

Sekce prolog obsahuje informace potřebné pro interpretaci souboru. Příkladem může být ohraničovací rámeček, který obsahuje všechny značky na stránce. Obsahuje také informace o zdrojích, jako jsou fonty a definice procedur. Tyto prostředky jsou logicky seskupeny do sad nazývaných procsets a obsahují explicitní metody pro inicializaci a ukončení jejich procedur.

### Skript

Grafické prvky na stránce popisuje skript. Skript obsahuje odkazy na operátory a procedury v prologu spolu s operandy a daty. Tři logické části skriptu zahrnují:

* Setup Sequence - která inicializuje a aktivuje zdroje definované v prologu
* Posloupnost popisných operátorů
* Trailer, který deaktivuje zdroje

Operátory ve skriptu jsou sekvence grafických prvků napsané v jazyce definovaném procsety v prologu. Tyto sekvence se skládají z kolekcí datových prvků, definic grafických atributů a volání procedur definovaných v procsetech.

### Značky objektů

Tagy objektu se používají k připojení vlastních informací k uměleckému objektu Adobe Illustrator. Tagy se skládají z:

* Identifikátor značky
* Typ značky
* Údaje

## Reference
* [Specifikace formátu souboru Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Formát souboru AI od PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

