{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDMP-tiedosto - Windows Heap Dump -tiedostomuoto",
  "description": "Opi HDMP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata HDMP-tiedostoja.",
  "linktitle": "HDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-hdm-fip"
}
},
  "lastmod": "2022-08-19"
}

## Mikä on HDMP-tiedosto?

HDMP-tiedosto on pakkaamaton muistivedos, kun sovellus tai ohjelma kaatuu virheen vuoksi. Sen on luonut vain Windows XP/Vista, ja se sisältää vedoksen sovelluksen tilasta, kun se kaatui. Pakkaamattomina HDMP-tiedostot vievät enemmän tilaa levyllä verrattuna Minidump [MDMP](/system/mdmp/) -tiedostoihin, jotka on pakattu raportointia varten.

Sovelluksia, joita voidaan käyttää HDMP-tiedostojen **avaukseen** tai analysointiin, ovat Microsoft Visual Studio ja Windowsin virheenkorjaustyökalut.

## HDMP-tiedostomuoto

HDMP-tiedostot tallennetaan levylle binääritiedostoina, eikä niistä ole mitään hyötyä, jos ne avataan ilman asianmukaisia sovelluksia. Ne sisältävät asiaankuuluvat järjestelmätiedot, jotka on tallennettu virheen tapahtuessa.

### Ero HDMP- ja MDMP-tiedostomuotojen välillä

HDMP ovat pakkaamattomia muistivedostiedostoja. Sitä vastoin MDMP ovat minivedostiedostoja, jotka pakataan tiedostokoon pienentämiseksi ja lähetetään Microsoftille ongelman ilmoittamista varten.

## Viite ##

* [DMP – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


