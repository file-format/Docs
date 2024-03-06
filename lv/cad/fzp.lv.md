{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par FZP faila formātu un API, kas var izveidot un atvērt FZP failus.",
  "title": "FZP faila formāts — Fritzing XML daļas apraksta fails",
  "linktitle": "FZP",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-fz-lvp"
}
},
  "lastmod": "2022-06-20"
}

## Kas ir FZP fails?

FZP fails ir XML fails, kas izveidots ar [Fritzing](https://fritzing.org/) elektroniskās shēmas prototipēšanas un dizaina lietojumprogrammu. Tajā ir informācija par daļas īpašībām, savienotājiem un kopnēm [XML](/web/xml/) faila formātā. FPZ failus Fritzing nevar izmantot neatkarīgi. Tā vietā tie tiek importēti kā daļa no FZPZ arhīva faila.

## FZP faila formāts — vairāk informācijas

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## FZP faila struktūras piemērs

Tipiskam FZP failam ir šāda XML struktūra.

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
## Atsauces

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Jaunas daļas ar fzpz paplašinājumu](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


