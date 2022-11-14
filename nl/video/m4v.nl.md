{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "bestand", "extensie", "format", "MPEG-4", "Digital Rights Management", "DRM", "Apple", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Meer informatie over M4V-bestandsindeling en API's die M4V-bestanden kunnen maken en openen.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Wat is een M4V-bestand?

**M4V**-bestandsindeling, ontwikkeld door Apple, is een videocontainer die optioneel wordt beschermd met Digital Rights Management (DRM) kopieerbeveiliging om privacy of kopiëren te beschermen. Video's en audiotracks worden omhuld door containerbestanden om afspeelstreams te indexeren en te organiseren. Daarnaast bieden containers ook de functie van hoofdstukken die vergelijkbaar zijn met die op dvd's. Apple gebruikt M4V om video's in de iTunes Store te coderen. Het beschermt ongeoorloofde reproductie via Apple's FairPlay-kopieerbeveiliging door toe te staan dat M4V-bestanden worden afgespeeld op alleen geautoriseerde computers met de accounts die zijn gebruikt om de video te kopen. Als DRM-beveiliging echter wordt verwijderd van M4V-bestanden, kunnen deze bestanden worden afgespeeld in andere videospelers door de extensie te wijzigen van .m4v naar .mp4. Daarom worden M4V-bestanden geassocieerd met MPEG-4. M4V gebruikt H.264 voor video en **[AAC](/nl/audio/aac/)** en Dolby Digital voor audiocodering en -decodering.

## M4V-bestandsstructuur ##

M4V-bestanden hebben continue chunks met een header van 8 bytes, een chunkgrootte van 4 bytes en een chunktype van 4 bytes in elk chunk. Het eerste blok is "ftype" en heeft een subtype op offset 8. M4V gedefinieerd door subtype dat "M4V_" moet zijn. Andere chunks zijn voorgedefinieerde handtekeningen: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PICT". Door chunks te herhalen, totdat een onbekend type wordt gedetecteerd, stellen we een M4V-bestand samen.

Hier is een onderzoek van een voorbeeld: De binaire gegevens van een voorbeeld van een m4v-bestand worden geïnspecteerd via Hex Viewer en het kan worden waargenomen dat het begint met een handtekening **ftyp** (hex: 66 74 79 70) op offset 4, wat QuickTime definieert Type containerbestand. Het bestandssubtype is **M4V_** (hex: 4D 34 56 20) wat verwijst naar het M4V (MPEG-4) bestandstype. De eerste blokgrootte is 32 (hex: 00 00 00 20, big-endian, high byte first), de grootte bevindt zich op offset 0. Bij offset 32 (hex: 20) bevindt zich de tweede chunk, die een grootte heeft van 30.322 (hex : 00 00 76 72, big-endian, eerst lagere byte) en typ **moov** (hex: 6D 6F 6F 76). De volgende chunk bevindt zich op offset 32+30,322#30,354 (hex: 00 00 76 92) en heeft maat 8 (hex: 00 00 00 08) en type **free** (hex: 66 72 65 65).
### Codecs gebruikt in M4V ###

#### Videocodec H.264 ####

H.264 is een standaard voor videocompressie die digitale video converteert naar een formaat dat minder ruimte nodig heeft bij verzending of opslag. M4V gebruikt H.264 voor videocompressie. De toepassing varieert van dvd, tv, videoconferenties en videostreaming via internet. H.264 bestaat uit twee hoofdonderdelen: Encoder – Die de video comprimeert, Decoder – Die de gecomprimeerde video terug decomprimeert. In de onderstaande afbeelding worden coderings- en decoderingsprocessen gemarkeerd en andere processen worden behandeld in de H.264-standaard.

##### Videocodering en decoderingsproces in H.264 #####

Voor de gecomprimeerde H.264-bitstream voert de video-encoder het voorspellings-, transformatie- en coderingsproces uit. Tegelijkertijd voert de decoder het omgekeerde proces van decodering, inverse transformatie en reconstructie uit om het videobestand terug te produceren. H.264 neemt de helft van de grootte van de MPEG in beslag.

#### Audiocodec ####

Advanced Audio Coding (AAC) is een audiocodec voor lossy digitale audiocompressie en wordt gebruikt in een M4V-container. AAC is de opvolger van het [MP3](/nl/audio/mp3/) formaat en bereikt met dezelfde bitrate een betere kwaliteit dan MP3. AAC-formaat gooit wat informatie weg tijdens het compressieproces, wat van minder belang is. AAC is een op blokken gebaseerde codec met variabele bitrate (VBR) waarbij elk blok decodeert tot 1024 tijddomein-samples.

### Referenties ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

