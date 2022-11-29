{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om FZP-filformat och API:er som kan skapa och öppna FZP-filer.",
  "title" :"FZP File Format - Fritzing XML Part Description File",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Vad är en FZP fil?

En FZP-fil är en XML-fil skapad av [Fritzing](https://fritzing.org/) prototyp- och designapplikation för elektroniska kretsar. Den innehåller information om delens egenskaper, kontakter och bussar i filformat [XML](/sv/web/xml/). FPZ-filer kan inte användas oberoende i Fritzing. Istället importeras de som en del av FZPZ-arkivfilen.

## FZP-filformat - Mer information

FZP-filer är XML-filer som innehåller information om delens egenskaper, kopplingar och bussar. Utöver dessa innehåller FZP-filer även information om titel, beskrivning, författare och publiceringsdatum för FZP-filen. När en Fritzing-delfil exporteras skapar Fritzing-appen ett [FZPZ](/sv/compression/fzpz/) komprimerat arkiv som innehåller en FZP-fil och fyra [SVG](/sv/image/svg/)-filer.

[FZP filformatspecifikationer](https://github.com/fritzing/fzp/blob/master/docs/README.md) finns på Github av Fritzing.

## Exempel på FZP-filstruktur

En typisk FZP-fil har följande XML-struktur.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>,
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
## Referenser

* [FZP filformatspecifikationer](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nya delar med fzpz-tillägg](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

