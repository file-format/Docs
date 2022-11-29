{
  "date" : "2021-04-08",
  "keywords" :[ "rpm-fil", "rpm-filformat", "vad är en rpm-fil", "fil", "rpm-exempel", "rpm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat Package Manager File",
  "description":"Läs mer om RPM-filformat och API:er som kan skapa och öppna RPM-filer.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Vad är RPM fil?

En fil med tillägget .rpm är ett Red Hat Linux-operativsystempaket för installationer av program på Linux-system. Red Hat Package Manager använder RPM-filformatet och är ett gratis pakethanteringssystem med öppen källkod. Även om RPM-filer kan användas som de är för installation av program, kan dessa konverteras till andra paketformat såsom [DEB](/sv/compression/deb/) med hjälp av Debian-programmet Alien.

## RPM filformat

En RPM-fil är en binär fil som kan innehålla en uppsättning filer. De flesta gånger är RPM-filer "binära RPM" som är de kompilerade körbara filerna för programvaran. RPM-filen kan innehålla käll-RPM (SRPM) som kan användas för att bygga paketet från källkoden. RPM-filformatet består av fyra sektioner.

* Lead - Den identifierar filen som en RPM-fil
* Signatur - Den kan användas för att säkerställa integritet och/eller autenticitet
* Header - Innehåller metadata inklusive paketnamn, version, arkitektur, fillista, etc.
* Filarkiv - Även känd som nyttolast, som vanligtvis är i cpio-format, komprimerad med [GZIP](/sv/compression/gz/)

## Referenser

* [RPM - Wikipedia](https://rpm.org)
* [RPM-dokumentation](https://rpm.org/documentation.html)

