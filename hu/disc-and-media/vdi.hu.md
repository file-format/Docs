{
  "date" : "2021-08-11",
  "keywords" :[ "vdi fájl", "vdi fájl formátum", "mi az a vdi fájl", "fájl", "vdi példa", "vdi fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ a VDI-fájlformátumról és az API-król, amelyek VDI-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"VDI - VirtualBox Virtual Disk Image File",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Mi az a VDI fájl?
A .vdi kiterjesztésű fájl egy virtuális lemezkép; kifejezetten az Oracle VirtualBox nevű, nyílt forráskódú asztali virtualizációs programjára vonatkozik. A VDI-fájlok a VirtualBox virtuális gép elindítására szolgálnak. A virtuális gépek lehetővé teszik a felhasználók számára további operációs rendszerek vagy programok futtatását egyetlen számítógépen. Ezért a VDI-fájlok előnye, hogy a felhasználók ezeket a lemezképfájlokat a merevlemezükre menthetik, és emulátorokkal futtathatják, amikor csak szükségük van rá.

## VDI fájlformátum
A Virtual Disk Image (VDI) az aktív fejlesztésű, nyílt forráskódú Oracle virtuális gép, a VirtualBox néven ismert elsődleges lemezfájl-formátuma, amely egy vállalati szintű virtualizációs termék. A VDI fájlformátumot úgy tervezték, hogy hordozható lemezképet készítsen, amely könnyen futtatható más virtualizációs programokkal. Támogatja mind a dinamikusan elosztott, mind a rögzített méretű tárolást. Lehetővé teszi a képfájl kibontását a létrehozás után, még akkor is, ha az már tartalmaz adatokat.

### Lemezvirtualizáció
A rendszer VDI lemezkép formátumban emulálja a merevlemezeket. A VirtualBox virtuális gépek használhatják a Microsoft Virtual PC-ben vagy VMware-ben létrehozott korábbi lemezeket, valamint saját natív formátumát. A VirtualBox képes csatlakozni iSCSI-célokhoz és nyers particionálásra a gazdagépen, akár virtuális merevlemezként is. A VirtualBox emulálja az IDE-t (PIIX4 és ICH6 vezérlők), a SATA-t (ICH8M vezérlő), a SAS vezérlőket, amelyekhez merevlemezek csatlakoztathatók, és az SCSI-t.

A támogatás a VirtualBox 2.2.0-s verziója óta elérhető az Open Virtualization Format (OVF) számára. Mind a gazdagéphez csatlakoztatott fizikai eszközök, mind az ISO lemezképek csatlakoztathatók CD- vagy DVD-meghajtóként.
A VirtualBox alapértelmezés szerint VESA-kompatibilis egyéni virtuális grafikus kártyán keresztül támogatja a grafikát.

### Virtualizációs támogatás az Ethernet számára
A VirtualBox a következő hálózati csatolókártyákat virtualizálja Ethernet hálózati adapterhez:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT asztali számítógép (82540EM)
- Intel Pro/1000 MT szerver (82545EM)
- Intel Pro/1000 T szerver (82543GC)
- Paravirtualizált hálózati adapter (virtio-net)

Az emulált hálózati kártyák lehetővé teszik a vendég operációs rendszerek futtatását anélkül, hogy meg kellene keresni és telepíteni kellene a hálózati hardverhez illesztőprogramokat, mivel ezek a vendég operációs rendszer részeként állnak rendelkezésre. Egy speciális paravirtualizált hálózati adapter javítja a hálózati teljesítményt azáltal, hogy csökkenti az adott hardver interfészhez való illeszkedés szükségességét. Ezért speciális illesztőprogram-támogatást igényel a vendégben.


## Hivatkozások

* [VirtualBox – Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


