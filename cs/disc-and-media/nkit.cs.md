{
  "date" : "2022-04-01",
  "keywords" :[ "soubor nkit", "formát souboru nkit", "co je soubor nkit", "soubor", "příklad nkit", "přípona souboru nkit", "přípona", "formát", "zápatí nkit", "soubor formát nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů NKIT a rozhraních API, která mohou vytvářet a otevírat soubory NKIT.",
  "title" :"NKIT - Formát souboru obrazu disku",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Co je soubor NKIT?

Soubor NKIT je obraz disku s daty extrahovanými z her NintendoWii a GameCube. NKIT je pro formát Nintendo Toolkit. Výsledný kompresní soubor [ISO](/cs/compression/iso/) využívá hlavní data těchto her ke spuštění s emulátorovými programy, jako jsou Dolphin, Swiss a Nintendont. NKit je dodáván v raw (iso) a komprimovaných (gcz) formátech souborů, které byly navrženy tak, aby byly zachovány hratelnost a velikost.

## Formát souboru NKIT

Formát souboru NKit je neztrátový formát a používá se pro zmenšování a obnovu obrázků Nintendo Wii a GameCube. Formáty jsou dostupné ve formátech souborů ISO a GCZ pro každou z her GameCube a Wii.

|Systém |Formát |Podporovaný hardware |Podporovaný Dolphin |Obnovitelný 1:1 |Poznámky|
---|---|---|---|---|---|
|GameCube| nkit.iso| Ano | Ano | Ano |Stejné jako zkomprimovaný GameCube iso|
|GameCube| nkit.gcz| Ne| Ano| Ano |GCZ je vlastní kompresní formát Dolphin s vyhledáváním bloků|
|Wii| nkit.iso| Ne Ano | Ano| Formát RVT-H lze přehrát pouze v Dolphin|
|Wii| nkit.gcz| Ne Ano | Ano| RVT-H v GCZ hratelné pouze v Dolphin|

### Záhlaví NKIT

Záhlaví formátu souboru NKIT je následující.

|Offset |Délka |Název|
---|---|---|
|0x200 |0x4 |Záhlaví NKit 'NKIT'|
|0x204 |0x4 |Verze NKit ' v01'|
|0x208 |0x4 |Zdrojový obrázek originál CRC32|
|0x20C |0x4 |NKit CRC - rovná se NKit souboru CRC32 zdrojovému CRC na 0x208 (na 0x4 v GCZ)|
|0x210 |0x4 |Délka zdrojového obrázku|
|0x214 |0x4 |Vynucené ID nevyžádané pošty (Když se ID disku liší – vzácné – pouze GameCube)|
|0x218 |0x4 |Wii Aktualizovat oddíl CRC32, pokud byl odstraněn při převodu|

## Reference ##

* [Formát souboru NKIT – od gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

