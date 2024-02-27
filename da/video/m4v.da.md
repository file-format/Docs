{
  "date": "2019-10-11",
  "keywords": [
"M4V",
"fil",
"udvidelse",
"format",
"MPEG-4",
"Digital Rights Management",
"DRM",
"Æble",
"video"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "Lær om M4V filformat og API'er, der kan oprette og åbne M4V filer.",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-dav"
}
},
  "lastmod": "2019-09-14"
}

## Hvad er en M4V fil?

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. M4V bruger H.264 til video og **[AAC](/audio/aac/)** og Dolby Digital til lydkodning og afkodning.

## M4V filstruktur ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V defineret af undertype, som skal være M4V_. Yderligere chunks-typer er foruddefinerede signaturer: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide , indlæs, ctab, imap, mat, kmat, klip, crgn, sync, chap, tmcd, scpt, ssrc,  BILLEDE. Gentager bidder, indtil ukendt type er fundet, komponerer vi M4V-fil.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Ved offset 32 (hex: 20) er den anden chunk placeret, som har en størrelse på 30.322 (hex: 00 00 76 72, big-endian, lavere byte først) og skriv **moov** (hex: 6D 6F 6F 76). Den næste chunk er placeret ved offset 32+30,322#30,354 (hex: 00 00 76 92) og har en størrelse 8 (hex: 00 00 00 08) og type **fri** (hex: 66 72 65 65).
### Codecs brugt i M4V ###

#### Video Codec H.264 ####

H.264 er en videokomprimeringsstandard, der konverterer digital video til et format, der kræver mindre plads, når det kræves transmission eller lagring. M4V bruger H.264 til videokomprimering. Dens anvendelse spænder fra DVD, TV, videokonferencer og videostreaming over internettet. H.264 består af to hoveddele: Encoder – som komprimerer videoen, Decoder – som udpakker den komprimerede video tilbage. I figuren nedenfor er kodnings- og afkodningsprocesser fremhævet, og andre processer er dækket af H.264-standarden.

##### Videokodnings- og afkodningsproces i H.264 #####

For den komprimerede H.264 bitstream udfører videokoderen forudsigelse, transformation og kodningsprocessen. Samtidig udfører dekoderen den omvendte proces med afkodning, invers transformation og rekonstruktion for at producere videofilen tilbage. H.264 tager halvdelen af størrelsen af MPEG.

#### Audio Codec ####

Advanced Audio Coding (AAC) er et audio-codec til digital lydkomprimering med tab og bruges i en M4V-beholder. AAC er efterfølgeren til [MP3](/audio/mp3/)-formatet og opnår bedre kvalitet end MP3 med samme bitrate. AAC-format smider nogle oplysninger væk under komprimeringsprocessen, hvilket er af mindre betydning. AAC er en variabel bitrate (VBR) blokbaseret codec, hvor hver blok afkoder til 1024 tidsdomæneeksempler.

### Referencer ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)

* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


