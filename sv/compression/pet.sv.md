{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PET-filformat - Puppy Linux Install Package File",
  "description":"Läs mer om PET-filformat och API:er som kan skapa och öppna PET-filer.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Vad är en Linux PET-fil?

En PET-fil är en applikationsinstallationspaketfil som skapats och används med PuppyLinux-varianten av operativsystemet Linux. Den skapas som en komprimerad [TGZ](/sv/compression/tgz/)-fil som minskar filstorleken på det komprimerade arkivet. Integriteten för PET-filformatet säkerställs av md5sum-kontrollsumman som läggs till i slutet av filen för verifiering i fjärränden. PET-filer kan extraheras med standardfilextraktorn TGZ och WinRAR. PET-filer ersatte de gamla installationsfilerna för [PUP](/sv/compression/pup/)-paketet.

## PET filformat

PET-filer sparas på skiva som komprimerade arkiv i binärt filformat. De interna filformatsdetaljerna för PET-filformatet är dock inte kända. I likhet med installationsfilerna för [.exe](/sv/executable/exe/) och [.msi](/sv/executable/msi/)-paketet startar PET-filerna en installation när de körs.

## Referenser

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Index över PuppyLinux PET-paket](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

