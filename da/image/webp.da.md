{
  "date": "2019-10-11",
  "keywords": [
"webp-fil",
"webp filformat",
"hvad er en webp-fil",
"fil",
"webp eksempel",
"webp filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WEBP - Google Raster Image File Format",
  "description": "Lær om WEBP-filformat og API'er, der kan oprette og åbne WEBP-filer.",
  "linktitle": "WEBP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-webp"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en WEBP fil?

WebP, introduceret af Google, er et moderne rasterwebbilledfilformat, der er baseret på tabsfri og tabsgivende komprimering. Det giver samme billedkvalitet og reducerer billedstørrelsen betydeligt. Da de fleste af websiderne bruger billeder som effektiv repræsentation af data, resulterer brugen af WebP-billeder på websider i hurtigere indlæsning af websider. Ifølge Google er WebP-tabsfrie billeder 26 % mindre i størrelse sammenlignet med [PNGs](/image/png/), mens WebP-tabsløse billeder er 25-34 % mindre end sammenlignelige [JPEG](/image/jpeg/)-billeder. Billeder sammenlignes baseret på SSIM-indekset (Structural Similarity) mellem WebP og andre billedfilformater. WebP er et søsterprojekt af [WebM](https://en.wikipedia.org/wiki/WebM) multimediebeholderformat.

## WebP-funktionsoversigt ##

WebP-billeder bruger komprimeringsprocessen baseret på forudsigelse af pixels fra deres omgivende blokke, hvilket resulterer i, at pixels bruges flere gange i en enkelt fil. Det understøtter animerede billeder og forventes at understøtte flere funktioner i fremtiden. Google har stillet kildekoden [online](https://developers.google.com/speed/webp/download) til rådighed for dens koder og dekoder, så den kan bruges, hvor det er nødvendigt. WebP-billedet understøtter:

* **Tabskomprimering:** Den tabsgivende komprimering er baseret på [VP8](https://en.wikipedia.org/wiki/VP8) nøglerammekodning. VP8 er et videokomprimeringsformat skabt af On2 Technologies som en efterfølger til VP6- og VP7-formaterne.

* **Tabsfri komprimering:** Det tabsfri komprimeringsformat er udviklet af WebP-teamet.

* **Transparens:** 8-bit alfakanal er nyttig til grafiske billeder. Alfakanalen kan bruges sammen med RGB med tab, en funktion, der i øjeblikket ikke er tilgængelig med noget andet format.

* **Animation:** Det understøtter animerede billeder i ægte farver.

* **Metadata:** Det kan have EXIF- og XMP-metadata (bruges f.eks. af kameraer).

* **Farveprofil:** Det kan have en indlejret ICC-profil.


Lossy WebP-komprimering bruger forudsigelig kodning til at kode et billede, den samme metode, som bruges af VP8-videocodec til at komprimere keyframes i videoer. Forudsigelig kodning bruger værdierne i naboblokke af pixels til at forudsige værdierne i en blok og koder derefter kun forskellen.

Tabsfri WebP-komprimering bruger allerede sete billedfragmenter for nøjagtigt at rekonstruere nye pixels. Den kan også bruge en lokal palet, hvis der ikke findes noget interessant match.

## Filformat ##

WebP-filformatet er baseret på RIFF-dokumentformatet (ressourceudvekslingsfilformat). WebP-beholderen understøtter ud over funktioner end kun at indeholde et enkelt billede kodet som en VP8-nøgleramme. Det grundlæggende element i en RIFF-fil er en del, der består af:


|Felt|Beskrivelse
---|---|
|Chunk FourCC: 32 bit|ASCII fire-tegns kode brugt til chunk identifikation
|Chunk Size: 32 bits (uint32)|The size of the chunk not including this field, the chunk identifier or paddi-dang
|Chunk Payload: Chunk Size bytes|Datanyttelasten. Hvis Chunk Size er ulige, tilføjes en enkelt polstringsbyte ~-~-, der skal være 0 ~-~-
|ChunkHeader ('ABCD')|Bruges til at beskrive FourCC- og Chunk Size-headeren for individuelle chunks, hvor 'ABCD' er FourCC for chunken. Dette elements størrelse er 8 bytes.

### WebP Header ###

En WebP-filoverskrift er som følger:

* RIFF Header - 32 bit, der repræsenterer ASCII-tegnene 'R' 'I' 'F' 'F'

* Filstørrelse - 32 bit (uint32) repræsenterer størrelsen af filen i bytes startende ved offset 8. Den maksimale værdi af dette felt er 2^32 minus 10 bytes og dermed er størrelsen af hele filen højst 4GiB minus 2 bytes .

* 'WEBP' - 32 bits repræsenterer ASCII-tegnene 'W' 'E' 'B' 'P'


### Lossy filformat ###

WebP-billeder bruger filformatet med tab, hvis billedet er baseret på kodning med tab og ikke kræver nogen avancerede/udvidede funktioner såsom gennemsigtighed, animation, alfa osv. Billeder med tab er mindre og understøttes også af de ældre programmer.

WebP-filen består i dette tilfælde af:

* 12 bytes WebP-filoverskrift

* VP8 Chunk


[VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) illustrerer VP8-bitstreamformatspecifikationerne.

### Filformat uden tab ###

Dette layout bruges, når billedet er baseret på tabsfri kodning, og der ikke er behov for de avancerede funktioner i det eksterne format. Ældre programmer kan dog muligvis ikke læse sådanne filer.

WebP-filen består i dette tilfælde af:

* 12 bytes WebP-filoverskrift

* VP8L Chunk


## Referencer ##

* [WebP Developer's Reference - Af Google](https://developers.google.com/speed/webp/)

* [WebP-filformat - af Wikipedia](https://en.wikipedia.org/wiki/WebP)


