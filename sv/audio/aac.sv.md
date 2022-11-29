{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "fil", "tillägg", "format", "Ljudkodning", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om AAC-filformat och API:er som kan skapa och öppna AAC-filer.",
  "title" :"AAC - Advanced Audio Coding File",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Vad är AAC fil?

AAC (Advanced Audio Coding) hänvisar till digital ljudkodningsstandard som representerar ljudfiler baserade på ljudkomprimering med förlust. Det lanserades som efterföljare till filformatet **[MP3](/sv/audio/mp3/)** med tanke på att laterala inför problem för implementering av nya idéer i kodningsprocessen baserat på utveckling av metoder för datakomprimering. AAC uppnår bättre ljudkvalitet jämfört med MP3 med samma bithastighet. Det definierades i MPEG-2 del 7 (ISO/IEC 13818-7) och i en uppdaterad form i MPEG-4 del 3 (ISO/IEC 14496-3).

AAC-format antogs som standardmediaformat av YouTube, iPhone, iPod, iPad, Apple iTunes och flera andra plattformar. Flera applikationer och API:er är tillgängliga för konvertering av AAC-filformat till andra format som MP3, WMA, M4A, **[WAV](/sv/audio/wav/)** och andra.

### Kort historik för AAC-fil

AAC-filformatet är en förbättrad version av MP3 med vissa förbättringar. Med bidrag från flera företag, inklusive Fraunhofer Institute (Fraunhofer IIS - utvecklare av MP3), Nokia, Dolby, AT&T och Sony, förklarades formatet som en internationell standard av Moving Picture Experts Group (MPEG) i april 1997. Senare 1999, MPEG-2 Part 7 uppdaterades och inkluderades i MPEG-4-familjen av standarder. Den var känd som MPEG-4 Part 3, identifierad som ISO/IEC 14496-3: 1999 eller MPEG-4 Audio.

## AAC-filformatspecifikationer

AAC-filformatsspecifikationerna tillåter mer flexibilitet att designa codec än MP3 gör, vilket resulterar i mer samtidiga kodningsstrategier och effektiv komprimering. Formatet har valts av ett antal hårdvaruplattformar för dess förbättringar jämfört med MP3 när det gäller att ge stöd för fler alternativ även vid mindre bithastigheter. AAC-filformatsspecifikationerna finns tillgängliga som [MPEG-2 del 7](https://www.iso.org/standard/43345.html) och [MPEG-4 del 3](https://www.iso.org /standard/53943.html) (inte gratis att ladda ner). Formatet använder följande mediatyper:

* ljud/aac
* ljud/aacp
* ljud/3gpp
* ljud/3gpp2
* ljud/mp4
* ljud/mp4a-latm
* ljud/mpeg4-generiskt

## AAC vs MP3 – Förbättringar ##

De viktigaste skillnaderna mellan AAC och MP3 när det gäller förbättringar är följande:

* AAC stöder ett bredare utbud av kanaler (upp till 48) och samplingsfrekvenser (från 8 kHz till 96 kHz)
* AAC har bättre kodningsfrekvenser över 16 kHz
* AAC har bredare variationsgränser i frekvens-tidsupplösningen för en filterbank som har lett till förbättrad kodning av transienter och stationära delar av ljudsignalen
* Effektivare och enklare filterbank: en hybridfilterbank har ersatts av standard MDCT (modifierad diskret cosinustransform)
* Stöder förbättrad effektivitet av komprimering med hjälp av Temporal Noise Shaping (TNS), prediktionskoefficienterna för MDCT-tid (långtidsprediktion), parametrisk stereo, perceptuell brussubstitution, spektralbandreplikering (SBR).
* mer flexibel ledstereo (olika metoder kan användas i olika frekvensområden);

## Referenser ##

* [AAC - av Wikipedia](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

