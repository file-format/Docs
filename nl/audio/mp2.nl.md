{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "mp2-bestand", "extensie", "format", "wat is een mp2-bestand", "muziek", "mp2-bestandsformaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over MP2-bestandsindelingen en API's die MP2-bestanden kunnen maken, converteren en openen.",
  "title" :"MP2 - MPEG Layer 2 audiobestandsindeling",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Wat is een MP2-bestand?

Een MP2-bestand dat ook wel MPA-bestand wordt genoemd, is een audiobestand dat is gecomprimeerd met Layer II van MPEG-1 of MPEG-2; een lossy audiocompressieformaat gedefinieerd door ISO/IEC 11172-3 naast MPEG-1 Audio Layer I en MPEG-1 Audio Layer III ([MP3](/nl/audio/mp3/)), om de grootte van het audiobestand te verkleinen. Terwijl MP3 populairder is dan MP2 vanwege de kleinere omvang en beschikbaarheid via internet. Daarom is MP2 nog steeds een essentiële standaard voor audio-uitzendingen.

## MP2-bestandsindeling

MPEG Audio Layer II (MP2) is het kernalgoritme van de MP3-standaarden. MPEG-1 Audio Layer 2-codering is verkregen van de MUSICAM-audiocodec. Het begon als het Digital Audio Broadcast (DAB)-project in Duitsland als onderdeel van het EUREKA-onderzoeksprogramma. De Eureka 147 bevatte drie hoofdelementen: Transmission Coding & Multiplexing, COFDM Modulation en MUSICAM Audio Coding (Masking pattern Universal Sub-band Integrated Coding And Multiplexing). De MUSICAM was een van de weinige coderingen die een hoge geluidskwaliteit kon bereiken met bitsnelheden in het bereik van 64 tot 192 kbit/s per monofoon kanaal. Het doel was om lage vertraging, lage complexiteit, foutrobuustheid, korte toegangseenheden te bieden en te voldoen aan de technische vereisten van uitzending, telecommunicatie en opname op digitale opslagmedia.

MP2 is een subband audio-encoder, die in het tijdsdomein kan worden gecomprimeerd met een low-delay filterbank die 32 frequentiedomeincomponenten genereert. Ter vergelijking: MP3 is een transformatie audio-encoder met hybride filterbank, wat betekent dat compressie wordt toegepast in het frequentiedomein na een hybride transformatie vanuit het tijddomein. De MP2-encoder kan gebruikmaken van redundantie tussen kanalen door gebruik te maken van optionele "joint stereo"-intensiteitscodering.

### Specificaties MP2-bestandsindeling

Het MP2-bestandsformaat is gebaseerd op opeenvolgende digitale frames van 1152 bemonsteringsintervallen met vier mogelijke formaten:

- mono-formaat
- stereoformaat
- intensiteit gecodeerd gezamenlijk stereoformaat (stereo irrelevantie)
- tweekanaals (niet-gecorreleerd) formaat
Enkele belangrijke technische specificaties van MP2 staan in de onderstaande tabel:

|Specificatie| Beschrijving|
---|---|
|**Bemonsteringspercentages**| 32, 44,1 en 48 kHz|
|**Bitsnelheden**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 en 384 kbit/s|
|**Extra bemonsteringsfrequenties**|16, 22,05 en 24 kHz|
|**Extra bitsnelheden**|8, 16, 24, 40 en 144 kbit/s|
|**Meerkanaalsondersteuning**|Tot 5 audiokanalen met volledig bereik en een LFE-kanaal (Low Frequency Enhancement-kanaal)|

## Referenties ##

* [MPEG-1 Audio Layer II - Door Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

