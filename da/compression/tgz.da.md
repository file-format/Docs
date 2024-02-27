{
  "date": "2022-03-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGZ-fil - Gzippet Tar-fil",
  "description": "Lær om TGZ filformat og API'er, der kan oprette og åbne TGZ filer.",
  "linktitle": "TGZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-daz"
}
},
  "lastmod": "2022-03-02"
}

## Hvad er TGZ fil?

En fil med filtypenavnet .tgz er en TAR-arkivfil, der består af flere filer og mapper, som er blevet komprimeret ved hjælp af Gnu Zip (gzip) komprimeringssoftwaren. En [TAR](/compression/tar/)-fil kombinerer normalt flere filer til en enkelt fil til sikkerhedskopiering eller distribution over internettet. Det er uncompress-fil, indtil den er komprimeret ved hjælp af gzip-softwaren, hvorefter den bliver til TGZ-filen. TGZ-filer, som er komprimerede filer, tager mindre plads på disken og kan nemt overføres via internettet via e-mail. Nogle programmer, der kan åbne TGZ-filer, inkluderer WinZip, Apple Archive Utility, 7-Zip og WinRAR. TGZ-filer bruges mest i UNIX- og Linux-systemer.

## TGZ filformat

TGZ-filer gemmes som komprimerede binære filer ved hjælp af [GZ](/compression/gz/)-komprimeringsalgoritmen.

## Sådan pakkes .tgz-filen ud på Linux

På Linux/Unix OS kan følgende kommando bruges til at udpakke TGZ-filer fra kommandolinjen.

```
tar zxvf tgzCompressedFile.tgz
```

Ovenstående kommando dekomprimerer den komprimerede TGZ-fil og udpakker dens filer fra TAR-arkivet til disk.
## Referencer ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)


