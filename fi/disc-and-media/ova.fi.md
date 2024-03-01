{
  "date": "2021-08-10",
  "keywords": [
".ova-tiedosto",
"tiedosto muoto",
"mikä on .ova-tiedosto",
"tiedosto",
"tiedostopääte"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi .ova-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ova-tiedostoja.",
  "title": "OVA-tiedostomuoto - Avaa Virtual Appliance -tiedosto",
  "linktitle": "OVA",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ov-fia"
}
},
  "lastmod": "2022-01-03"
}

## Mikä on OVA-tiedosto?

OVA-tiedosto (Open Virtual Appliance) on OVF-hakemisto, joka on tallennettu arkistoksi käyttämällä .tar-arkistointimuotoa. Se on virtuaalinen laitepakettitiedosto, joka sisältää tiedostoja virtuaalikoneessa toimivien ohjelmistojen jakelua varten. OVA-paketti sisältää [.ovf](/disc-and-media/ovf/)-kuvaustiedoston, varmennetiedostot, valinnaisen [.mf](/programming/mf/)-tiedoston sekä muita aiheeseen liittyviä tiedostoja. OVA-tiedostojen mediatyyppi on application/ovf.

## OVA-tiedostomuoto

Kuten mainittiin, OVA-tiedosto on arkistotiedosto, joka luodaan käyttämällä OVF-hakemistoa TAR-tiedostomuodossa. Itse tiedosto tallennetaan binääritiedostona. Useimmat virtualisointiympäristöt, kuten VMware, Microsoft, Oracle ja Citrix, voivat asentaa virtuaalilaitteita OVF-tiedostosta, joka on kuvaustiedosto, jossa on virtuaalikoneeseen ladattavan kuvan tiedot.

## OVA-tiedoston edut

* OVA-tiedostot on pakattu, mikä mahdollistaa nopeamman latauksen.

* vSphere Client tarkistaa OVA-tiedoston ennen sen tuontia ja varmistaa, että se on yhteensopiva aiotun kohdepalvelimen kanssa. Jos laite ei ole yhteensopiva valitun isännän kanssa, sitä ei voi tuoda ja näyttöön tulee virheilmoitus.

* OVA voi kapseloida monitasoisia sovelluksia ja useamman kuin yhden virtuaalikoneen.


## Viitteet

* [OVA File Formats and Templates](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html)
* [OVF File Format Specifications](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

