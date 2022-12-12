{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az FZP fájlformátumról és az FZP-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"FZP fájlformátum - Fritzing XML részleíró fájl",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Mi az FZP fájl?

Az FZP-fájl egy XML-fájl, amelyet a [Fritzing](https://fritzing.org/) elektronikus áramkör prototípus- és tervezőalkalmazása hozott létre. Információkat tartalmaz az alkatrész tulajdonságairól, csatlakozóiról és buszairól [XML](/hu/web/xml/) fájlformátumban. Az FPZ fájlok nem használhatók önállóan a Fritzingben. Ehelyett az FZPZ archív fájl részeként importálódnak.

## FZP fájlformátum - További információ

Az FZP fájlok olyan XML fájlok, amelyek információkat tartalmaznak az alkatrész tulajdonságairól, csatlakozóiról és buszairól. Ezeken kívül az FZP fájlok az FZP fájl címére, leírására, szerzőjére és közzétételi dátumára vonatkozó információkat is tartalmaznak. Fritzing-alkatrészfájl exportálásakor a Fritzing alkalmazás létrehoz egy [FZPZ](/hu/compression/fzpz/) tömörített archívumot, amely egy FZP-fájlt és négy [SVG](/hu/image/svg/) fájlt tartalmaz.

Az [FZP fájlformátum specifikációi] (https://github.com/fritzing/fzp/blob/master/docs/README.md) elérhetők a Github by Fritzing webhelyen.

## Példa az FZP fájlszerkezetre

Egy tipikus FZP-fájl a következő XML-struktúrával rendelkezik.

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
## Hivatkozások

* [FZP fájlformátum specifikációi](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Új alkatrészek fzpz kiterjesztéssel](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

