{
  "date" : "2019-10-11",
  "keywords" :[ "j2k-fil", "j2k-filformat", "vad är en j2k-fil", "fil", "j2k-exempel", "j2k-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Läs mer om J2K-filformat och API:er som kan skapa och öppna J2K-filer.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Vad är J2K fil?

En **J2K**-fil är en bild som komprimeras med hjälp av wavelet-komprimering istället för DCT-komprimering. Detta filformat används av Joint Photographic Experts Group (JPEG) 2000-filer. J2K-filer lagrar metadatainformation om bildfilen i XML till skillnad från .jpeg eller .jpg som använder EXIF-formatet för detta ändamål. J2K-filer stöder 15-bitars färg, alfatransparens och förlustfri komprimering. Det finns flera kommersiella API:er för att avkoda JPEG 2000-bilder som J2K-Codec. En J2K-fil kan öppnas på Windows OS med standardbildvisare.

## J2K-filformat ##

J2K-filformatet är detsamma som JPEG 2000 som ofta sparas som .jp2 och .jpc. Detta gör att J2K-filer följer samma tillvägagångssätt för att koda metadata i XML-format där standarden 12234-1 används som referens mellan Exif-taggarna och XML-komponenterna. Det förbättras ytterligare av JPEG 2000 del-2-tillägget som kombinerar animeringsmekanismen och kodströmskonfigurationerna till en enda bild. Sådana filer i utökat filformat sparas som .jpx.

### Layout av en JPEG2000-fil ###

JPEG2000 stöder en mängd olika applikationer baserat på överensstämmelse för utökningsbara filformat. Även om den enklaste typen kan innehålla en enda bild, kan mer komplexa typer inkludera en serie bilder, staplade ovanpå varandra eller är tidsbaserade sekvenserade.

#### JP2 Box ####
Det är byggstenen på högsta nivån i JP2-filformatet och innehåller en typ och längdfält i rubriken och en datasektion. Den mest anmärkningsvärda typen av box är den sammanhängande kodströmsboxen. Denna box lagrar JPEG2000-kodströmmen i sin datasektion.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream är en sekvens av byte som krävs för att avkoda den komprimerade JPEG2000-bilden. Om filen inte har något annat än denna kodström, kallas den en rå kodströmsfil. Vanligtvis är en JPEG-kodström tillämpningen av JPEG2000-komprimeringsalgoritmen på en bild, även om det inte är det enda sättet.

#### Kakeldelar ####

En JPEG2000-kodad bild är en samling dataenheter som kallas paket. Dessa paket underhålls i kodströmmen inuti paketgrupper som kallas tile-parts. Innan du kodar en bild delar kodaren upp bilden i ett rektangulärt rutnät av block, kallade brickor där varje bricka kodas separat, oavsett andra brickor.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 filformat" >}}

## J2K-komprimering ##
JPEG 2000 använder wavelet-komprimeringsteknik vilket gör det snabbt baserat på det faktum att relativt få pixlar visas i vilken visningsport eller vilket fönster betraktaren än visar bilden. Detta kan understrykas av det faktum att endast ett fåtal megabyte pixlar visas på skärmen för mycket stora bilder (i gigabyte). Detta hjälper till att snabbt hämta och rendera endast den del av bilddata som krävs för att fylla visningspixlarna. Detta kräver också höghastighetsdekompressionsteknik för att påskynda bildhämtningsmekanismen för att skapa de bilder som krävs i farten.

J2K drar fördel av snabb dekompression och hämtar endast nödvändig information för pixeldata för att snabbt återge delar av synliga bilder till skärmarna. J2K är främst designad för att visa data och inte redigera den.

## J2K-identifikation ##
JPEG 2000-filer har signaturbyte 6A 50 20 20.

### Mimetyper ###
Registrerade Mime-typer för JPEG 2000-filer inkluderar:
*bild/jp2
* bild/jpx
* bild/jpm
* video/mj2

## Förbättringar jämfört med JPEG-standarden ##
Förbättringar jämfört med JPEG-standarden inkluderar:
* Överlägsen kompressionsprestanda
* Representation med flera upplösningar
* Progressiv överföring med pixel och noggrannhet i upplösning
* Val av förlustfri eller förlustfri komprimering
* Feltålighet, flexibelt filformat
* Stöd för högt dynamiskt omfång
* Rumslig information om sidokanaler

## Referenser ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

