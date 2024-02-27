{
  "date": "2021-04-08",
  "keywords": [
"deb-fil",
"deb filformat",
"hvad er en deb-fil",
"fil",
"deb eksempel",
"deb filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DEB - Bzip Compressed Tar Archive",
  "description": "Lær om DEB-filformat og API'er, der kan oprette og åbne DEB-filer.",
  "linktitle": "DEB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-de-dab"
}
},
  "lastmod": "2021-04-09"
}

## Hvad er DEB fil?

En fil med filtypenavnet .deb er et Debians binære pakkefilformat, der er tilgængeligt til distribution af softwarepakker på Linux OS. Den består af to [TAR](/compression/tar/) arkivfiler. DPKG'en giver mekanismen til at læse og installere DEB-pakkerne. DEB-pakker kan installeres ved hjælp af APT-pakkesoftwarestyringsgrænsefladen. DEB-filer har Internet Media Type som `application/vnd.debian.binary-package`.

## DEB filformat

En DEB-fil består af to [TAR](/compression/tar/) arkivfiler. Et arkiv indeholder kontroloplysningerne, og et andet indeholder de installerbare data.

### Pakkeorganisation

DEB-filen er en **ar**-arkivfil, der har en magisk værdi på `!<arch> `. Siden Debian 0.93 indeholder DEB-filernes arkiveringsmekanisme tre filer i en bestemt rækkefølge.

 1. `Debian Binary` - Det er bestemt til at have en række linjer, adskilt af nye linjer. På nuværende tidspunkt er der kun en enkelt linje, der beskriver versionsnummeret. Det aktuelle versionsnummer er 2.0.
 1. `Kontrolarkiv` - Det indeholder et control.tar-arkiv, der har vedligeholdelsesscripts og metainformation om pakken, såsom pakkenavn, version, afhængigheder og vedligeholder.
 1. `Data Archive` - Det er et tar-arkiv med navnet data.tar og indeholder de faktiske installerbare mediefiler. Arkivet kan komprimeres med gz, bz2, lzma eller xz, og dataarkivets filtype ændres tilsvarende.

### Kontrolarkiv

Kontrolarkivet kan indeholde indhold som følger.

 * `control` - It contains a brief description of the package as well as other information such as its dependencies.
 * `md5sums` - Den indeholder MD5 kontrolsummer af alle filer i pakken for at opdage korrupte eller ufuldstændige filer.
 * `conffiles` - Det viser filerne i pakken, der skal behandles som konfigurationsfiler. Konfigurationsfiler overskrives ikke under en opdatering, medmindre det er angivet.
 * `preinst`, postinst, prerm og postrm - Valgfri scripts, der udføres før eller efter installation eller fjernelse af pakken
 * `config` er et valgfrit script, der understøtter debconf-konfigurationsmekanismen.
 * `shlibs` - Det er en liste over delte biblioteksafhængigheder.

## Referencer

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))

* [Debian binært pakkeformat](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)


