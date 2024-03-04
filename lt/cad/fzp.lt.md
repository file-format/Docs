{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie FZP failo formatą ir API, kurios gali kurti ir atidaryti FZP failus.",
  "title": "FZP failo formatas – Fritzing XML dalies aprašo failas",
  "linktitle": "FZP",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-fz-ltp"
}
},
  "lastmod": "2022-06-20"
}

## Kas yra FZP failas?

FZP failas yra XML failas, sukurtas naudojant [Fritzing](https://fritzing.org/) elektroninės grandinės prototipų ir projektavimo programą. Jame pateikiama informacija apie dalies savybes, jungtis ir magistrales [XML](/web/xml/) failo formatu. FPZ failai negali būti naudojami atskirai Fritzing. Vietoj to, jie importuojami kaip FZPZ archyvo failo dalis.

## FZP failo formatas – daugiau informacijos

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## FZP failo struktūros pavyzdys

Įprastas FZP failas turi tokią XML struktūrą.

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
## Nuorodos

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Naujos dalys su fzpz plėtiniu](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


