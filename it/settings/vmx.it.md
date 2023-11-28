{
"data": "08-06-2023",
  "keywords": [
"file vmx",
"cos'è un file vmx",
"Esempio di file vmx",
"come aprire il file vmx",
"cosa contiene il file vmx",
"qual è il formato del file vmx",
"file",
"estensione file vmx",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file VMX - File di configurazione della macchina virtuale VMware",
  "description":"Informazioni sul formato VMX e sulle API in grado di creare e aprire file VMX.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent" : "settings"
}
},
"lastmod": "2023-06-08"
}

## Cos'è un file VMX?

Un file VMX, noto anche come file di configurazione della macchina virtuale, è un file di testo semplice utilizzato dal software di virtualizzazione VMware per definire le impostazioni e la configurazione della macchina virtuale (VM). I file VMX contengono informazioni come la configurazione hardware della VM, mappature del disco virtuale, impostazioni di rete e altri parametri.

## Esempio di file VMX

Ecco un esempio di come potrebbe apparire il file VMX:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## Cosa contiene il file VMX?

Un file VMX contiene varie impostazioni di configurazione per la macchina virtuale (VM). Ecco alcune delle impostazioni comunemente presenti nel file VMX:

- `.encoding:` Specifica la codifica dei caratteri utilizzata nel file.
- `config.version:` Indica la versione del formato file VMX.
- `virtualHW.version:` Specifica la versione dell'hardware virtuale per la VM.
- "guestOS:" specifica il sistema operativo guest installato nella VM.
- `memSize:` Definisce la quantità di memoria allocata alla VM.
- "displayName:" imposta il nome visualizzato o l'etichetta per la VM.
- `powerType:` Definisce il comportamento di alimentazione per diverse operazioni (spegnimento, accensione, ripristino, sospensione).
- `floppyX:` Impostazioni di configurazione relative alle unità floppy, come presenza e mappature dei file.
- `numvcpus:` Specifica il numero di CPU virtuali assegnate alla VM.
- "scsiX:" Impostazioni di configurazione per i controller SCSI e i relativi dischi virtuali associati.
- "ethernetX:" impostazioni di configurazione per gli adattatori di rete, incluso il tipo di dispositivo virtuale, il nome della rete e il tipo di indirizzo.
- "ideX:" Impostazioni di configurazione per i controller IDE e i relativi dischi virtuali associati.
- "usbX:" Impostazioni di configurazione per i dispositivi USB, come dettagli sulla presenza e sulla connessione.
- `sound:` Impostazioni di configurazione per l'adattatore audio virtuale.
- `tools.syncTime:` Indica se la sincronizzazione dell'ora con il sistema host è abilitata.
- `uuid.bios:` Specifica l'UUID del BIOS della VM.
- `uuid.location:` Specifica l'UUID della posizione della VM.

## Come aprire il file VMX?

Non è consigliabile aprire manualmente un file VMX. Quando esegui una macchina virtuale utilizzando VMware Fusion, il software carica automaticamente le informazioni dal file VMX.

Tuttavia, se desideri modificare manualmente il file VMX, puoi farlo utilizzando qualsiasi editor di testo, ad esempio Blocco note (Windows) o TextEdit (Mac).

## Qual è il formato del file VMX?

Un file VMX è un file di testo semplice con un formato specifico. Il formato segue una struttura di coppie chiave-valore in cui ciascuna riga rappresenta un'opzione di configurazione separata.

Il formato generale del file VMX è il seguente:

```
key1 = value1
key2 = value2
key3 = value3
```

Ogni riga è composta da una chiave seguita dal segno uguale (=) e dal valore corrispondente. La chiave rappresenta un'impostazione di configurazione specifica e il valore rappresenta il valore assegnato a tale impostazione.

Ad esempio, `memSize = "8192"` nel file VMX specifica che il limite di memoria della macchina virtuale è 8192 MB di RAM.

Il formato del file VMX può includere anche commenti, indicati da un segno di cancelletto (#) all'inizio della riga, che vengono ignorati dal software VMware durante l'analisi del file. I commenti vengono spesso utilizzati per fornire informazioni aggiuntive o spiegazioni per impostazioni specifiche.

## Riferimenti
* [File VMX di esempio](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




