{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Torrent filformat - BitTorrent fil",
  "description":"Lær om TORRENT-filer og API'er, der kan oprette og åbne TORRENT-filer.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent-da",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Hvad er en TORRENT fil?

En TORRENT-fil er en tekstfil, der bruges af BitTorrent og andre P2P (peer-to-peer) programmer til download og udveksling af indhold. Det downloadbare indhold kan omfatte dokumenter, videoer, spil, film og andre medier, der er tilgængelige på internettet. Det inkluderer metadataoplysninger om indholdet og placeringen af det medie, der skal downloades. Software som BitTorrent bruger information fra denne fil såsom navn, filstørrelse og mappestruktur til download af data. Torrent-filer kan konverteres til andre filformater såsom [PDF](/pdf/) online.

## Hvad er Torrenting? TORRENT-filformatet til dataudveksling

Torrenting er konceptet med udveksling (download og upload) af datafiler ved hjælp af BitTorrent-netværket. I modsætning til konventionelle servere, hvor data uploades for andre at få adgang til og downloade, hentes og sendes torrentfiler ved hjælp af torrent-netværket. Når en bruger åbner en .torrent-fil i applikationer som BitTorrent, begynder softwaren at downloade indholdet af filen bitvist. Hvis flere brugere har den samme fil, opdeler BitTorrent downloads mellem alle brugerne for at fremskynde processen med at downloade. På samme tid bliver computeren på den bruger, der downloader filen, også kilden til filen for at sende den til andre brugere, som også downloader den samme fil.

### Struktur af en TORRENT-fil

En torrentfil er en kombination af en liste over filer og metadataoplysninger om alle dele af filen, der skal downloades. Den indeholder følgende oplysninger i form af nøgler.

- announce - URL'en på trackeren, der annonceres til andre peers for at informere om tilgængeligheden af filen
- 'info' — Dette knytter sig til en ordbog, hvis nøgler er afhængige af, om en eller flere filer bliver delt:
  - "filer – en liste over ordbøger, der hver svarer til en fil (kun når flere filer deles). Hver ordbog har følgende nøgler:"
- 'længde' — størrelsen af filen i bytes.
- `sti` - en liste over strenge, der svarer til undermappenavne, hvoraf den sidste er det faktiske filnavn
- 'længde' — størrelsen af filen i bytes (kun når en fil deles)
- `navn` — filnavn, hvor filen skal gemmes
- piece length — antal bytes pr. styk. Dette er almindeligvis 28 KiB = 256 KiB = 262.144 B.
- `pieces` — en hash-liste, der er en sammenkædning af hver brik's SHA-1-hash.

## Er torrenting sikkert og lovligt?

Torrenting-protokol til udveksling af data mellem P2P-brugere er sikker, da det kun er midlet til at dele enhver type fil. Protokollen i sig selv er således ikke usikker eller ulovlig. Indholdet, der deles via netværket, kan dog indeholde filer eller medier, der kan krænke de delte dokumenters juridiske status. I sådanne tilfælde kan udvekslingen af sådanne data forårsage retssager mod de parter, der er involveret i at dele sådanne filer offentligt.

## Referencer

* [TORRENT-fil - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)


