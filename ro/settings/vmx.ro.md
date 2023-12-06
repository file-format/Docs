{
"data": "2023-06-08",
  "keywords": [
"fișier vmx",
"Ce este un fișier vmx",
"exemplu de fișier vmx",
"cum se deschide fișierul vmx",
"ce conține fișierul vmx",
"care este formatul fișierului vmx",
"fişier",
"extensie fișier vmx",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fișier VMX - Fișier de configurare a mașinii virtuale VMware",
  "description":"Aflați despre formatul VMX și despre API-urile care pot crea și deschide fișiere VMX.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## Ce este un fișier VMX?

Un fișier VMX, cunoscut și ca fișier de configurare a mașinii virtuale, este un fișier text simplu utilizat de software-ul de virtualizare VMware pentru a defini setările și configurația mașinii virtuale (VM). Fișierele VMX conțin informații precum configurația hardware a VM, mapările discurilor virtuale, setările de rețea și alți parametri.

## Exemplu de fișier VMX

Iată un exemplu despre cum ar putea arăta fișierul VMX:

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

## Ce conține fișierul VMX?

Un fișier VMX conține diverse setări de configurare pentru mașina virtuală (VM). Iată câteva dintre setările frecvent întâlnite în fișierul VMX:

- `.encoding:` Specifică codarea caracterelor folosită în fișier.
- `config.version:` indică versiunea formatului de fișier VMX.
- `virtualHW.version:` Specifică versiunea hardware-ului virtual pentru VM.
- `guestOS:` Specifică sistemul de operare invitat instalat în VM.
- `memSize:` Definește cantitatea de memorie alocată VM-ului.
- `displayName:` Setează numele afișat sau eticheta pentru VM.
- `powerType:` Definește comportamentul alimentării pentru diferite operațiuni (oprire, pornire, resetare, suspendare).
- `floppyX:` Setări de configurare legate de unitățile de dischete, cum ar fi prezența și mapările fișierelor.
- `numvcpus:` Specifică numărul de procesoare virtuale atribuite VM.
- `scsiX:` Setări de configurare pentru controlerele SCSI și discurile virtuale asociate acestora.
- `ethernetX:` Setări de configurare pentru adaptoarele de rețea, inclusiv tipul de dispozitiv virtual, numele rețelei și tipul de adresă.
- `ideX:` Setări de configurare pentru controlerele IDE și discurile virtuale asociate acestora.
- `usbX:` Setări de configurare pentru dispozitivele USB, cum ar fi prezența și detaliile conexiunii.
- `sound:` Setări de configurare pentru adaptorul de sunet virtual.
- `tools.syncTime:` indică dacă sincronizarea orei cu sistemul gazdă este activată.
- `uuid.bios:` Specifică UUID-ul BIOS al mașinii virtuale.
- `uuid.location:` Specifică locația UUID-ului VM.

## Cum se deschide fișierul VMX?

Deschiderea manuală a unui fișier VMX nu este recomandată. Când rulați o mașină virtuală folosind VMware Fusion, software-ul încarcă automat informațiile din fișierul VMX.

Cu toate acestea, dacă doriți să editați manual fișierul VMX, puteți face acest lucru folosind orice editor de text, de exemplu Notepad (Windows) sau TextEdit (Mac).

## Care este formatul fișierului VMX?

Un fișier VMX este un fișier text simplu cu un anumit format. Formatul urmează o structură de pereche cheie-valoare în care fiecare linie reprezintă o opțiune de configurare separată.

Formatul general al fișierului VMX este următorul:

```
key1 = value1
key2 = value2
key3 = value3
```

Fiecare linie constă dintr-o cheie urmată de semnul egal (=) și valoarea corespunzătoare. Tasta reprezintă o anumită setare de configurare, iar valoarea reprezintă valoarea atribuită acelei setări.

De exemplu, `memSize = "8192"` în fișierul VMX specifică că limita de memorie a mașinii virtuale este de 8192 MB de RAM.

Formatul fișierului VMX poate include, de asemenea, comentarii, notate cu semnul lire sterline (#) la începutul liniei, care sunt ignorate de software-ul VMware la analizarea fișierului. Comentariile sunt adesea folosite pentru a oferi informații suplimentare sau explicații pentru anumite setări.

## Referințe
* [Eșantion de fișier VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




