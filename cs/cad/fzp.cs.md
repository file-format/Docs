{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů FZP a rozhraních API, která mohou vytvářet a otevírat soubory FZP.",
  "title" :"Formát souboru FZP - soubor popisu části Fritzing XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Co je soubor FZP?

Soubor FZP je soubor XML vytvořený aplikací [Fritzing](https://fritzing.org/) pro prototypování a návrh elektronických obvodů. Obsahuje informace o vlastnostech součásti, konektorech a sběrnicích ve formátu souboru [XML](/cs/web/xml/). Soubory FPZ nelze ve Fritzingu používat samostatně. Místo toho jsou importovány jako součást archivního souboru FZPZ.

## Formát souboru FZP – Další informace

Soubory FZP jsou soubory XML, které obsahují informace o vlastnostech součásti, konektorech a sběrnicích. Kromě nich obsahují soubory FZP také informace o názvu, popisu, autorovi a datu zveřejnění souboru FZP. Při exportu souboru součásti Fritzing vytvoří aplikace Fritzing komprimovaný archiv [FZPZ](/cs/compression/fzpz/), který obsahuje soubor FZP a čtyři soubory [SVG](/cs/page-description-language/svg/).

[Specifikace formátu souboru FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) jsou k dispozici na Github od Fritzing.

## Příklad struktury souboru FZP

Typický soubor FZP má následující strukturu XML.

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
## Reference

* [Specifikace formátu souboru FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nové díly s rozšířením fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

