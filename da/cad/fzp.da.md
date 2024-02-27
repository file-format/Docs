{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om FZP filformat og API'er, der kan oprette og åbne FZP filer.",
  "title": "FZP-filformat - Fritzing XML-delbeskrivelse Fil",
  "linktitle": "FZP",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-fz-dap"
}
},
  "lastmod": "2022-06-20"
}

## Hvad er en FZP fil?

En FZP-fil er en XML-fil, der er oprettet af [Fritzing](https://fritzing.org/) elektronisk kredsløbsprototype- og designapplikation. Den indeholder oplysninger om delens egenskaber, stik og busser i filformatet [XML](/web/xml/). FPZ-filer kan ikke bruges uafhængigt i Fritzing. I stedet importeres de som en del af FZPZ-arkivfilen.

## FZP-filformat - flere oplysninger

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## Eksempel på FZP-filstruktur

En typisk FZP-fil har følgende XML-struktur.

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
## Referencer

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nye dele med fzpz-udvidelse](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


