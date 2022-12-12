{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier FZP și despre API-urile care pot crea și deschide fișiere FZP.",
  "title" :"Format de fișier FZP - Fișier de descriere a părții XML Fritzing",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Ce este un fișier FZP?

Un fișier FZP este un fișier XML creat de [Fritzing](https://fritzing.org/) aplicația de prototipare și proiectare a circuitelor electronice. Conține informații despre proprietățile piesei, conectorii și magistralele în format de fișier [XML](/ro/web/xml/). Fișierele FPZ nu pot fi utilizate independent în Fritzing. În schimb, acestea sunt importate ca parte a fișierului de arhivă FZPZ.

## Format de fișier FZP - Mai multe informații

Fișierele FZP sunt fișiere XML care conțin informații despre proprietățile piesei, conectorii și magistralele. Pe lângă acestea, fișierele FZP conțin și informații despre titlul, descrierea, autorul și data publicării fișierului FZP. Când un fișier de parte Fritzing este exportat, aplicația Fritzing creează o arhivă comprimată [FZPZ](/ro/compression/fzpz/) care conține un fișier FZP și patru fișiere [SVG](/ro/image/svg/).

[Specificațiile formatului fișierului FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) sunt disponibile pe Github by Fritzing.

## Exemplu de structură a fișierului FZP

Un fișier FZP tipic are următoarea structură XML.

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
## Referințe

* [Specificații de format de fișier FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Piese noi cu extensia fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

