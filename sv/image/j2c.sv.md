{
  "date" : "2019-10-11",
  "keywords" :[ "j2c fil", "j2c filformat", "vad är en j2c fil", "fil", "j2c exempel", "j2c filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Läs mer om J2C-filformat och API:er som kan skapa och öppna J2C-filer.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Vad är J2C fil?

En fil med filtillägget .j2c är en variant av JPEG-filformatet och komprimeras med wavelet-komprimeringen. Den har nästan identiskt system av markörer och segment som JPEG 2000-filformatet. J2C-filformatet är som definierat i del 1 av JPEG 2000-stativet som stöder både förlustfri och förlustfri komprimering. JPEG 2000-kodströmmen har utformats för att bäddas in i [JP2](/sv/image/jp2/) eller ett annat filformat, även om det kan visas i en fil för sig. En J2C-fil kan öppnas med Adobe Photoshop 2020, Adobe Illustrator 2020 och Corel Paintshop Pro.

## J2C filformat

J2C-filformatet är detsamma som JPEG 2000 som ofta sparas som .jp2 och .jpc. Detta gör att J2C-filer följer samma metod för att koda metadata i XML-format där standarden 12234-1 används som referens mellan Exif-taggarna och XML-komponenterna. Det förbättras ytterligare av JPEG 2000 del-2-tillägget som kombinerar animeringsmekanismen och kodströmskonfigurationerna till en enda bild. Sådana filer i utökat filformat sparas som [.jpx](/sv/image/jpx/).

### Layout av en JPEG2000-fil

JPEG2000 stöder en mängd olika applikationer baserat på överensstämmelse för utökningsbara filformat. Även om den enklaste typen kan innehålla en enda bild, kan mer komplexa typer inkludera en serie bilder, staplade ovanpå varandra eller är tidsbaserade sekvenserade.

#### JP2 Box
Det är byggstenen på högsta nivån i JP2-filformatet och innehåller en typ och längdfält i rubriken och en datasektion. Den mest anmärkningsvärda typen av box är den sammanhängande kodströmsboxen. Denna box lagrar JPEG2000-kodströmmen i sin datasektion.

#### JPEG2000 CodeStream

JPEG2000 CodeStream är en sekvens av byte som krävs för att avkoda den komprimerade JPEG2000-bilden. Om filen inte har något annat än denna kodström, kallas den en rå kodströmsfil. Vanligtvis är en JPEG-kodström tillämpningen av JPEG2000-komprimeringsalgoritmen på en bild, även om det inte är det enda sättet.

#### Kakeldelar ####

En JPEG2000-kodad bild är en samling dataenheter som kallas paket. Dessa paket underhålls i kodströmmen inuti paketgrupper som kallas tile-parts. Innan du kodar en bild delar kodaren upp bilden i ett rektangulärt rutnät av block, kallade brickor där varje bricka kodas separat, oavsett andra brickor.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 filformat" >}}

## J2C-komprimering
JPEG 2000 använder wavelet-komprimeringsteknik vilket gör det snabbt baserat på det faktum att relativt få pixlar visas i vilken visningsport eller vilket fönster betraktaren än visar bilden. Detta kan understrykas av det faktum att endast ett fåtal megabyte pixlar visas på skärmen för mycket stora bilder (i gigabyte). Detta hjälper till att snabbt hämta och rendera endast den del av bilddata som krävs för att fylla visningspixlarna. Detta kräver också höghastighetsdekompressionsteknik för att påskynda bildhämtningsmekanismen för att skapa de bilder som krävs i farten.

J2C drar fördel av snabb dekompression och hämtar endast nödvändig information för pixeldata för att snabbt återge delar av synliga bilder till skärmarna. J2C är främst designad för visning av data och inte för att redigera den.

## J2C-identifikation
JPEG 2000-filer har signaturbytes `FF 4F FF 51`.

### Mimetyper
Registrerade Mime-typer för JPEG 2000-filer inkluderar:
* image/j2c
* bild/jpx
* bild/jpm
* video/mj2

## Förbättringar jämfört med JPEG-standarden
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

