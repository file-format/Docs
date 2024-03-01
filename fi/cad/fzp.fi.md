{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi FZP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata FZP-tiedostoja.",
  "title": "FZP-tiedostomuoto - Fritzing XML -osan kuvaustiedosto",
  "linktitle": "FZP",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-fz-fip"
}
},
  "lastmod": "2022-06-20"
}

## Mikä on FZP-tiedosto?

FZP-tiedosto on XML-tiedosto, joka on luotu [Fritzing](https://fritzing.org/) elektronisten piirien prototyyppi- ja suunnittelusovelluksella. Se sisältää tietoja osan ominaisuuksista, liittimistä ja väylistä [XML](/web/xml/)-tiedostomuodossa. FPZ-tiedostoja ei voi käyttää itsenäisesti Fritzingissä. Sen sijaan ne tuodaan osana FZPZ-arkistotiedostoa.

## FZP-tiedostomuoto - lisätietoja

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## Esimerkki FZP-tiedostorakenteesta

Tyypillisellä FZP-tiedostolla on seuraava XML-rakenne.

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
## Viitteet

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Uudet osat fzpz-laajennuksella](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


