{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "soubor mp2", "přípona", "formát", "co je soubor mp2", "hudba", "formát souboru mp2"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů MP2 a rozhraních API, která mohou vytvářet, převádět a otevírat soubory MP2.",
  "title" :"MP2 - MPEG Layer 2 Audio File Format",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Co je soubor MP2?

Soubor MP2, který se také nazývá soubor MPA, je zvukový soubor komprimovaný pomocí vrstvy II MPEG-1 nebo MPEG-2; formát ztrátové komprese zvuku definovaný normou ISO/IEC 11172-3 spolu s MPEG-1 Audio Layer I a MPEG-1 Audio Layer III ([MP3](/cs/audio/mp3/)), aby se zmenšila velikost zvukového souboru. Vzhledem k tomu, že MP3 je populárnější než MP2, protože má menší velikost a dostupnost přes internet. Proto je MP2 stále zásadním standardem pro audio vysílání.

## Formát souboru MP2

MPEG Audio Layer II (MP2) je základním algoritmem standardů MP3. Kódování MPEG-1 Audio Layer 2 bylo získáno ze zvukového kodeku MUSICAM. Začalo to jako projekt Digital Audio Broadcast (DAB) v Německu jako součást výzkumného programu EUREKA. Eureka 147 obsahovala tři hlavní prvky: Transmission Coding & Multiplexing, COFDM Modulation a MUSICAM Audio Coding (Masking pattern Universal Sub-band Integrated Coding And Multiplexing). MUSICAM byl jedním z mála kódování, které dokázalo dosáhnout vysoké kvality zvuku při přenosových rychlostech v rozsahu 64 až 192 kbit/s na monofonní kanál. Cílem bylo zajistit nízké zpoždění, nízkou složitost, chybovou robustnost, krátké přístupové jednotky a splnit technické požadavky vysílání, telekomunikace a záznamu na digitální paměťová média.

MP2 je subpásmový audio kodér, který lze komprimovat v časové oblasti pomocí banky filtrů s nízkým zpožděním generující 32 komponent ve frekvenční oblasti. Pro srovnání, MP3 je transformační audio kodér s hybridní bankou filtrů, což znamená, že komprese aplikovaná ve frekvenční doméně po hybridní transformaci z časové domény. Kodér MP2 může využívat mezikanálové redundance pomocí volitelného kódování intenzity "společného sterea".

### Specifikace formátu souboru MP2

Formát souboru MP2 je založen na po sobě jdoucích digitálních snímcích o 1152 vzorkovacích intervalech se čtyřmi možnými formáty:

- mono formát
- stereo formát
- Intenzita kódovaný společný stereo formát (stereo irelevantnost)
- dvoukanálový (nekorelovaný) formát
Některé důležité technické specifikace MP2 jsou uvedeny v tabulce níže:

|Specifikace| Popis|
---|---|
|**Výběrové poměry**| 32, 44,1 a 48 kHz|
|**Přenosové rychlosti**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 a 384 kbit/s|
|**Další vzorkovací frekvence**|16, 22,05 a 24 kHz|
|**Další přenosové rychlosti**|8, 16, 24, 40 a 144 kbit/s|
|**Podpora více kanálů**|Až 5 zvukových kanálů s plným rozsahem a jeden kanál LFE (kanál s nízkou frekvencí)|

## Reference ##

* [MPEG-1 Audio Layer II – podle Wikipedie](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

