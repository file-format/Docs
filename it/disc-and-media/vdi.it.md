{
  "date" : "2021-08-11",
  "keywords" :[ "file vdi", "formato file vdi", "cos'è un file vdi", "file", "esempio vdi", "estensione file vdi", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file VDI e le API che possono creare e aprire file VDI.",
  "title" :"VDI - File immagine disco virtuale VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Che cos'è un file VDI?
Un file con estensione .vdi è un'immagine del disco virtuale; specifico per il programma di virtualizzazione desktop open source di Oracle chiamato VirtualBox. I file VDI vengono utilizzati per avviare la macchina virtuale VirtualBox. Le macchine virtuali consentono agli utenti di eseguire sistemi operativi o programmi aggiuntivi su un singolo computer. Quindi, il vantaggio dei file VDI è che gli utenti possono salvare questi file di immagine del disco sul proprio disco rigido e possono eseguirli utilizzando emulatori ogni volta che ne hanno bisogno.

## Formato file VDI
Virtual Disk Image (VDI) è il formato di file del disco principale per una VM Oracle open source sviluppata attivamente nota come VirtualBox, che è un prodotto di virtualizzazione di classe enterprise. Il formato di file VDI è progettato per creare un'immagine disco portatile che può essere facilmente eseguita utilizzando altri programmi di virtualizzazione. Supporta sia l'archiviazione allocata dinamicamente che quella a dimensione fissa. Ti permette di espandere un file immagine dopo che è stato creato, anche se contiene già dei dati.

### Virtualizzazione del disco
Il sistema emula i dischi rigidi in formato immagine disco VDI. Una VM VirtualBox può utilizzare dischi precedenti creati in Microsoft Virtual PC o VMware, nonché il proprio formato nativo. VirtualBox è anche in grado di connettersi a destinazioni iSCSI e partizionare non elaborato sull'host, utilizzando entrambi come dischi rigidi virtuali. VirtualBox emula IDE (controller PIIX4 e ICH6), SATA (controller ICH8M), controller SAS a cui è possibile collegare dischi rigidi e SCSI.

Il supporto è disponibile per Open Virtualization Format (OVF) dalla versione 2.2.0 di VirtualBox. Sia i dispositivi fisici collegati all'host che le immagini ISO possono essere montati come unità CD o DVD.
Per impostazione predefinita, VirtualBox supporta la grafica tramite una scheda grafica virtuale personalizzata compatibile VESA.

### Supporto per la virtualizzazione per Ethernet
VirtualBox virtualizza le seguenti schede di interfaccia di rete per una scheda di rete Ethernet:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Desktop Intel Pro/1000 MT (82540EM)
- Server Intel Pro/1000 MT (82545EM)
-Server Intel Pro/1000 T (82543GC)
- Adattatore di rete paravirtualizzato (virtio-net)

Le schede di rete emulate consentono l'esecuzione dei sistemi operativi guest senza la necessità di cercare e installare i driver per l'hardware di rete poiché sono disponibili come parte del sistema operativo guest. Uno speciale adattatore di rete paravirtualizzato migliora le prestazioni della rete riducendo la necessità di abbinare un'interfaccia hardware specifica. Pertanto, richiede un supporto speciale del driver nel guest.


## Riferimenti

* [VirtualBox - di Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


