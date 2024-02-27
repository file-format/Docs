{
  "date": "2021-04-08",
  "keywords": [
"rpm fil",
"rpm filformat",
"hvad er en rpm fil",
"fil",
"rpm eksempel",
"rpm filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RPM - Red Hat Package Manager-fil",
  "description": "Lær om RPM-filformat og API'er, der kan oprette og åbne RPM-filer.",
  "linktitle": "RPM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-rp-dam"
}
},
  "lastmod": "2021-04-09"
}

## Hvad er en RPM fil?

En fil med filtypen .rpm er en Red Hat Linux-operativsystempakke til installationer af programmer på Linux-systemer. Red Hat Package Manager bruger RPM-filformatet og er et gratis og open source-pakkehåndteringssystem. Selvom RPM-filer kan bruges som de er til installation af programmer, kan disse konverteres til andre pakkeformater såsom [DEB](/compression/deb/) ved hjælp af Debian-programmet kaldet Alien.

## RPM filformat

En RPM-fil er en binær fil, der kan indeholde et sæt filer. De fleste gange er RPM-filer binære RPM'er, som er de kompilerede eksekverbare filer i softwaren. RPM-filen kan indeholde kilde-RPM'er (SRPM'er), der kan bruges til at bygge pakken ud fra kildekoden. RPM-filformatet består af fire sektioner.

 * Lead - Det identificerer filen som en RPM-fil
 * Signatur - Den kan bruges til at sikre integritet og/eller ægthed
 * Header - Indeholder metadata inklusive pakkenavn, version, arkitektur, filliste osv.
 * Filarkiv - Også kendt som nyttelast, som normalt er i cpio-format, komprimeret med [GZIP](/compression/gz/)

## Referencer

* [RPM - Wikipedia](https://rpm.org)

* [RPM-dokumentation](https://rpm.org/documentation.html)


