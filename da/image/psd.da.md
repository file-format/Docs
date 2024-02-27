{
  "date": "2019-10-11",
  "keywords": [
"psd fil",
"psd filformat",
"hvad er en psd-fil",
"fil",
"psd eksempel",
"psd filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSD - Photoshop billedfilformat",
  "description": "Lær om PSD-filformat og API'er, der kan oprette og åbne PSD-filer.",
  "linktitle": "PSD",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-dad"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en PSD fil?

PSD, Photoshop Document, repræsenterer Adobe Photoshops oprindelige filformat, der bruges til grafisk design og udvikling. PSD-filer kan omfatte billedlag, justeringslag, lagmasker, annoteringer, filoplysninger, nøgleord og andre Photoshop-specifikke elementer. Photoshop-filer har standardudvidelsen som .PSD og har en maksimal højde og bredde på 30.000 pixels og en længdegrænse på to gigabyte.

## PSD-filformatspecifikationer ##

Data i en PSD-fil gemmes i big endian byte-rækkefølge. Dette indebærer udskiftning af de korte og lange heltal, når du læser eller skriver på Windows-platformen. Photoshop-filformatet er opdelt i fem hoveddele. Den har mange længdemarkører, der kan bruges til at flytte fra den ene sektion til den næste. Længdemarkørerne er normalt polstret med bytes for at afrunde til nærmeste 2 eller 4 byte interval. De fem hoveddele er:

* Filoverskrift

* Farvetilstandsdata

* Billedressourcer

* Information om lag og maske

* Billeddata


Af hensyn til overensstemmelsen bør data skrives til alle disse felter i sektionen, da Photoshop kan forsøge at læse hele sektionen. Det indebærer også, at der skrives nuller til overspringede felter, mens der skrives til en fil. Længdefeltet i de længdeafgrænsede sektioner skal bruges til at beslutte, hvornår læsningen skal stoppes. I de fleste tilfælde angiver længdefeltet antallet af bytes, ikke poster, der følger. Følgende punkter skal huskes, mens du læser en fil.

* Værdierne i kolonnen "Længde" i alle tabeller er i bytes.

* Alle værdier defineret som Unicode-streng består af:

* Et felt med en længde på 4 bytes, der repræsenterer antallet af tegn i strengen (ikke bytes).

* Strengen af Unicode-værdier, to bytes pr. tegn.


### Filoverskrift ###

Filhovedet indeholder de grundlæggende egenskaber for billedet.

|Længde|Beskrivelse
---|---|
|4|Signatur: altid lig med '8BPS' . Forsøg ikke at læse filen, hvis signaturen ikke matcher denne værdi.
|2|Version: always equal to 1. Forsøg ikke at læse filen, hvis versionen ikke matcher denne værdi. (~*~*PSB~*~* version er 2.)
|6|Reserveret: skal være nul.
|2|Antallet af kanaler i billedet, inklusive eventuelle alfakanaler. Understøttet område er 1 til 56.
|4|Billedets højde i pixels. Understøttet område er 1 til 30.000.
|4|Billedets bredde i pixels. Understøttet område er 1 til 30.000.
|2|Dybde: antallet af bits pr. kanal. Understøttede værdier er 1, 8, 16 og 32.
|2|Filens farvetilstand. Understøttede værdier er: Bitmap # 0; Gråtoner # 1; Indekseret # 2; RGB # 3; CMYK # 4; Multikanal # 7; Duotone # 8; Lab #9.

### Farvetilstand Data Sektion ###

Farvetilstandsdatasektionen er struktureret som følger:


|Længde|Beskrivelse
---|---|
|4|Længden af følgende farvedata
|variabel|Farvedataene

Farvetilstandsdata er kun tilgængelige for indekserede farver og duotone som defineret af tilstandsfeltet i afsnittet Filoverskrift. For alle andre tilstande er denne sektion repræsenteret af 4-byte nulstillede værdier. For indekserede farvebilleder er længden 768, og farvedataene indeholder farvetabellen for billedet i ikke-sammenflettet rækkefølge. For Duotone-billeder indeholder farvedata duotone-specifikationen (hvis formatet ikke er dokumenteret). Andre programmer, der læser Photoshop-filer, kan behandle et duotone-billede som et gråt billede og blot bevare indholdet af duotone-informationen, når du læser og skriver filen.

### Billedressourcesektion ###

Den tredje sektion af filen indeholder billedressourcer. Det starter med et længdefelt efterfulgt af en række ressourceblokke.


|Længde|Beskrivelse
---|---|
|4|Længde af billedressourceafsnit. Længden kan være nul.
|Variabel|Billedressourcer (Billedressourceblokke)

Billedressourcer bruges til at gemme ikke-pixeldata, der er forbundet med billeder, såsom stier til penneværktøjer. De omtales som ressourceblokke, fordi de indeholder data, der blev gemt i Macintosh'ens ressource i tidlige versioner af Photoshop. Den grundlæggende struktur af billedressourceblokke er som vist nedenfor:


|Længde|Beskrivelse
---|---|
|4|Signatur: '8BIM
|2|Unik identifikator for ressourcen. Billedressource-id'er indeholder en liste over ressource-id'er, der bruges af Photoshop.
|Variabel|Navn: Pascal-streng, polstret for at gøre størrelsen lige (et null-navn består af to bytes på 0)
|4|Faktisk størrelse af ressourcedata, der følger
|Variabel|Ressourcedataene, beskrevet i afsnittene om de enkelte ressourcetyper. Den er polstret for at gøre størrelsen ens.

Billedressourcer bruger flere standard-id-numre.

### Lag- og maskeoplysninger ###

Den fjerde sektion af en Photoshop-fil indeholder oplysninger om lag og masker såsom antal lag, kanaler i lagene, blandingsområder, justeringslagstaster, effektlag og maskeparametre. Hvis der ikke er nogen lag eller masker, er denne sektion repræsenteret af nulstillet 4-byte felt. Der skal lægges særlig vægt på længden af afsnit, mens du læser dette afsnit på grund af de nulstillede værdier. Arrangementet af Layer and Mask sektionen er som følger:


|Længde|Beskrivelse
---|---|
|4|Længde af lag- og maskeinformationssektionen. (PSB-længde er 8 bytes.)
|Variabel|Laag info
|Variabel|Global lagmaskeinfo
|Variabel|Serie af taggede blokke, der indeholder forskellige typer data.

#### Laginfo ####

Følgende tabel viser organiseringen af laginformationen på højt niveau.


|Længde|Beskrivelse
---|---|
|4|Length of the layers info section, rounded up to a multiple of 2. (PSB-længde er 8 bytes.)
|2|Antal lag. Hvis det er et negativt tal, er dets absolutte værdi antallet af lag, og den første alfakanal indeholder gennemsigtighedsdataene for det flettede resultat.
|Variabel|Oplysninger om hvert lag. Se Lagposter beskriver strukturen af disse oplysninger for hvert lag.
|Variabel|Kanalbilleddata. Indeholder en eller flere billeddataposter for hvert lag. Lagene er i samme rækkefølge som i laginformationen

### Billeddata ###

Billedpixeldataene er indeholdt i billeddataafsnittet i filen. Arrangement af data i billeddatasektionen er i plan rækkefølge, dvs. først alle de røde data, derefter alle de grønne data osv. Hvert plan er lagret i scan-line rækkefølge, uden pad bytes. Billeddatasektionen er arrangeret i et format som vist i følgende tabel.

|Længde|Beskrivelse
---|---|
|2|Compression method: *0 = Raw image data * 1 = RLE komprimeret billeddataene starter med bytetællingerne for alle scanningslinjerne (rækker * kanaler), med hver optælling gemt som en to-byte værdi. De RLE-komprimerede data følger, med hver scanningslinje komprimeret separat. RLE-komprimeringen er den samme kompressionsalgoritme, der bruges af Macintosh ROM-rutinen PackBits og TIFF-standarden. *2 = ZIP uden forudsigelse *3 = ZIP med forudsigelse.
|Variabel|Billeddataene. Planar orden = RRR GGG BBB osv.

## Referencer ##

* [PSD-filformatspecifikationer - af Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)

* [Adobe Photoshop-filformat](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


