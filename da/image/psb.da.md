{
  "date": "2019-10-11",
  "keywords": [
"psb fil",
"psb filformat",
"hvad er en psb-fil",
"fil",
"psb eksempel",
"psb filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSB - Photoshop Big Image File Format",
  "description": "Lær om PSB-filformat og API'er, der kan oprette og åbne PSB-filer.",
  "linktitle": "PSB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-dab"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en PSB fil?
Adobe Photoshop gemmer filer i to formater. Filer med en størrelse på 30.000 gange 30.000 pixels gemmes med PSD-udvidelse, og filer større end PSD op til 300.000 gange 300.000 pixels gemmes med PSB-udvidelse kendt som Photoshop Big. Mere specifikt kan PSB-filer være så store som 4 EB (over 4,2 milliarder GB) med billeder, der har en højde og bredde på op til 300.000 pixels. PSD'er kan på den anden side maksimalt være på op til 2 GB og billeddimensioner på 30.000 pixels.

PSB is also known as large format size for photoshop and supports all the photoshop features like layers, effects and filters.Photoshop can convert PSB file to [PSD](/image/psd/), [JPG](/image/jpeg/), [PNG](/image/png/), [EPS](/page-description-language/eps/), [GIF](/image/gif/) and other formats as well. Photoshop large document format is available once the feature of file handling pane of Photoshop’s preferences dialog box is enabled.

## Filformatoplysninger ##

Photoshop-filformatet er opdelt i fem store dele med mange længdemarkører til at flytte mellem sektioner.

|Filformat
---|
|Filhoved
|Farvetilstandsdata
| Billedressourcer
|Information om lag og maske
|(((
Billeddata
)))

### Filoverskrift ###

Filhovedet har en fast længde på 26 bytes og indeholder de grundlæggende egenskaber for billedet.

BYTE Signatur [4] – Er lig med '8BPS'.

WORD-version [2] – Versionsnummer, PSD # 1, PSB # 2.

BYTE Reserveret [6] – Reserveret og altid nul.

WORD-kanaler [2] – Antal farvekanaler i billedet inklusive alfakanaler. Dens værdi går fra 1 til 56.

LANGE rækker [4] – Billedets højde i pixels, PSD 1-30.000, PSB 1-300.000.

LANGE kolonner [4] – Billedets bredde i pixels, PSD 1-30.000, PSB 1-300.000.

WORD Depth [2] – Antal bits pr. kanal. Understøttede værdier er 1,8,16 og 32.

WORD Mode [2] – Farvetilstand for filen.

#### Tilstandsbeskrivelse ####


|Tilstand|Beskrivelse
---|---|
|0|Bitmap (monokrom)
|1|Gråskala
|2|Indekseret
|3|RGB
|4|CMYK
|7|Multikanal
|8|Duotone (halvtone)
|9|Lab

### Farvetilstandsdata ###

Efter filoverskriftssektionen følger farvetilstandsdatasektionen. Blokken starter med et LANG Tal, som angiver længden af blokken i bytes. Strukturen af farvetilstandsdataene er som følger:

4 bytes – Længden af følgende farvedata.

Variabel – Farvedata

Hvis tilstandsfeltværdien i overskriftssektionen ikke er indekseret farve eller duotone, vil længden af blokken være 0, og der vil ikke være nogen data efter længdefeltet.

For indekserede farvebilleder vil længden være 768 bytes, som vil indeholde en 256 farvepalet. For duotone vil data indeholde skærmparametre og andre relaterede oplysninger.

### Billedressourcer ###

Efter farvetilstandsdatasektionen er den tredje blok billedressourceafsnittet. De første fire bytes er et LANG tal, der angiver længden af blokken efterfulgt af en række ressourceblokke. Strukturen af billedressourceblokken er som følger:

BYTE Type [4] – Signatur '8BIM

WORD ID [2] – Billedressource-id. Der er en liste over ressource-id'er, som kan ses fra referencelinket.

BYTE-navn [Variabel] – Navn: Pascal-streng med lige længde. ** **

LANG Størrelse [4] – Faktisk størrelse af ressourcedata, der følger.

BYTE Data [Variable} – Ressourcedata. Den er polstret for at få den lige størrelse.

Nogle af ressourceformaterne er kort forklaret nedenfor:

**Gitter and Guides Ressource Format:** Grid and Guides-oplysninger gemmes i ressourceblokken. Disse ressourceblokke indeholder 16 byte gitter og guideheader efterfulgt af 5 byte blokke med guideinformation.

**Thumbnail-ressourceformat:** Miniatureoplysninger gemmes i billedressourceblok til forhåndsvisning, som består af 28 byte-header og JFIF-thumbnail i RGB.

**Farveeksemplere ressourceformat:** Farveprøvetagningsoplysninger gemmes i billedressourceblok med en 8 byte-header efterfulgt af en blok med variabel længde med farvesampleroplysninger.

### Lag- og maskeoplysninger ###

Den fjerde blok er lag- og maskeinformationsblok og indeholder information om lagene og maskerne. Laginformation gemmes først og derefter maskeinformation.

**Layer Information:** Layer information starter med en LONG værdi, som viser længden af laginformationen. Derefter er der WORD-værditælling, som viser antallet af lagposter, der skal følges.

[8] – længden af lagene

[2] – Antal lag

[Variabel] – Oplysninger om hvert lag.

[Variabel] – kanalbilleddata.** **

**Maskeoplysninger:** Maskestrukturen har følgende format:


|Datastruktur|Feltnavn| Beskrivelse
---|---|---|
|ORD| Overlay Farverum| (Ikke dokumenteret)
|BYTE[8]| Farvekomponenter| 4x2 byte farvekomponenter
|ORD| Opacitet| 0#gennemsigtig, 1#ugennemsigtig
|BYTE| Kind| 0#inverteret, 1#beskyttet, 128#brug lagret værdi
|BYTE| polstring| sat til nul

### Billeddata ###

Det sidste afsnit indeholder billedpixeldata. Billeddataene lagres som en serie af sekvenser i fly, dvs. først alle røde data, derefter alle grønne data osv. WORD i starten af hver linje viser størrelsen i bytes relateret til hver scanningslinje.

[2] – Kompressionsmetode:

[Variabel] – Billeddata i plan rækkefølge, dvs. RRRR, GGGG, BBBB osv.

Kompressionsmetoder:

0 – Raw Billeddata

1 – RLE komprimeret

2 – Zip uden forudsigelse

3 – Zip med forudsigelse

## Reference ##

* [PSB-filformat - af Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


