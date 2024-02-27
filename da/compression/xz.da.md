{
  "date": "2022-01-23",
  "keywords": [
"xz filen",
"filformat",
"hvad er en xz-fil",
"fil",
"xz eksempel",
"xz filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XZ-fil - XZ-komprimeret arkiv",
  "description": "Lær om XZ-filformat og API'er, der kan oprette og åbne XZ-filer.",
  "linktitle": "XZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-x-daz"
}
},
  "lastmod": "2022-01-23"
}

## Hvad er en XZ fil?

XZ er et komprimeret filformat, der bruger LZMA2-komprimeringsalgoritmen. Det blev designet som en erstatning for de populære gzip- og bzip2-formater og tilbyder en række fordele i forhold til disse ældre standarder. XZ-filer er godt understøttet på tværs af mange platforme og kan dekomprimeres hurtigt og nemt. Selvom de ikke er så almindelige som [ZIP](/compression/zip/)- eller [RAR](/compression/rar/)-filer, kan XZ-arkiver bruges til at gemme store mængder data uden at ofre komprimeringskvaliteten. Hvis du har brug for at komprimere eller dekomprimere store filer, er XZ filtypenavnet værd at overveje.

## XZ filformat

XZ-fil genereres og gemmes som binære filer på disk. Den bruger LZMA-algoritmen til at komprimere data og kan opnå et komprimeringsforhold på op til 50 %. XZ-filer bruges typisk til softwaredistributioner og backup-arkiver. De kan dekomprimeres ved hjælp af XZ-værktøjet, som er inkluderet i de fleste Linux-distributioner.

## Udpak XZ-filer på Linux/Unix

For at udpakke XZ-filer skal du først installere `xz-utils`-pakken:
```
$ sudo apt-get install xz-utils
```

Brug kommandoen `unxz` til at udpakke .xz-filer:
```
$ unxz compressed_xz_file.xz
```

eller bruge med --decompress mulighed for XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Referencer

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)


