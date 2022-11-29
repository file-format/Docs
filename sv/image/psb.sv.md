{
  "date" : "2019-10-11",
  "keywords" :[ "psb-fil", "psb-filformat", "vad är en psb-fil", "fil", "psb-exempel", "psb-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Photoshop Big Image File Format",
  "description":"Läs mer om PSB-filformat och API:er som kan skapa och öppna PSB-filer.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är PSB fil?
Adobe Photoshop sparar filer i två format. Filer med 30 000 x 30 000 pixlar i storlek sparas med PSD-tillägget och filer större än PSD upp till 300 000 x 300 000 pixlar sparas med PSB-tillägget som kallas "Photoshop Big". Mer specifikt kan PSB-filer vara så stora som 4 EB (över 4,2 miljarder GB) med bilder som har en höjd och bredd på upp till 300 000 pixlar. PSD:er, å andra sidan, kan vara på maximalt upp till 2 GB och bilddimensioner på 30 000 pixlar.

PSB är också känd som storformatsstorlek för photoshop och stöder alla Photoshop-funktioner som lager, effekter och filter. Photoshop kan konvertera PSB-filer till [PSD](/sv/image/psd/), [JPG](/sv/image/jpeg/) , [PNG](/sv/image/png/), [EPS](/sv/page-description-language/eps/), [GIF](/sv/image/gif/) och andra format också. Photoshop stora dokumentformat är tillgängligt när funktionen i filhanteringsrutan i Photoshops inställningsdialogruta är aktiverad.,

## Filformatinformation ##

Photoshop-filformatet är uppdelat i fem huvuddelar med många längdmarkörer för att flytta mellan avsnitten.

|Filformat
---|
|Filhuvud
|Färglägesdata
| Bildresurser
|Lager och maskinformation
|(((
Bilddata
)))

### Filhuvud ###

Filhuvudet har en fast längd på 26 byte och innehåller bildens grundläggande egenskaper.

BYTE-signatur [4] – är lika med '8BPS'.

WORD Version [2] – Versionsnummer, PSD # 1, PSB # 2.

BYTE Reserved [6] – Reserverad och alltid noll.

WORD-kanaler [2] – Antal färgkanaler i bilden inklusive alfakanaler. Dess värde sträcker sig från 1 till 56.

LÅGA rader [4] – Bildens höjd i pixlar, PSD 1-30 000, PSB 1-300 000.

LÅNG Kolumner [4] – Bildens bredd i pixlar, PSD 1-30 000, PSB 1-300 000.

ORDdjup [2] – Antal bitar per kanal. Värden som stöds är 1,8,16 och 32.

WORD-läge [2] – Färgläge för filen.

#### Lägesbeskrivning ####


|Läge|Beskrivning
---|---|
|0|Bitmapp (monokrom)
|1|Gråskala
|2|Indexerad
|3|RGB
|4|CMYK
|7|Multikanal
|8|Duotone (halvton)
|9|Labb

### Färglägesdata ###

Efter filrubriken följer avsnittet för färglägesdata. Blocket börjar med ett LÅNGT nummer som anger blockets längd i byte. Strukturen för färglägesdata är som följer:

4 byte – Längden på följande färgdata.

Variabel – Färgdata

Om lägesfältvärdet i rubriksektionen inte är Indexerad färg eller duoton, kommer blockets längd att vara 0 och det kommer inga data efter längdfältet.

För indexerade färgbilder kommer längden att vara 768 byte som kommer att innehålla en 256 färgpalett. För duotone kommer data att innehålla skärmparametrar och annan relaterad information.

### Bildresurser ###

Efter färglägesdatasektionen är det tredje blocket bildresurssektionen. De första fyra byten är ett LÅNGT nummer som anger längden på blocket följt av en serie resursblock. Strukturen för bildresursblocket är som följer:

BYTE Type [4] – Signatur '8BIM'

WORD ID [2] – Bildresurs-ID. Det finns en lista över resurs-ID:n som kan ses från referenslänken.

BYTE Namn [Variabel] – Namn: Pascal String med jämn längd. ** **

LONG Size [4] – Verklig storlek på resursdata som följer.

BYTE-data [Variabel} – Resursdata. Den är vadderad för att göra den jämna storleken.

Några av resursformaten förklaras kort nedan:

**Grid and Guides Resurs Format:** Grid and Guides information lagras i resursblock. Dessa resursblock innehåller 16 byte rutnät och guiderubrik följt av 5 byte block med guideinformation.

**Miniatyrresursformat:** Miniatyrbildsinformation lagras i bildresursblocket för förhandsvisning som består av 28 byte-huvud och JFIF-miniatyr i RGB.

**Färgsamplingsresursformat:** Färgsamplingsinformation lagras i bildresursblock med en 8 byte-rubrik följt av ett block med variabel längd med information om färgsamplare.

### Lager- och maskinformation ###

Det fjärde blocket är lager- och maskinformationsblock och innehåller information om lagren och maskerna. Lagerinformation lagras först och sedan maskeras information.

**Lagerinformation:** Lagerinformation börjar med ett LONG-värde som visar längden på lagerinformationen. Efter det finns WORD-värderäkning som visar antalet lagerposter som ska följas.

[8] – längden på lagren

[2] – Antal lager

[Variabel] – Information om varje lager.

[Variabel] – kanalbilddata.** **

**Maskinformation:** Maskstrukturen har följande format:


|Datastruktur|Fältnamn| Beskrivning
---|---|---|
|ORD| Överlägg färgrymd| (Ej dokumenterat)
|BYTE[8]| Färgkomponenter| 4x2 byte färgkomponenter
|ORD| Opacitet| 0#transparent, 1#ogenomskinlig
|BYTE| Snäll| 0#inverterad, 1#skyddad, 128#använd lagrat värde
|BYTE| stoppning| inställd på noll

### Bilddata ###

Det sista avsnittet innehåller bildpixeldata. Bilddata lagras som en serie av sekvenser i plan, dvs först alla röda data, sedan alla gröna data etc. WORD i början av varje rad visar storleken i byte relaterad till varje skanningslinje.

[2] – Komprimeringsmetod:

[Variabel] – Bilddata i plan ordning dvs RRRR, GGGG, BBBB etc.

Komprimeringsmetoder:

0 – Raw Bilddata

1 – RLE komprimerad

2 – Zip utan förutsägelse

3 – Zip med förutsägelse

## Referens ##

* [PSB-filformat - av Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

