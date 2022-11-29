{
  "date" : "2021-04-08",
  "keywords" :[ "deb-fil", "deb-filformat", "vad är en deb-fil", "fil", "deb-exempel", "deb-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip Compressed Tar Archive",
  "description":"Läs mer om DEB-filformat och API:er som kan skapa och öppna DEB-filer.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Vad är DEB fil?

En fil med filtillägget .deb är ett Debians binära paketfilformat tillgängligt för distribution av programvarupaket på Linux OS. Den består av två [TAR](/sv/compression/tar/) arkivfiler. DPKG tillhandahåller mekanismen för att läsa och installera DEB-paketen. DEB-paket kan installeras med hjälp av APT-pakethanteringsgränssnittet. DEB-filer har Internet Media Type som `application/vnd.debian.binary-package`.

## DEB filformat

En DEB-fil består av två [TAR](/sv/compression/tar/) arkivfiler. Ett arkiv innehåller kontrollinformationen och ett annat innehåller installerad data.

### Paketorganisation

DEB-filen är en **ar**-arkivfil som har ett magiskt värde på `!<arch> `. Sedan Debian 0.93 innehåller arkiveringsmekanismen för DEB-filer tre filer i en specifik ordning.

1. `Debian Binary` - Det är avsett att ha en serie rader, åtskilda av nya rader. För närvarande finns endast en rad som beskriver versionsnumret. Det nuvarande versionsnumret är 2.0.
1. `Kontrollarkiv` - Det innehåller ett control.tar-arkiv som har underhållarskript och metainformation om paketet såsom paketnamn, version, beroenden och underhållare.
1. `Dataarkiv` - Det är ett tar-arkiv som heter data.tar och innehåller de faktiska installationsbara mediefilerna. Arkivet kan komprimeras med gz, bz2, lzma eller xz, och filtillägget för dataarkivet ändras därefter.

### Kontrollarkiv

Kontrollarkivet kan innehålla innehåll enligt följande.

* `kontroll` - Den innehåller en kort beskrivning av paketet samt annan information som dess beroenden.
* `md5sums` - Den innehåller MD5-kontrollsummor för alla filer i paketet för att upptäcka korrupta eller ofullständiga filer.
* `conffiles` - Den listar filerna i paketet som ska behandlas som konfigurationsfiler. Konfigurationsfiler skrivs inte över under en uppdatering om inget annat anges.
* `preinst`, postinst, prerm och postrm - Valfria skript som körs före eller efter installation eller borttagning av paketet
* `config` är ett valfritt skript som stöder debconf-konfigurationsmekanismen.
* `shlibs` - Det är en lista över delade biblioteksberoenden.

## Referenser

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Debians binära paketformat](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

