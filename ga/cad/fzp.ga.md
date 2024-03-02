{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid FZP agus APIs ar féidir leo comhaid FZP a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid FZP - Comhad Cur Síos Cuid XML Fritzing",
  "linktitle": "FZP",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-fz-gap"
}
},
  "lastmod": "2022-06-20"
}

## Cad is comhad FZP ann?

Is comhad XML é comhad FZP cruthaithe ag [Fritzing](https://fritzing.org/) feidhmchlár um fhréamhshamhlú agus dearadh ciorcad leictreonach. Tá faisnéis ann maidir le hairíonna, nascóirí agus busanna na coda i bhformáid comhaid [XML](/web/xml/). Ní féidir comhaid FPZ a úsáid go neamhspleách i Fritzing. Ina áit sin, déantar iad a allmhairiú mar chuid de chomhad cartlainne FZPZ.

## Formáid Comhaid FZP - Tuilleadh Eolais

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## Sampla de Struchtúr Comhad FZP

Tá an struchtúr XML seo a leanas ag gnáthchomhad FZP.

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
## Tagairtí

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Páirteanna nua le síneadh fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


