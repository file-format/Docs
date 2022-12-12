{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "soubor", "přípona", "formát", "Kódování zvuku", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru AAC a rozhraních API, která mohou vytvářet a otevírat soubory AAC.",
  "title" :"AAC - Advanced Audio Coding File",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Co je soubor AAC?

AAC (Advanced Audio Coding) označuje standard kódování digitálního zvuku, který představuje zvukové soubory založené na ztrátové kompresi zvuku. Byl spuštěn jako nástupce **[MP3](/cs/audio/mp3/)** formátu souboru s ohledem na to, že strana čelí problémům s implementací nových nápadů v procesu kódování založeném na vývoji metod pro kompresi dat. AAC dosahuje lepší kvality zvuku ve srovnání s MP3 při stejné přenosové rychlosti. Byl definován v MPEG-2 Part 7 (ISO/IEC 13818-7) a v aktualizované podobě v MPEG-4 Part 3 (ISO/IEC 14496-3).

Formát AAC přijaly YouTube, iPhone, iPod, iPad, Apple iTunes a několik dalších platforem jako výchozí formát médií. Pro převod formátu souboru AAC do jiných formátů, jako jsou MP3, WMA, M4A, **[WAV](/cs/audio/wav/)** a další, je k dispozici několik aplikací a rozhraní API.

### Stručná historie souboru AAC

Formát souboru AAC je vylepšená verze MP3 s některými vylepšeními. S přispěním několika společností včetně Fraunhofer Institute (Fraunhofer IIS - vývojáři MP3), Nokia, Dolby, AT&T a Sony byl tento formát prohlášen za mezinárodní standard Moving Picture Experts Group (MPEG) v dubnu 1997. Později v roce 1999 MPEG-2 Part 7 byl aktualizován a zahrnut do rodiny standardů MPEG-4. Byl známý jako MPEG-4 Part 3, identifikovaný jako ISO/IEC 14496-3: 1999 nebo MPEG-4 Audio.

## Specifikace formátu souboru AAC

Specifikace formátu souboru AAC umožňují větší flexibilitu při navrhování kodeků než MP3, což má za následek více souběžných strategií kódování a účinnější kompresi. Formát byl vybrán řadou hardwarových platforem pro jeho vylepšení oproti MP3, pokud jde o poskytování podpory více možností i při nižších bitratech. Specifikace formátu souboru AAC jsou k dispozici jako [MPEG-2 část 7](https://www.iso.org/standard/43345.html) a [MPEG-4 část 3](https://www.iso.org /standard/53943.html) (není zdarma ke stažení). Formát používá následující typy médií:

* audio/aac
* audio/aacp
* audio/3gpp
* audio/3gpp2
* audio/mp4
* audio/mp4a-latm
* audio/mpeg4-generické

## AAC vs MP3 – Vylepšení ##

Hlavní rozdíly mezi AAC a MP3 z hlediska vylepšení jsou následující:

* AAC podporuje širší rozsah kanálů (až 48) a vzorkovací frekvence (od 8 kHz do 96 kHz)
* AAC má lepší kódovací frekvence nad 16 kHz
* AAC má širší limity variací ve frekvenčně-časovém rozlišení banky filtrů, které vedly k lepšímu kódování přechodných a stacionárních částí audio signálu
* Efektivnější a jednodušší banka filtrů: hybridní banka filtrů byla nahrazena standardní MDCT (modifikovaná diskrétní kosinusová transformace)
* Podporuje zvýšenou účinnost komprese pomocí Temporal Noise Shaping (TNS), predikční koeficienty MDCT-time (dlouhodobá predikce), parametrické stereo, percepční substituce šumu, replikace spektrálního pásma (SBR).
* flexibilnější joint stereo (lze použít různé metody v různých frekvenčních rozsazích);

## Reference ##

* [AAC – z Wikipedie](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

