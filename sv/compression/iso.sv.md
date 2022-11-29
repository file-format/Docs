{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Disk Image File Format",
  "description":"Vad är en ISO-fil och API:er som kan skapa och öppna ISO-filer.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Vad är en ISO-fil?

En fil med filtillägget .iso är en okomprimerad arkivskivbildsfil som representerar innehållet i hela data på en optisk skiva som CD eller DVD. Baserat på standarden [ISO-9660](https://www.iso.org/standard/17505.html), innehåller ISO-bildfilformatet skivdata tillsammans med filsysteminformationen som är lagrad i den. Förmågan hos ISO-filer att innehålla en exakt kopia av innehållet gör den till den perfekta filtypen för att skapa kopior av CD-/DVD-skivor och används mest för att lagra startbar data för installation. Oftast bränns ISO-filer till USB/CD/DVD som startbart innehåll för att starta upp maskinen för installation. ISO-filer har MIME-typ application/x-iso9660-image.

## ISO filformat

ISO-filformat är inte som andra containerfilformat även om det arkiverar det angivna innehållet i data. Arkivet skapas som en binär fil med den exakta strukturen för innehållet och filsysteminformation. ISO-filformatet beskrivs av [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) enligt följande.

### Toppnivåstruktur för ISO-fil

Den övergripande strukturen för filen består av:

* `System Area` - 32 768 byte och används inte av ISO_9660
* `Dataområde` - består av volymdeskriptoruppsättning och sökvägstabeller, kataloger och filer

### Volume Descriptor Set

Dataområdet börjar med volymdeskriptoruppsättningen, en uppsättning av en eller flera volymdeskriptorer som avslutas med en volymdeskriptoruppsättningsterminator. Dessa fungerar tillsammans som en rubrik för dataområdet, som beskriver dess innehåll (liknande BIOS-parameterblocket som används av FAT-, HPFS- och NTFS-formaterade diskar).

En volymbeskrivningsuppsättning är som visas nedan.

|Volym Descriptor Set|
---|
|Volymbeskrivning #1|
|...|
|Volymbeskrivning #N|
|Volymdeskriptoruppsättningsterminator|

#### Volymbeskrivning

Varje volymdeskriptor är 2048 byte stor och har följande struktur:

|Del |Typ |Identifierare |Version |Data|
---|---|---|---|---|
|Storlek |1 byte |5 byte (alltid 'CD001') |1 byte (alltid 0x01) |2 041 byte|

## Referenser

* [Optical Disk Image - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Filsignaturer](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

