{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file FZP e le API che possono creare e aprire file FZP.",
  "title" :"Formato file FZP - Fritzing file di descrizione della parte XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Che cos'è un file FZP?

Un file FZP è un file XML creato da [Fritzing](https://fritzing.org/) applicazione di prototipazione e progettazione di circuiti elettronici. Contiene informazioni sulle proprietà, sui connettori e sui bus della parte nel formato file [XML](/it/web/xml/). I file FPZ non possono essere utilizzati indipendentemente in Fritzing. Vengono invece importati come parte del file di archivio FZPZ.

## Formato file FZP - Ulteriori informazioni

I file FZP sono file XML che contengono informazioni sulle proprietà, sui connettori e sui bus della parte. Oltre a questi, i file FZP contengono anche informazioni sul titolo, la descrizione, l'autore e la data di pubblicazione del file FZP. Quando un file di parte Fritzing viene esportato, l'app Fritzing crea un archivio compresso [FZPZ](/it/compression/fzpz/) che contiene un file FZP e quattro file [SVG](/it/image/svg/).

Le [Specifiche del formato file FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) sono disponibili su Github di Fritzing.

## Esempio di struttura di file FZP

Un tipico file FZP ha la seguente struttura XML.

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
## Riferimenti

* [Specifiche del formato file FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nuove parti con estensione fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

