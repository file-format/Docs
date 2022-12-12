{
  "date" : "2021-08-10",
  "keywords" :[ ".ova fájl", "fájlformátum", "mi az .ova fájl", "fájl", "fájl kiterjesztése"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ az .ova fájlformátumról és az API-król, amelyek ova fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"OVA fájlformátum - virtuális készülékfájl megnyitása",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Mi az az OVA fájl?

Az OVA (Open Virtual Appliance) fájl egy OVF-könyvtár, amelyet archívumként mentenek el .tar archiválási formátumban. Ez egy virtuális készülékcsomagfájl, amely a virtuális gépen futó szoftverek terjesztéséhez szükséges fájlokat tartalmazza. Az OVA-csomag tartalmaz egy [.ovf](/hu/disc-and-media/ovf/) leíró fájlt, tanúsítványfájlokat, egy opcionális [.mf](/hu/programming/mf/) fájlt, valamint más kapcsolódó fájlokat. Az OVA-fájlok médiatípusa: application/ovf.

## OVA fájl formátum

Mint említettük, az OVA-fájl egy archív fájl, amely az OVF-könyvtár használatával jön létre TAR-fájlformátumban. Maga a fájl bináris fájlként kerül mentésre. A legtöbb virtualizációs platform, például a VMware, a Microsoft, az Oracle és a Citrix, telepíthet virtuális készülékeket egy OVF-fájlból, amely egy leíró fájl, amely a virtuális gépbe betöltendő kép részleteit tartalmazza.

## Az OVA fájl előnyei

* Az OVA-fájlok tömörítettek, ami gyorsabb letöltést tesz lehetővé.
* A vSphere Client ellenőrzi az OVA-fájlt az importálás előtt, és biztosítja, hogy az kompatibilis a tervezett célkiszolgálóval. Ha a készülék nem kompatibilis a kiválasztott gazdagéppel, akkor nem importálható, és hibaüzenet jelenik meg.
* Az OVA többszintű alkalmazásokat és egynél több virtuális gépet is magában foglalhat.

## Hivatkozások

* [OVA fájlformátumok és -sablonok](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [OVF fájlformátum specifikációi](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

