{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku FZP i interfejsy API, które mogą tworzyć i otwierać pliki FZP.",
  "title" :"Format pliku FZP — plik opisu części Fritzing XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Czym jest plik FZP?

Plik FZP to plik XML utworzony przez [Fritzing](https://fritzing.org/) aplikację do prototypowania i projektowania obwodów elektronicznych. Zawiera informacje o właściwościach części, złączach i magistralach w formacie pliku [XML](/pl/web/xml/). Pliki FPZ nie mogą być używane niezależnie we Fritzing. Zamiast tego są importowane jako część pliku archiwum FZPZ.

## Format pliku FZP — więcej informacji

Pliki FZP to pliki XML, które zawierają informacje o właściwościach części, złączach i magistralach. Oprócz tego pliki FZP zawierają również informacje o tytule, opisie, autorze i dacie publikacji pliku FZP. Podczas eksportowania pliku części Fritzing aplikacja Fritzing tworzy skompresowane archiwum [FZPZ](/pl/compression/fzpz/), które zawiera plik FZP i cztery pliki [SVG](/pl/page-description-language/svg/).

[Specyfikacje formatu plików FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) są dostępne na Github przez Fritzing.

## Przykład struktury pliku FZP

Typowy plik FZP ma następującą strukturę XML.

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
## Bibliografia

* [Specyfikacje formatu plików FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nowe części z rozszerzeniem fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

