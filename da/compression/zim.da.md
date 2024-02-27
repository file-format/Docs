{
  "date": "2019-12-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIM-filformat - OpenZIM-arkivfil",
  "description": "Lær om ZIM-filformat og API'er, der kan oprette og åbne ZIM-filer.",
  "linktitle": "ZIM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-dam"
}
},
  "lastmod": "2019-12-09"
}

## Hvad er en ZIM fil? ##

Filer med filtypenavnet .zim er arkiver oprettet for at gemme Wiki-indhold offline. Det anses for at være det mest egnede åbne filformat til lagring af Wikipedia på en USB. Det gemmer webstedets indhold i et kompakt format. Dens navn kommer fra Zeno IMproved, som var det tidligere Zeno-filformat. ZIM vedligeholdes af [openZIM ](https://openzim.org/)projekt, som er sponsoreret af Wikimedia CH og støttet af Wikimedia Foundation. ZIM-filer kan åbnes af programmer som Kiwix og ZIMReader. OpenZIM-projektet har været vært for implementeringen af ZIM-filformatet på [Github](https://github.com/openzim) for bidrag fra OpenSource-fællesskabet.

## Specifikationer for ZIM-filformat

ZIM-filformatet blev udviklet oven på [Zeno file format](https://openzim.org/wiki/Zeno_file_format) og er ikke bagudkompatibelt. Formatspecifikationerne for ZIM-filformatet er [available online](https://openzim.org/wiki/ZIM_file_format) af openZIM til udviklerens reference. OpenZIM har leveret C++ open source-implementering, [LibZim](https://openzim.org/wiki/Zimlib), til læsning og skrivning af ZIM-filer.

ZIM-filformatet bruger LZMA2-komprimering til at gøre indholdet kompakt.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM filformat" >}}


### ZIM Header

A ZIM file starts with a header that is at offset 0. Alle bestanddelene er baseret på little-endian, og alle heltal er heltal uden fortegn, dvs. uint_16, uint_32, uint_64.

|Feltnavn |Type| Offset| Længde| Beskrivelse|
---|---|---|---|---|
|magisk nummer| heltal| 0| 4| Magisk tal for at genkende filformatet skal være 72173914 (0x44D495A)|
|majorVersion| heltal| 4| 2| Hovedversion af ZIM-filformatet (5 eller 6)|
|minorVersion| heltal| 6| 2| Mindre version af ZIM-filformatet|
|uuid| heltal| 8| 16| unik id for denne zim-fil|
|articleCount| heltal| 24| 4| samlet antal artikler|
|clusterCount| heltal| 28| 4| samlet antal klynger|
|urlPtrPos| heltal| 32| 8| placering af mappemarkørlisten sorteret efter URL|
|titlePtrPos| heltal| 40| 8| placering af mappemarkørlisten sorteret efter Titel|
|clusterPtrPos| heltal| 48| 8| placering af klyngemarkørlisten|
|mimeListPos| heltal| 56| 8| placering af MIME-typelisten (også overskriftstørrelse)|
|hovedside| heltal| 64| 4| hovedside eller 0xffffffff hvis ingen hovedside|
|layoutside| heltal| 68| 4| layoutside eller 0xffffffffff, hvis der ikke er nogen layoutside|
|checksumPos| heltal| 72| 8| markør til md5checksum af denne fil uden selve checksummen. Dette peger altid 16 bytes før slutningen af filen.|

## Referencer ##

* [OpenZIM](https://openzim.org/)

* [C++ LibZim](https://openzim.org/wiki/Zimlib)


