{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Soubor WOFF2 - Web Open Font Format 2.0 File",
  "description": "Zjistěte, co je soubor WOFF2 a rozhraní API, která mohou vytvořit a otevřít soubor WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-cs2"
}
},
  "lastmod": "2023-01-10"
}

## Co je soubor WOFF2?

WOFF2 je formát souboru písem, který je více komprimovanou verzí formátu WOFF (Web Open Font Format). Byl vyvinut jako způsob, jak snížit velikost souboru webových písem, což jim umožňuje rychlejší načítání a menší využití šířky pásma. WOFF2 používá ke kompresi dat písem kompresní algoritmus nazvaný Brotli, což může vést k velikosti souborů, které jsou výrazně menší než ekvivalentní [WOFF](/font/woff/) fonty. Tento formát je podporován většinou moderních webových prohlížečů včetně Chrome, Firefox, Safari, Opera a Edge (verze 14 a novější).

## Formát souboru WOFF2 – Další informace

Vnitřní struktura souboru souboru písem WOFF2 se skládá z několika různých částí, včetně záhlaví, metadat, adresáře tabulky a samotných dat písem.

 1. Záhlaví obsahuje informace o celkovém formátu souboru, včetně čísla verze a počtu tabulek, které se v souboru nacházejí.

 1. Sekce Metadata obsahuje informace, jako je název písma, autorská práva a další informace související s písmy.

 1. Adresář tabulky obsahuje informace o různých tabulkách, které tvoří písmo, včetně jejich umístění v souboru a jejich délky.

 1. Samotná data písma jsou rozdělena do několika různých tabulek, z nichž každá obsahuje specifické informace o písmu, jako jsou jeho znaky a jim odpovídající glyfy. Tyto tabulky mohou obsahovat:

 * Tabulka 'glyf' obsahuje skutečné obrysy písma, včetně tvaru a velikosti každého znaku.
 * Tabulka 'head' obsahuje obecné informace o písmu, jako je jeho číslo verze, velikost návrhu a tak dále.
 * Tabulka 'hmtx' obsahuje informace o metrikách písma, včetně šířek a pozic znaků.
 * Každá tabulka je po dokončení procesu kódování zkomprimována a uložena ve formátu souboru WOFF2.

Celková struktura je navržena tak, aby umožňovala rychlou analýzu a dekódování, takže webové prohlížeče mohou rychle a efektivně načíst a zobrazit písmo na webu.

### Záhlaví WOFF2
Záhlaví WOFF obsahuje identifikační podpis, který označuje druh dat obsažených v souboru. Záhlaví WOFF spolu s jeho poli je následující.

|Typ|Název pole|Popis|
---|---|---|
|UInt32|podpis |0x774F4632 'wOF2' |
|UInt32| aroma |Verze sfnt vstupního písma.|
|UInt32| délka |Celková velikost souboru WOFF.|
|UInt16| numTables |Počet položek v adresáři tabulek písem.|
|UInt16| vyhrazeno |Vyhrazeno; nastavit na nulu.|
|UInt32| totalSfntSize |Celková velikost potřebná pro nekomprimovaná data písem, včetně hlavičky sfnt, adresáře a tabulek písem (včetně odsazení).|
|UInt32| totalCompressedSize Celková délka komprimovaného datového bloku.|
|UInt16| majorVersion |Hlavní verze souboru WOFF.|
|UInt16| minorVersion |Menší verze souboru WOFF.|
|UInt32| metaOffset |Offset k bloku metadat, od začátku souboru WOFF.|
|UInt32| metaLength |Délka komprimovaného bloku metadat.|
|UInt32| metaOrigLength |Nekomprimovaná velikost bloku metadat.|
|UInt32| privOffset |Offset k bloku soukromých dat, od začátku souboru WOFF.|
|UInt32| privLength |Délka bloku soukromých dat.|


## Reference
 * [Formát souboru w3 WOFF2](https://www.w3.org/TR/WOFF2/)

