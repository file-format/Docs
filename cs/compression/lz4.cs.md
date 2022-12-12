{
  "date" : "2021-04-08",
  "keywords" :[ "soubor lz4", "formát souboru lz4", "co je soubor lz4", "soubor", "příklad lz4", "přípona souboru lz4", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 komprimovaný formát souboru",
  "description":"Další informace o formátu souborů LBR a rozhraních API, která mohou vytvářet a otevírat soubory LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Co je soubor LZ4?

Soubor s příponou .lz4 je komprimovaný archivní soubor vytvořený pomocí aplikací/utilit, které podporují kompresi [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). Algoritmus LZ4 se zaměřuje na kompromis mezi rychlostí a kompresním poměrem. Komprimované archivy LZ4 lze vytvořit pomocí nástroje příkazového řádku LZ4 a lze je pomocí téhož nástroje dekomprimovat.

## Formát souboru LZ4

Formát souboru LZ4, založený na kompresním algoritmu LZ4, je nezávislý na typu CPU, operačním systému, systému souborů a znakové sadě. Je vhodný pro kompresi souborů a kompresi streamování pomocí algoritmu LZ4. Počáteční implementaci formátu LZ4 provedl v jazyce [C](/cs/programming/c/) Yann Collet v roce 2011 a je k dispozici pro vývojáře na [Github](https://github.com/lz4/lz4) .

### Formát rámečku LZ4

Obecná struktura formátu souboru LZ4 je uvedena níže.

|MagicNb|F. Deskriptor| Blok|(...)|Koncová značka |C. Kontrolní součet|
---|---|---|---|---|---|
|4 bajty| 3-15 bajtů||| 4 bajty| 0-4 bajty|

#### Magické číslo

4 bajty, formát Little endian. Hodnota: 0x184D2204

#### Deskriptor rámce

Deskriptor rámce se skládá z 3 t0 15 bytů a je nejdůležitější částí specifikací. Pole Magic_Number a Frame_Descriptor jsou společně označovány jako záhlaví rámce LZ4 a jeho velikost se pohybuje mezi 7 a 19 bajty. Je to tak, jak je uvedeno níže.

|FLG| BD| (Velikost obsahu)| (ID slovníku)| HC|
---|---|---|---|---|
|1 bajt| 1 bajt| 0 - 8 bajtů| 0 - 4 bajty| 1 bajt|

#### Datové bloky

Každý datový blok se řídí následujícím pořadím.

|Velikost bloku| údaje| (Kontrolní součet bloku)|
---|---|---|
|4 bajty| |0 - 4 bajty|

#### Koncová značka

Tok bloků končí, když po posledním datovém bloku následuje 32bitová hodnota 0x00000000.

#### Kontrolní součet obsahu

Content_Checksum ověřuje správnost správného dekódování obsahu a provádí se pomocí výsledku algoritmu xxHash-32. Ověřuje výsledky úspěšného přenosu všech bloků ve správném pořadí a bez chyby.

## Reference

* [Formát rámce LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4 Compression Algorithm – Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

