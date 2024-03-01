{
  "date": "2021-08-11",
  "keywords": [
"vdi tiedosto",
"vdi-tiedostomuoto",
"mikä on vdi-tiedosto",
"tiedosto",
"vdi esimerkki",
"vdi tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi VDI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VDI-tiedostoja.",
  "title": "VDI - VirtualBox Virtual Disk Image File",
  "linktitle": "VDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vd-fii"
}
},
  "lastmod": "2021-08-11"
}

## Mikä on VDI-tiedosto?
Tiedosto, jonka pääte on .vdi, on näennäislevykuva; Oraclen avoimen lähdekoodin työpöydän virtualisointiohjelma nimeltä VirtualBox. VDI-tiedostoja käytetään VirtualBox-virtuaalikoneen käynnistämiseen. Virtuaalikoneiden avulla käyttäjät voivat suorittaa muita käyttöjärjestelmiä tai ohjelmia yhdessä tietokoneessa. Tästä syystä VDI-tiedostojen etu on, että käyttäjät voivat tallentaa nämä levykuvatiedostot kiintolevylleen ja käyttää niitä emulaattoreilla aina kun he tarvitsevat.

## VDI-tiedostomuoto
Virtual Disk Image (VDI) on ensisijainen levytiedostomuoto aktiivisesti kehitetylle avoimen lähdekoodin Oracle VM:lle, joka tunnetaan nimellä VirtualBox, joka on yritysluokan virtualisointituote. VDI-tiedostomuoto on suunniteltu tekemään kannettava levykuva, jota voidaan helposti käyttää muilla virtualisointiohjelmilla. Se tukee sekä dynaamisesti allokoitua että kiinteän kokoista tallennustilaa. Sen avulla voit laajentaa kuvatiedostoa sen luomisen jälkeen, vaikka se sisältäisi jo tietoja.

### Levyn virtualisointi
Järjestelmä emuloi kiintolevyjä VDI-levykuvamuodossa. VirtualBox VM voi käyttää aiempia levyjä, jotka on luotu Microsoft Virtual PC:llä tai VMwarella, sekä omaa alkuperäistä muotoaan. VirtualBox pystyy myös muodostamaan yhteyden iSCSI-kohteisiin ja muodostamaan raakaosion isännässä joko virtuaalisina kiintolevyinä. VirtualBox emuloi IDE:tä (PIIX4- ja ICH6-ohjaimet), SATA-ohjainta (ICH8M-ohjain), SAS-ohjaimia, joihin voidaan liittää kiintolevyjä, ja SCSI:tä.

Tuki on saatavilla Open Virtualization Formatille (OVF) VirtualBoxin versiosta 2.2.0 lähtien. Sekä isäntään kytketyt fyysiset laitteet että ISO-otokset voidaan asentaa CD- tai DVD-asemiksi.
Oletuksena VirtualBox tukee grafiikkaa VESA-yhteensopivan mukautetun virtuaalisen näytönohjaimen kautta.

### Virtualisointituki Ethernetille
VirtualBox virtualisoi seuraavat verkkoliitäntäkortit Ethernet-verkkosovittimelle:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Desktop (82540EM)
- Intel Pro/1000 MT Server (82545EM)
- Intel Pro/1000 T -palvelin (82543GC)
- Paravirtualisoitu verkkosovitin (virtio-net)

Emuloidut verkkokortit mahdollistavat vieraskäyttöjärjestelmien käytön ilman, että verkkolaitteiston ohjaimia tarvitsee etsiä ja asentaa, koska ne ovat saatavilla osana vieraskäyttöjärjestelmää. Erityinen paravirtualisoitu verkkosovitin parantaa verkon suorituskykyä vähentämällä tarvetta sovittaa tiettyyn laitteistoliitäntään. Siksi se vaatii erityistä kuljettajatukea vieraalta.


## Viitteet 

* [VirtualBox - Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)



