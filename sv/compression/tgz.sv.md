{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGZ-fil - Gzippad Tar-fil",
  "description":"Läs mer om TGZ-filformat och API:er som kan skapa och öppna TGZ-filer.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Vad är TGZ fil?

En fil med tillägget .tgz är en TAR-arkivfil, som består av flera filer och mappar, som har komprimerats med komprimeringsprogramvaran Gnu Zip (gzip). En [TAR](/sv/compression/tar/)-fil kombinerar vanligtvis flera filer till en enda fil för säkerhetskopiering eller distribution över internet. Det är en uncompress-fil tills den komprimeras med hjälp av gzip-mjukvaran, varefter den blir TGZ-filen. TGZ-filer, som är komprimerade filer, tar mindre utrymme på skivan och kan enkelt överföras via internet via e-post. Vissa program som kan öppna TGZ-filer inkluderar WinZip, Apple Archive Utility, 7-Zip och WinRAR. TGZ-filer används mest i UNIX- och Linux-system.

## TGZ filformat

TGZ-filer sparas som komprimerade binära filer med hjälp av [GZ](/sv/compression/gz/)-komprimeringsalgoritmen.

## Hur man packar upp .tgz-filen på Linux

På Linux/Unix OS kan följande kommando användas för att packa upp TGZ-filer från kommandoraden.

```
tar zxvf tgzCompressedFile.tgz
```

Ovanstående kommando dekomprimerar den komprimerade TGZ-filen och extraherar dess filer från TAR-arkivet till skiva.
## Referenser ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

