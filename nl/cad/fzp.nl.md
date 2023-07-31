{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over FZP-bestandsindelingen en API's die FZP-bestanden kunnen maken en openen.",
  "title" :"FZP File Format - Fritzing XML Part Description File",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Wat is een FZP-bestand?

Een FZP-bestand is een XML-bestand gemaakt door [Fritzing](https://fritzing.org/) prototype- en ontwerptoepassing voor elektronische circuits. Het bevat informatie over de eigenschappen, connectoren en bussen van het onderdeel in [XML](/nl/web/xml/) bestandsformaat. FPZ-bestanden kunnen niet zelfstandig worden gebruikt in Fritzing. In plaats daarvan worden ze geïmporteerd als onderdeel van het FZPZ-archiefbestand.

## FZP-bestandsindeling - Meer informatie

FZP-bestanden zijn XML-bestanden die informatie bevatten over de eigenschappen, connectoren en bussen van het onderdeel. Daarnaast bevatten FZP-bestanden ook informatie over de titel, beschrijving, auteur en publicatiedatum van het FZP-bestand. Wanneer een Fritzing-onderdeelbestand wordt geëxporteerd, maakt de Fritzing-app een [FZPZ](/nl/compression/fzpz/) gecomprimeerd archief aan dat een FZP-bestand en vier [SVG](/nl/page-description-language/svg/)-bestanden bevat.

De [FZP bestandsformaatspecificaties](https://github.com/fritzing/fzp/blob/master/docs/README.md) zijn beschikbaar op Github door Fritzing.

## Voorbeeld van FZP-bestandsstructuur

Een typisch FZP-bestand heeft de volgende XML-structuur.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Referenties

* [FZP-bestandsindelingspecificaties](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nieuwe onderdelen met fzpz-extensie](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

