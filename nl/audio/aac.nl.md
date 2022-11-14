{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "bestand", "extensie", "formaat", "Audiocodering", "MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over AAC-bestandsindelingen en API's die AAC-bestanden kunnen maken en openen.",
  "title" :"AAC - Geavanceerd audiocoderingsbestand",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Wat is een AAC-bestand?

AAC (Advanced Audio Coding) verwijst naar de standaard voor digitale audiocodering die audiobestanden vertegenwoordigt op basis van audiocompressie met verlies. Het werd gelanceerd als opvolger van het **[MP3](/nl/audio/mp3/)** bestandsformaat, rekening houdend met de laterale problemen voor de implementatie van nieuwe ideeën in het coderingsproces op basis van de ontwikkeling van methoden voor datacompressie. AAC bereikt een betere geluidskwaliteit in vergelijking met MP3 bij dezelfde bitsnelheid. Het werd gedefinieerd in MPEG-2 Part 7 (ISO/IEC 13818-7), en in een bijgewerkte vorm in MPEG-4 Part 3 (ISO/IEC 14496-3).

Het AAC-formaat werd door YouTube, iPhone, iPod, iPad, Apple iTunes en verschillende andere platforms als standaard mediaformaat aangenomen. Er zijn verschillende toepassingen en API's beschikbaar voor de conversie van het AAC-bestandsformaat naar andere formaten zoals MP3, WMA, M4A, **[WAV](/nl/audio/wav/)** en andere.

### Korte geschiedenis van AAC-bestand

Het AAC-bestandsformaat is een verbeterde versie van MP3 met enkele verbeteringen. Bijgedragen door verschillende bedrijven, waaronder het Fraunhofer Institute (Fraunhofer IIS - ontwikkelaars van MP3), Nokia, Dolby, AT&T en Sony, werd het formaat in april 1997 door Moving Picture Experts Group (MPEG) uitgeroepen tot een internationale standaard. Later in 1999, de MPEG-2 Part 7 is bijgewerkt en opgenomen in de MPEG-4-familie van normen. Het stond bekend als MPEG-4 Part 3, geïdentificeerd als ISO/IEC 14496-3: 1999 of MPEG-4 Audio.

## Specificaties AAC-bestandsindeling

De specificaties van het AAC-bestandsformaat bieden meer flexibiliteit om codecs te ontwerpen dan MP3, wat resulteert in meer gelijktijdige coderingsstrategieën en efficiënte compressie. Het formaat is door een aantal hardwareplatforms gekozen vanwege de verbeteringen ten opzichte van MP3 in termen van ondersteuning voor meer opties, zelfs bij lagere bitrates. De specificaties van de AAC-bestandsindeling zijn beschikbaar als [MPEG-2 Part 7](https://www.iso.org/standard/43345.html) en [MPEG-4 Part 3](https://www.iso.org /standard/53943.html) (niet gratis te downloaden). Het formaat gebruikt de volgende mediatypes:

* audio/aac
* audio/aacp
* audio/3gpp
* audio/3gpp2
* audio/mp4
* audio/mp4a-latm
* audio/mpeg4-generiek

## AAC versus MP3 - Verbeteringen ##

De belangrijkste verschillen tussen AAC en MP3 in termen van verbeteringen zijn als volgt:

* AAC ondersteunt een breder scala aan kanalen (tot 48) en bemonsteringsfrequenties (van 8 kHz tot 96 kHz)
* AAC heeft betere coderingsfrequenties boven 16 kHz
* AAC heeft ruimere variatielimieten in de frequentie-tijdresolutie van een reeks filters die hebben geleid tot een verbeterde codering van transiënten en stationaire delen van het audiosignaal
* Efficiëntere en eenvoudigere filterbank: een hybride filterbank is vervangen door de standaard MDCT (gemodificeerde discrete cosinustransformatie)
* Ondersteunt verbeterde effectiviteit van compressie met behulp van Temporal Noise Shaping (TNS), de voorspellingscoëfficiënten van MDCT-tijd (voorspelling op lange termijn), parametrische stereo, perceptuele ruissubstitutie, spectrale bandreplicatie (SBR).
* flexibelere gezamenlijke stereo (verschillende methoden kunnen worden gebruikt in verschillende frequentiebereiken);

## Referenties ##

* [AAC - Door Wikipedia](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

