{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "file", "extension", "format", "audio interchange bestandsformaat", "music", "aiff file format", "aiff to mp3", "aiff vs wav", "convert aiff to mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over AIFF-bestandsindelingen en API's die AIFF-bestanden kunnen maken, converteren en openen.",
  "title" :"AIFF - Audio Interchange-bestandsindeling",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Wat is een AIFF-bestand?
De AIFF (Audio Interchange File Format) is een niet-gecomprimeerd audiobestandsformaat ontwikkeld door Apple in 1998, maar is gebaseerd op **EA IFF 85** (Standard for Interchange Format Files ontwikkeld door Electronic Arts), een wrapper-formaat dat wordt gebruikt op Amiga-systemen . Dit bestandsformaat komt met een standaard voor het opslaan van gesamplede geluiden. Het formaat is flexibel genoeg en maakt de opslag van mono- of meerkanaals gesamplede geluiden met verschillende samplefrequenties en samplebreedtes mogelijk. Omdat de AIFF-bestanden niet zijn gecomprimeerd, maakt dit ze groter in omvang dan andere verliesgevende formaten zoals [MP3](/audio/mp3/).

AIFF-bestanden bestaan uit 2 kanalen met ongecomprimeerde stereo-audio met een samplegrootte van 16 bits, opgenomen op 44,1 kHz. Vanwege de hoge audiokwaliteit kan een audio van 5 minuten tot 50 MB schijfruimte in beslag nemen, wat vergelijkbaar is met het [WAV](/audio/wav/) bestandsformaat.

## AIFF versus WAV

De AIFF en WAV zijn qua kwaliteit bijna hetzelfde. Beiden gebruiken dezelfde PCM (pulse-code modulatie) codering, waardoor ze groter zijn in vergelijking met andere lossy formaten, zoals [MP3](/audio/mp3/), [M4A](/audio/m4a/). Enkele van de algemene verschillen staan in de onderstaande tabel:

|AIFF|WAV|
---|---|
|Voornamelijk gebruikt voor MAC|Meestal gebruikt voor pc's|
|Maakt metadeta mogelijk| Staat geen metadeta toe|

## AIFF-bestandsstructuur

De **EA IFF 85** bevat een algemene structuur voor het opslaan van gegevens in bestanden. Een **EA IFF 85**-bestand bestaat uit een aantal brokken gegevens. Een blok is een bouwblok van een AIFF-bestand dat bestaat uit wat header-informatie gevolgd door gegevens:
{{< figure src="../chunk.png" alt="AIFF Brokken" >}}

Een AIFF-bestand is een verzameling van een aantal verschillende soorten chunks. Er zijn twee algemene soorten chunks die belangrijk zijn om een AIFF-bestandsbrok te vormen:
- **Common Chunk**: Bevat belangrijke parameters die het gesamplede geluid beschrijven, zoals de lengte en de samplefrequentie.
- **Sound Data Chunk**: bevat de daadwerkelijke audiosamples.
Er zijn veel andere optionele blokken die instrumentparameters weergeven, markeringen definiëren, toepassingsspecifieke informatie opslaan, enz.

### Lokale broktypes

De chunk-types om AIFF te vormen worden gegeven in de onderstaande tabel:

|Brokkentype| Beschrijving|
---|---|
|Common Chunk|De Common Chunk beschrijft fundamentele parameters van het gesamplede geluid|
|Sound Data Chunk|De Sound Data Chunk bevat de daadwerkelijke voorbeeldframes|
|Marker Chunk|De Marker Chunk bevat markeringen die verwijzen naar posities in de geluidsdata|
|Instrument Chunk|De Instrument Chunk definieert basisparameters die een instrument, zoals een sampler, zou kunnen gebruiken om de geluidsgegevens af te spelen|
|MIDI Data Chunk|De MIDI Data Chunk kan worden gebruikt om MIDI-data op te slaan|
|Audio Recording Chunk|De Audio Recording Chunk bevat informatie die relevant is voor audio-opnameapparaten|
|Application Specific Chunk|De Application Specific Chunk kan voor elk doel worden gebruikt door fabrikanten van applicaties|
|Comments Chunk|De Comments Chunk wordt gebruikt om opmerkingen op te slaan in het FORM AIFF|
|Tekstblokken - naam, auteur, copyright, annotatie| Het zijn allemaal stukjes tekst|

## Referenties ##

* [Audio Interchange-bestandsindeling - door Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

