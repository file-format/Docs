---
date: 2019-12-13
keywords: flac, formát souboru flac, přípona .flac, soubor flac, flac vs mp3
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souboru FLAC a rozhraních API, která mohou vytvářet a otevírat soubory FLAC."
title: Formát souboru FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Co je soubor FLAC?

FLAC (Free Lossless Audio Codec) je bezztrátový kompresní formát kódování zvuku vyvinutý nadací Xiph.Org Foundation. FLAC je bezplatný otevřený formát, který je uložen s příponou .flac. Digitální zvuk komprimovaný pomocí algoritmu FLAC je obvykle zmenšen na 50 až 70 procent. Soubory FLAC lze dekomprimovat na identickou kopii původních zvukových souborů.

## Formát souboru FLAC

Toto je přehled bitového toku FLAC.

- **značka fLaC**: Tato značka se přidá na začátek streamu. Za ním následuje jeden nebo více bloků metadat.
- **Bloky metadat**: FLAC podporuje 128 druhů bloků metadat; v současné době jsou definovány následující.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: Zvuková data se skládají z jednoho nebo více zvukových snímků.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Stručná historie formátu souboru FLAC

Josh Coalson zahájil vývoj FLAC v roce 2000. První verze FLAC byla vydána 20. července 2001. FLAC byl začleněn pod vlajkou Xiph.Org dne 20. ledna 2003. Vývoj FLAC byl přesunut do úložiště git Xiph.Org s vydání verze 1.3.0 dne 26. března 2013.

## Složení projektu FLAC

Projekt FLAC se skládá z následujících částí:

- Streamové formáty.
- Jednoduchý formát kontejneru pro stream (FLAC).
- libFLAC: Knihovna referenčních kodérů, dekodérů a rozhraní metadat.
- libFLAC++: objektově orientovaný obal pro libFLAC.
- flac: Program příkazového řádku pro kódování a dekódování toků FLAC.
- metaflac: Editor metadat příkazového řádku pro FLAC.
- Vstupní pluginy pro hudební přehrávače jako Winamp, XMMX atd.
- Formát kontejneru Ogg (Ogg FLAC).

## Design FLAC

V závislosti na hustotě a amplitudě hudby může být velikost komprimovaného souboru o 80 % menší než velikost původního souboru.

### Zdrojový kodér ###

- Podporuje pouze celočíselné vzorky a ne s plovoucí desetinnou čárkou. Zvládne bitové rozlišení PCM od 4 do 32 bitů na vzorek a vzorkovací frekvenci od 1 Hz do 65 535 Hz. Kódování FLAC je omezeno na 24 bitů na vzorek.
- Kanály lze seskupit, aby bylo možné využít výhod mezikanálových korelací ke zvýšení komprese.
- Kontrolní součty CRC se používají k identifikaci poškozených rámců.
- Pro převod zvukových vzorků používá FLAC lineární predikci.

### Metadata ###

- FLAC podporuje ReplayGain (používá se k vnímání a normalizaci hlasitosti zvuku).
- FLAC používá pro označování stejný systém jako v komentářích Vorbis.
- libFLAC používá většina aplikací FLAC pro kódování/dekódování.
- libFLAC API je organizováno do proudů, vyhledatelných proudů a souborů pro zvýšení abstrakce ze základního bitového proudu FLAC.

### Komprese ###

libFLAC používá úrovně komprese od 0 do 8, kde 0 je nejrychlejší a 8 je nejpomalejší úroveň komprese. Komprimované soubory jsou vždy bezeztrátové, i když kompromis je mezi rychlostí a velikostí.

## FLAC vs MP3
MP3 je formát se ztrátovou kompresí, což znamená, že po použití komprese může snížit část zvuku, aby se zmenšila jeho velikost. Zatímco FLAC je bezztrátový formát souboru, což znamená, že můžete slyšet zvuk v jeho nejčistší podobě. Dříve byly bezztrátové formáty souborů CDA nebo WAV, které nebyly příliš prostorově úsporné jako FLAC. Následující tabulka ukazuje srovnání těchto dvou formátů pro některé důležité termíny:

|Termín|FLAC|MP3|
---|---|---|
|**Kvalita dat**|Žádná ztráta zvukových dat| Některá data mohou být ztracena při komprimaci audio dat|
|**Velikost**|Větší velikost souboru ve srovnání se ztrátovými formáty. Potřebujete tedy větší úložnou kapacitu| Menší velikost souboru, vhodná pro přehrávání na kompaktních audio zařízeních s malým úložným prostorem |
|**Požadavky na hardware**| Potřebujete vysoce kvalitní audio zařízení a obrovskou úložnou kapacitu | Obrovské zvukové knihovny lze uložit do menšího úložného prostoru. Vhodné pro ruční zařízení, jako jsou audio přehrávače nebo mobilní telefony|
|**Distribuce přes internet**|Nelze snadno distribuovat přes internet kvůli velké velikosti souboru |Kompaktní velikost souboru usnadňuje distribuci přes internet|
|**Kompatibilita**|Nejoblíbenější kodek pro poslech hudby a zvuku, který je téměř kompatibilní s každým zařízením na planetě Kompatibilní s počítači nové generace, telefony, AV přijímači, blu-ray přehrávači, streamovacími zařízeními jako Roku nebo Fire TV|

## Reference ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

