{
  "date": "2023-06-08",
  "keywords": [
"vmx tiedosto",
"mikä on vmx-tiedosto",
"vmx tiedosto esimerkki",
"kuinka avata vmx tiedosto",
"mitä vmx-tiedosto sisältää",
"mikä on vmx-tiedoston muoto",
"tiedosto",
"vmx tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VMX-tiedostomuoto - VMware Virtual Machine -määritystiedosto",
  "description": "Opi VMX-muodosta ja API-liittymistä, jotka voivat luoda ja avata VMX-tiedostoja.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx-fi",
      "parent": "settings"
}
},
  "lastmod": "2023-06-08"
}

## Mikä on VMX-tiedosto?

VMX-tiedosto, joka tunnetaan myös nimellä virtuaalikoneen määritystiedosto, on pelkkä tekstitiedosto, jota VMware-virtualisointiohjelmisto käyttää virtuaalikoneen (VM) asetusten ja konfiguraatioiden määrittämiseen. VMX-tiedostot sisältävät tietoja, kuten VM:n laitteistokokoonpanon, virtuaalilevykartoitukset, verkkoasetukset ja muut parametrit.

## Esimerkki VMX-tiedostosta

Tässä on esimerkki siitä, miltä VMX-tiedosto voi näyttää:

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

## Mitä VMX-tiedosto sisältää?

VMX-tiedosto sisältää erilaisia virtuaalikoneen (VM) konfigurointiasetuksia. Tässä on joitain VMX-tiedostossa yleisesti löydettyjä asetuksia:

- `.encoding:` Määrittää tiedostossa käytetyn merkkikoodauksen.
- `config.version:` Ilmaisee VMX-tiedostomuodon version.
- `virtualHW.version:` Määrittää virtuaalikoneen virtuaalisen laitteiston version.
- `guestOS:` Määrittää virtuaalikoneeseen asennetun vieraskäyttöjärjestelmän.
- `memSize:` Määrittää VM:lle varatun muistin määrän.
- `displayName:` Asettaa virtuaalikoneen näyttönimen tai tunnisteen.
- `powerType:` Määrittää virrankäytön eri toimintoja varten (virrankatkaisu, virta päälle, nollaus, keskeytys).
- `floppyX:` Levykeasemiin liittyvät asetukset, kuten läsnäolo- ja tiedostokartoitukset.
- `numvcpus:` Määrittää virtuaalikoneelle määritettyjen virtuaalisuorittimien määrän.
- `scsiX:` SCSI-ohjainten ja niihin liittyvien virtuaalilevyjen määritysasetukset.
- `ethernetX:` Verkkosovittimien määritysasetukset, mukaan lukien virtuaalisen laitteen tyyppi, verkon nimi ja osoitetyyppi.
- `ideX:` IDE-ohjainten ja niihin liittyvien virtuaalilevyjen konfigurointiasetukset.
- `usbX:` USB-laitteiden määritysasetukset, kuten läsnäolo- ja yhteystiedot.
- `ääni:` Virtuaaliäänesovittimen konfigurointiasetukset.
- `tools.syncTime:` Ilmaisee, onko ajan synkronointi isäntäjärjestelmän kanssa käytössä.
- `uuid.bios:` Määrittää virtuaalikoneen BIOS UUID:n.
- `uuid.location:` Määrittää virtuaalikoneen sijainnin UUID:n.

## Kuinka avata VMX-tiedosto?

VMX-tiedoston avaamista manuaalisesti ei suositella. Kun käytät virtuaalikoneen VMware Fusionilla, ohjelmisto lataa tiedot automaattisesti VMX-tiedostosta.

Jos kuitenkin haluat muokata VMX-tiedostoa manuaalisesti, voit tehdä sen millä tahansa tekstieditorilla, esim. Muistiolla (Windows) tai TextEditillä (Mac).

## Mikä on VMX-tiedoston muoto?

VMX-tiedosto on pelkkä tekstitiedosto tietyssä muodossa. Muoto noudattaa avain-arvo-parirakennetta, jossa jokainen rivi edustaa erillistä määritysvaihtoehtoa.

VMX-tiedoston yleinen muoto on seuraava:

```
key1 = value1
key2 = value2
key3 = value3
```

Jokainen rivi koostuu avaimesta, jota seuraa yhtäläisyysmerkki (=) ja vastaava arvo. Avain edustaa tiettyä kokoonpanoasetusta ja arvo edustaa tälle asetukselle määritettyä arvoa.

Esimerkiksi `memSize = 8192 VMX-tiedostossa määrittää, että virtuaalikoneen muistiraja on 8192 Mt RAM-muistia.

VMX-tiedoston muoto voi sisältää myös kommentteja, jotka on merkitty rivin alussa olevalla puntamerkillä (#), jotka VMware-ohjelmisto jättää huomioimatta tiedostoa jäsennettäessä. Kommentteja käytetään usein antamaan lisätietoja tai selityksiä tietyille asetuksille.

## Viitteet
* [VMX-esimerkkitiedosto](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)





