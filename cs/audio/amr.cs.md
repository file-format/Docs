{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "soubor", "přípona", "formát", "co je soubor amr", "hudba", "formát souboru amr", "soubor amr", "převést soubor amr na mp3", "přehrát soubor amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů AMR a rozhraních API, která mohou vytvářet, převádět a otevírat soubory AMR.",
  "title" :"AMR - Adaptive Multi-Rate Codec File",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Co je soubor AMR?
Soubor s příponou .amr je formát zvukových dat relevantní pro zvukový kodek **Adaptive Multi-Rate**; sestává z vícerychlostního úzkopásmového kodeku řeči, který kóduje úzkopásmové signály s přenosovou rychlostí 4,75-12,2 kbit/s s hovorovou kvalitou od 7,4 kbit/s; používá přizpůsobení linky k výběru jedné z osmi různých bitových rychlostí.

## Formát souboru AMR
Formát souboru AMR využívá mnoho technik kódování, algoritmus ACELP (Algebraic Code Excited Linear Prediction) je jednou z nejlepších technik; navržený pro účinnější kompresi lidského mluveného zvuku. AMR byl nastaven jako standardní kodek hlasu nebo řeči organizací 3GPP v roce 1999. Formát souboru AMR se také používá k ukládání mluveného zvuku pomocí zvukového kodeku **Adaptive Multi-Rate**, který používá mnoho chytrých telefonů k ukládání nahraných záznamů. projevy.

### Struktura formátu souboru
AMR (Adaptive Multi-Rate) je zvukový formát; široce používané v různých mobilních aplikacích a zařízeních, typicky v audio přehrávači/rekordéru nebo v aplikacích typu VoIP. AMR lze dále klasifikovat jako:

1. AMR-NB (NarrowBand)
2. AMR-WB (WideBand)

Obvykle AMR označuje AMR-NB. Formát souboru AMR má následující strukturu:

Každý soubor AMR obsahuje 6bajtové záhlaví, které rozpoznává soubor jako zvuk AMR. Tato hlavička je vždy nastavena na:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

To je obvykle podobné u všech souborů AMR-NB. Pokud záhlaví odpovídá standardu, je pravděpodobné, že soubor je poškozen a neměl by být používán. soubor AMR se skládá z celého počtu zabalených snímků zvuku. Každý z těchto snímků tvoří 20 ms zvuku. Každý snímek lze zakódovat pomocí libovolného z platných režimů AMR-NB (0-7, 8 SID v režimu DTX). Vzhledem k tomu, že rámce mohou být kódovány různými bitovými rychlostmi, tato typická metoda se nazývá Adaptive Multi-Rate (AMR).
#### Režimy AMR
Níže jsou uvedeny různé režimy AMR a jejich odpovídající přenosové rychlosti:

|REŽIM| BITOVÉ SAZBY|
---|---|
|0| AMR 4,75 – Kóduje rychlostí 4,75 kbit/s|
|1 | AMR 5.15 - Kóduje rychlostí 5,15 kbit/s|
|2 | AMR 5.9 – Kóduje rychlostí 5,9 kbit/s|
|3 | AMR 6.7 – Kóduje rychlostí 6,7 kbit/s|
|4 | AMR 7.4 - Kóduje rychlostí 7,4 kbit/s|
|5 | AMR 7,95 – Kóduje rychlostí 7,95 kbit/s|
|6 | AMR 10.2 - Kóduje rychlostí 10,2 kbit/s|
|7 | AMR 12.2 - Kóduje rychlostí 12,2 kbit/s|

Velikost rámce režimů AMR v bajtech (včetně bajtu záhlaví) je uvedena níže:

|CMR |MODE |VELIKOST RÁMU (v bajtech)|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5,15 |14|
|2 |AMR 5,9 |16|
|3 |AMR 6,7 |18|
|4 |AMR 7,4 |20|
|5 |AMR 7,95 |21|

## Reference ##

* [Adaptive Multi-Rate audio kodek – Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [RTP Payload Format a File Storage Format pro audio kodeky AMR a AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

