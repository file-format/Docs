{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "soubor", "přípona", "formát", "formát souboru pro výměnu zvuku", "hudba", "formát souboru aiff", "aiff na mp3", "aiff vs wav", "převést aiff na mp3"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru AIFF a rozhraních API, která mohou vytvářet, převádět a otevírat soubory AIFF.",
  "title" :"AIFF - Audio Interchange File Format",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Co je soubor AIFF?
AIFF (Audio Interchange File Format) je nekomprimovaný formát audio souborů vyvinutý společností Apple v roce 1998, ale je založen na **EA IFF 85** (Standard for Interchange Format Files vyvinutý společností Electronic Arts), formátu obalu používaného na systémech Amiga. . Tento formát souboru přichází se standardem pro ukládání samplovaných zvuků. Formát je dostatečně flexibilní a umožňuje ukládání mono nebo vícekanálových vzorkovaných zvuků při různých vzorkovacích frekvencích a šířkách vzorků. Vzhledem k tomu, že soubory AIFF jsou nekomprimované, díky tomu jsou větší než jiné ztrátové formáty, jako je [MP3](/audio/mp3/).

Soubory AIFF se skládají ze 2 kanálů nekomprimovaného stereo zvuku s velikostí vzorku 16 bitů, zaznamenaných při 44,1 khz. Kvůli vysoké kvalitě zvuku může 5minutový zvuk zabrat až 50 MB místa na disku, což je podobné formátu souboru [WAV](/audio/wav/).

## AIFF vs WAV

AIFF a WAV jsou z hlediska kvality téměř stejné. Oba používají stejné kódování PCM (pulse-code modulation), což je činí většími ve srovnání s jinými ztrátovými formáty, jako je [MP3](/audio/mp3/), [M4A](/audio/m4a/). Některé z obecných rozdílů jsou uvedeny v tabulce níže:

|AIFF|WAV|
---|---|
|Používá se většinou pro MAC|Většinou se používá pro PC|
|Umožňuje metadeta| Nepovoluje metadeta|

## Struktura souboru AIFF

**EA IFF 85** stanoví celkovou strukturu pro ukládání dat v souborech. Soubor **EA IFF 85** se skládá z několika částí dat. Blok tvořící blok souboru AIFF se skládá z některých informací v záhlaví následovaných daty:
{{< figure src="../chunk.png" alt="AIFF Chunk" >}}

Soubor AIFF je kolekce několika různých typů bloků. Existují dva obecné typy částí, které jsou důležité pro vytvoření části souboru AIFF:
- **Common Chunk**: Obsahuje důležité parametry popisující vzorkovaný zvuk, jako je jeho délka a vzorkovací frekvence.
- **Sound Data Chunk**: Obsahuje skutečné zvukové vzorky.
Existuje mnoho dalších volitelných částí, které vypisují parametry nástroje, definují značky, ukládají informace specifické pro aplikaci atd.

### Místní typy bloků

Typy bloků pro vytvoření AIFF jsou uvedeny v tabulce níže:

|Typ kusu| Popis|
---|---|
|Common Chunk|Common Chunk popisuje základní parametry samplovaného zvuku|
|Sound Data Chunk|Sound Data Chunk obsahuje skutečné ukázkové snímky|
|Chunk značek|Chunk značek obsahuje značky, které ukazují na pozice ve zvukových datech|
|Chunk nástroje|Chunk nástroje definuje základní parametry, které může nástroj, jako je sampler, použít k přehrávání zvukových dat|
|MIDI Data Chunk|MiDI Data Chunk lze použít k ukládání MIDI dat|
|Audio Recording Chunk|Audio Recording Chunk obsahuje informace týkající se zařízení pro záznam zvuku|
|Application Specific Chunk|Application Specific Chunk mohou výrobci aplikací používat pro jakékoli účely|
|Chunk komentářů|Chunk komentářů se používá k ukládání komentářů ve FORM AIFF|
|Částky textu – jméno, autor, autorská práva, anotace| Všechny jsou kusy textu|

## Reference ##

* [Audio Interchange File Format – Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

