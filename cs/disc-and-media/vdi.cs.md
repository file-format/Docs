{
  "date" : "2021-08-11",
  "keywords" :[ "soubor vdi", "formát souboru vdi", "co je soubor vdi", "soubor", "příklad vdi", "přípona souboru vdi", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů VDI a rozhraních API, která mohou vytvářet a otevírat soubory VDI.",
  "title" :"VDI - VirtualBox Virtual Disk Image File",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Co je soubor VDI?
Soubor s příponou .vdi je obraz virtuálního disku; specifické pro open source program virtualizace desktopů společnosti Oracle s názvem VirtualBox. Soubory VDI se používají ke spuštění virtuálního stroje VirtualBox. Virtuální počítače umožňují uživatelům spouštět další operační systémy nebo programy na jednom počítači. Výhodou souborů VDI je tedy to, že uživatelé mohou tyto obrazové soubory disku uložit na svůj pevný disk a mohou je spouštět pomocí emulátorů, kdykoli potřebují.

## Formát souboru VDI
Virtual Disk Image (VDI) je primární formát souboru disku pro aktivně vyvíjený open-source Oracle VM známý jako VirtualBox, což je virtualizační produkt podnikové třídy. Formát souboru VDI je navržen tak, aby vytvořil obraz přenosného disku, který lze snadno spustit pomocí jiných virtualizačních programů. Podporuje jak dynamicky alokované úložiště, tak úložiště s pevnou velikostí. Umožňuje rozbalit obrazový soubor poté, co byl vytvořen, i když již obsahuje data.

### Virtualizace disků
Systém emuluje pevné disky ve formátu obrazu disku VDI. Virtuální počítač VirtualBox může používat dřívější disky vytvořené v Microsoft Virtual PC nebo VMware, stejně jako svůj vlastní nativní formát. VirtualBox je také schopen připojovat se k cílům iSCSI a dělit na hostitele nezpracované oddíly, a to buď jako virtuální pevné disky. VirtualBox emuluje IDE (řadiče PIIX4 a ICH6), SATA (řadič ICH8M), řadiče SAS, ke kterým lze připojit pevné disky a SCSI.

Podpora je dostupná pro Open Virtualization Format (OVF) od verze 2.2.0 VirtualBoxu. Fyzická zařízení připojená k hostiteli i obrazy ISO lze připojit jako jednotky CD nebo DVD.
Ve výchozím nastavení VirtualBox podporuje grafiku prostřednictvím vlastní virtuální grafické karty kompatibilní s VESA.

### Podpora virtualizace pro Ethernet
VirtualBox virtualizuje následující karty síťového rozhraní pro síťový adaptér Ethernet:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Desktop (82540EM)
- Intel Pro/1000 MT Server (82545EM)
- Intel Pro/1000 T Server (82543GC)
- Paravirtualizovaný síťový adaptér (virtio-net)

Emulované síťové karty umožňují běh hostujícím OS bez nutnosti vyhledávat a instalovat ovladače pro síťový hardware, protože jsou dostupné jako součást hostujícího OS. Speciální paravirtualizovaný síťový adaptér zlepšuje výkon sítě tím, že snižuje potřebu přizpůsobit se specifickému hardwarovému rozhraní. Proto vyžaduje speciální podporu ovladače v hostovi.


## Reference

* [VirtualBox – z Wikipedie](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


