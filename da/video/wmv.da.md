{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMV filformat",
  "description": "Lær om WMV-filformat og API'er, der kan oprette og åbne WMV-filer.",
  "linktitle": "WMV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-wm-dav"
}
},
  "lastmod": "2019-09-16"
}

## Hvad er en WMV fil?

Advanced Systems Format (ASF) er en digital multimediebeholder designet primært til lagring og transmission af mediestrømme. Microsoft Windows Media Video (WMV) er det komprimerede videoformat og Microsoft Windows Media Audio (WMA) er det komprimerede lydformat sammen med yderligere metadata i ASF-beholderen udviklet af Microsoft. Når først WMV- eller WMA-filerne er kodet med Windows Media Video og Windows Media Audio-codecs, er de repræsenteret med .asf-udvidelsen. WMV komprimerer store filer for en bedre transmissionshastighed over et netværk, mens kvaliteten af videoen bevares. WMV er specielt designet til at køre på alle Windows-enheder. Efter standardiseringen af Society of Motion Picture and Television Engineers (SMPTE) anses WMV nu for at være et åbent standardformat.

## Historie ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. Forbedringer blev tilføjet i yderligere to versioner, dvs. WMV8 og 9. Microsoft indsendte en 9^^th^^ version af WMV til SMPTE til standardisering i 2003, som til sidst blev standardiseret i 2006 som SMPTE 421M også kendt som VC-1. Ideen bag WMV var at udvikle et medieformat, der kunne understøttes af al den Microsoft-understøttede hardware og software. Et andet hovedformål var desuden at overføre videostreams over internettet i et optimalt scenarie. Efter standardiseringen fra SMPTE blev WMV også et videoformat til Blu-ray-diske.

## Filformatspecifikationer

### Container

Generelt pakkes WMV i en ASF-beholder, men derudover kan Matroska- eller AVI-beholderen også understøtte den med udvidelser på henholdsvis .mkv og .avi.

### Windows Media Video 9

Selvom der er forskellige audio- og video-codecs tilgængelige i Windows Media Video 9-serien til oprettelse og afspilning af digitale medier, er WMV-9-codec det nyeste og bedste video-codec, da det kan opnå den optimale komprimering fra meget lave bithastigheder, dvs. 160 x 120 ved 10 Kbps til 1920 x 1080 ved 4-8 Mbps for en række forskellige HD-videoer.

### Codec's struktur

WMV-9 har et 8 bit 4:2:0 internt farveformat. Som alle andre populære videokomprimeringsstandarder MPEG-1 og H.261 bruger WMV-9 en blokbaseret bevægelseskompensation og rumlig transformation. Generelt kan vi sige, at disse standarder udfører blok-for-blok bevægelseskompensation fra den tidligere rekonstruerede ramme ved hjælp af en 2-D størrelse kaldet bevægelsesvektoren (MV) for at signalere rumlig forskydning. Den aktuelle blok dannes ved hjælp af at forudsige værdierne fra den samme størrelse tidligere rekonstruerede ramme, som er forskudt fra den aktuelle position af bevægelsesvektoren. Til sidst beregnes restfejlen som forskellen mellem den bevægelseskompenserede forudsagte blok og den faktiske blok. Denne resterende fejl transformeres ved hjælp af en lineær energikomprimerende transformation, der derefter kvantificeres og entropikodes.

Quantized transform coefficients are entropy decoded, de-quantized, and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

Resten af afsnittet vil diskutere de nye forbedringer i WMV-9, som adskiller den fra resten af videokodningsløsninger som MPEG-standarder. WMV-9 har intra (I), forudsagte (P) og tovejs forudsagte (B) rammer. Intra frames er dem, der er kodet uafhængigt og ikke er afhængige af andre frames. Forudsagte frames er frames, der afhænger af én frame i fortiden. Afkodning af en forudsagt ramme kan kun forekomme, efter at alle referencerammer forud for den aktuelle ramme startende fra den seneste (I) ramme er blevet afkodet. B-rammer er rammer, der har to referencer - en i den tidsmæssige fortid og en i den tidsmæssige fremtid. B-rammer transmitteres efter deres referencer, hvilket betyder, at B-frames sendes ud af funktion for at sikre, at deres referencer er tilgængelige på tidspunktet for afkodningen. B-frames i WMV-9 bruges ikke som reference for efterfølgende frames. Dette placerer B-frames uden for afkodningsløkken, hvilket gør det muligt at tage genveje under afkodningen af B-frames uden drift eller langsigtede visuelle artefakter. Ovenstående definition af I-, P- og B-rammer gælder for både progressive og interlaced-sekvenser.

Ydeevnen af video-codecs sammenlignes med deres rate-distortion (RD) plot. Det er en 2-D kurve, der viser den forvrængning, der produceres af komprimeringen ved en bestemt bitrate.

WMV-9 har løst dette problem med introduktionen af en række forskellige teknikker, der er anført nedenfor:

1. Adaptiv blokstørrelsestransformation

2. Transformationssæt med begrænset præcision

3. Bevægelseskompensation

4. Kvantisering og dekvantisering

5. Avanceret entropikodning

6. Loop-filtrering

7. Avanceret B-rammekodning

8. Interlace-kodning

9. Overlap udjævning

10. Lavprisværktøjer

11. Faldende kompensation

## Referencer

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html )

* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


