{
  "date" : "2021-08-11",
  "keywords" :[ "vdi-fil", "vdi-filformat", "vad är en vdi-fil", "fil", "vdi-exempel", "vdi-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om VDI-filformat och API:er som kan skapa och öppna VDI-filer.",
  "title" :"VDI - VirtualBox Virtual Disk Image File",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Vad är en VDI fil?
En fil med filtillägget .vdi är en virtuell diskavbildning; specifikt för Oracles open source-skrivbordsvirtualiseringsprogram som heter VirtualBox. VDI-filerna används för att starta den virtuella VirtualBox-maskinen. De virtuella datorerna tillåter användarna att köra ytterligare operativsystem eller program på en enda dator. Därför är fördelen med VDI-filer att användare kan spara dessa skivavbildningsfiler på sin hårddisk och kan köra dessa med emulatorer när de behöver.

## VDI-filformat
Virtual Disk Image (VDI) är det primära diskfilformatet för en aktivt utvecklad Oracle VM med öppen källkod känd som VirtualBox, som är en virtualiseringsprodukt i företagsklass. VDI-filformatet är utformat för att skapa en bärbar skivavbild som enkelt kan köras med andra virtualiseringsprogram. Den stöder både dynamiskt allokerad och fast storlek lagring. Det låter dig expandera en bildfil efter att den har skapats, även om den redan innehåller data.

### Skivvirtualisering
Systemet emulerar hårddiskar i VDI-diskavbildningsformat. En VirtualBox VM kan använda tidigare diskar skapade i Microsoft Virtual PC eller VMware, såväl som sitt eget inbyggda format. VirtualBox kan också ansluta till iSCSI-mål och råpartitionering på värden, antingen som virtuella hårddiskar. VirtualBox emulerar IDE (PIIX4- och ICH6-kontroller), SATA (ICH8M-kontroller), SAS-kontroller som hårddiskar kan anslutas till och SCSI.

Stödet är tillgängligt för Open Virtualization Format (OVF) sedan version 2.2.0 av VirtualBox. Både värdanslutna fysiska enheter och ISO-bilder kan monteras som CD- eller DVD-enheter.
Som standard stöder VirtualBox grafik via ett VESA-kompatibelt anpassat virtuellt grafikkort.

### Virtualiseringsstöd för Ethernet
VirtualBox virtualiserar följande nätverkskort för en Ethernet-nätverksadapter:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Desktop (82540EM)
- Intel Pro/1000 MT Server (82545EM)
- Intel Pro/1000 T Server (82543GC)
- Paravirtualiserad nätverksadapter (virtio-net)

De emulerade nätverkskorten gör att gästoperativsystem kan köras utan att behöva söka och installera drivrutiner för nätverkshårdvara eftersom de är tillgängliga som en del av gästoperativsystemet. En speciell paravirtualiserad nätverksadapter förbättrar nätverksprestandan genom att minska behovet av att matcha ett specifikt hårdvarugränssnitt. Därför kräver det särskilt förarstöd hos gästen.


## Referenser

* [VirtualBox - av Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


