{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "bestand", "extensie", "format", "audio-uitwisselingsbestandsformaat", "muziek"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over WAV-bestandsindeling en API's die WAV-bestanden kunnen maken en openen.",
  "title" :"WAV - Waveform Audio File Format",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Wat is een WAV-bestand?

WAV, bekend van WAVE (Waveform Audio File Format), is een subset van Microsoft's Resource Interchange File Format (RIFF)-specificatie voor het opslaan van digitale audiobestanden. Het formaat past geen compressie toe op de bitstream en slaat de audio-opnames op met verschillende bemonsteringsfrequenties en bitsnelheden. Het was en is een van de standaardformaten voor audio-cd's. Wave-bestanden zijn groter in vergelijking met nieuwe audiobestandsindelingen zoals [MP3](/nl/audio/mp3/) die compressie met verlies gebruikt om de bestandsgrootte te verkleinen met behoud van dezelfde audiokwaliteit. WAV-bestanden kunnen echter worden gecomprimeerd met behulp van Audio Compression Manager (ACM) codecs. Er zijn verschillende API's en applicaties beschikbaar die WAV-bestanden kunnen converteren naar andere populaire audiobestandsformaten.

**Wist je dat?**
U kunt een bijdrager worden op FileFormat.com om de gemeenschap voor bestandsindelingen op de hoogte te houden van uw bevindingen. Als u iets wilt delen over WAV- of audiobestandsindelingen, kunt u uw bevindingen posten in het gedeelte [Audio File Format News](https://news.fileformat.com/t/audio) zodat mensen op de hoogte blijven.

## WAV-bestandsindeling ##

Het WAVE-bestandsformaat, dat een subset is van de RIFF-specificatie van Microsoft, begint met een bestandsheader gevolgd door een reeks gegevensbrokken. Een WAVE-bestand heeft een enkele "WAVE"-chunk die uit twee sub-chunks bestaat:

* een "fmt" chunk - specificeert het dataformaat
* een "data"-chunk - bevat de daadwerkelijke voorbeeldgegevens

### WAV-bestandskop ###

De header van een WAV (RIFF)-bestand is 44 bytes lang en heeft het volgende formaat:


|Posities|Voorbeeldwaarde|Beschrijving
---|---|---|
|1 - 4|"RIFF"|Markeert het bestand als een riff-bestand. Tekens zijn elk 1 byte lang.
|5 - 8|Bestandsgrootte (geheel getal)|Grootte van het totale bestand - 8 bytes, in bytes (32-bits geheel getal). Normaal gesproken vult u dit in na het maken.
|9 -12|"WAVE"|Bestandstypekoptekst. Voor onze doeleinden is het altijd gelijk aan "WAVE".
|13-16|"fmt "|Brokken marker opmaken. Inclusief trailing null
|17-20|16|Lengte van formaatgegevens zoals hierboven vermeld
|21-22|1|Type formaat (1 is PCM) - 2 byte integer
|23-24|2|Aantal kanalen - geheel getal van 2 bytes
|25-28|44100|Sample Rate - 32 byte integer. Gebruikelijke waarden zijn 44100 (CD), 48000 (DAT). Sample Rate = Aantal samples per seconde, of Hertz.
|29-32|176400|(Bemonsteringsfrequentie * BitsPerSample * Kanalen) / 8.
|33-34|4|(BitsPerSample * Kanalen) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Bits per monster
|37-40|"data"|"data" chunk header. Markeert het begin van de gegevenssectie.
|41-44|Bestandsgrootte (gegevens)|Grootte van de gegevenssectie.
|Voorbeeldwaarden zijn hierboven gegeven voor een 16-bits stereobron.

## Referenties ##

* [WAV - Door Wikipedia](https://en.wikipedia.org/wiki/WAV)

