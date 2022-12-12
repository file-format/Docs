{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "rozšíření", "soubor", "formát", "obrázek", "Obrázek ikony Apple", "macOS", "Apple", "Ikona" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Obrázek ikony Apple",
  "description":"Další informace o formátu souboru ICNS a rozhraních API, která mohou vytvářet a otevírat soubory ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor ICNS? ##

Formát ikon používaný programy macOS se nazývá soubor ICNS. Umožňuje 1bitová a 8bitová pásma alfa a ukládá jeden nebo více obrázků, obvykle vytvořených z dokumentů [PNG](/cs/image/png). Ikona programu v prohlížeči a rozhraní macOS se zobrazuje pomocí souborů ICNS.

V závislosti na umístění může mít ikona stejného stylu více nastavení. Formát ICNS prošel četnými změnami a vyvinul se do bodu, kdy jej lze nyní použít jako základ pro různé kompatibilní formáty. Zde je několik dalších důležitých bodů, které potřebujete vědět:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource a Mac OS icons Resource jsou některé z dalších jmen.
* Pro informace o ikoně se používá zdroj ve větvi zdroje.
* Ve většině případů soubor obsahuje mnoho obrázků. Podporované velikosti obrázků jsou 1612 čtverečních pixelů a 1024, 512, 256, 128, 48, 32 a 16 pixelů čtverečních.


## Formát souboru ICNS ##

Datový formát ICNS je kapsle pro jeden nebo více snímků, podporuje 1bitová pásma a četné stavy snímků.
Operační systém může změnit velikost obrázků ikon tak, aby odpovídaly požadované velikosti zobrazení. Větší obrázky ikon se obvykle ukládají jako soubory [JPEG](/cs/image/jpeg/) 2000 nebo [PNG](/cs/image/png). Je možný typ komprimovaných i nekomprimovaných souborů ICNS.

Data záhlaví a binární ikony tvoří strukturu souboru ICNS. Hlavička obsahuje 8 bajtů dat, z nichž čtyři jsou magický literál a čtyři z nich jsou délky souboru. Typ a velikost každého obrázku ikony jsou uloženy v sekci dat ikony, po které následují data binárního obrázku. Velikost obrázku určuje velikost binárního úseku.

## Technická specifikace ##

### Záhlaví ###

|Offset|Velikost|Cíl
---|---|---|
|0|4|Magický literál, musí být "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Délka souboru v bajtech, nejprve msb


### Údaje ikony ###

|Offset|Velikost|Cíl
---|---|---|
|0|4|Typ ikony
|4|4|Délka dat v bajtech (včetně typu a délky), nejprve msb
|8|Proměnná|Data ikon

### Komprese ###

Data pixelů jsou do určité míry komprimována. 32bitové ("is32", "il32", "ih32", "it32") a ARGB ("ic04", "ic05") pixely jsou často komprimovány (na kanál) podobným způsobem jako PackBits.

|Hodnota hlavního zákazníka|Koncové bajty|Výsledek (nekomprimovaný)
---|---|---|
|0 - 127|1 - 128|1 - 128 bajtů
|128 - 255|1 bajt|3 - 130 kopií

## reference ##

* [ICNS – Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

