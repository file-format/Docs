{
"date": "08/06/2023",
  "keywords": [
"fichier vmx",
"qu'est-ce qu'un fichier vmx",
"exemple de fichier vmx",
"comment ouvrir le fichier vmx",
"que contient le fichier vmx",
"quel est le format du fichier vmx",
"déposer",
"extension de fichier VMX",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier VMX - Fichier de configuration de la machine virtuelle VMware",
  "description":"Découvrez le format VMX et les API permettant de créer et d'ouvrir des fichiers VMX.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent": "paramètres"
}
},
"lastmod": "2023-06-08"
}

## Qu'est-ce qu'un fichier VMX ?

Un fichier VMX, également appelé fichier de configuration de machine virtuelle, est un fichier texte brut utilisé par le logiciel de virtualisation VMware pour définir les paramètres et la configuration de la machine virtuelle (VM). Les fichiers VMX contiennent des informations telles que la configuration matérielle de la VM, les mappages de disques virtuels, les paramètres réseau et d'autres paramètres.

## Exemple de fichier VMX

Voici un exemple de ce à quoi pourrait ressembler un fichier VMX :

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

## Que contient le fichier VMX ?

Un fichier VMX contient divers paramètres de configuration pour la machine virtuelle (VM). Voici quelques-uns des paramètres les plus courants dans le fichier VMX :

- `.encoding :` Spécifie le codage de caractères utilisé dans le fichier.
- `config.version :` Indique la version du format de fichier VMX.
- `virtualHW.version :` Spécifie la version du matériel virtuel pour la VM.
- `guestOS :` Spécifie le système d'exploitation invité installé dans la VM.
- `memSize :` Définit la quantité de mémoire allouée à la VM.
- `displayName :` Définit le nom d'affichage ou l'étiquette de la VM.
- `powerType :` Définit le comportement d'alimentation pour différentes opérations (mise hors tension, mise sous tension, réinitialisation, suspension).
- `floppyX :` Paramètres de configuration liés aux lecteurs de disquettes, tels que la présence et les mappages de fichiers.
- `numvcpus :` Spécifie le nombre de CPU virtuels attribués à la VM.
- `scsiX :` Paramètres de configuration des contrôleurs SCSI et de leurs disques virtuels associés.
- `ethernetX :` paramètres de configuration pour les adaptateurs réseau, y compris le type de périphérique virtuel, le nom du réseau et le type d'adresse.
- `ideX :` Paramètres de configuration pour les contrôleurs IDE et leurs disques virtuels associés.
- `usbX :` Paramètres de configuration pour les périphériques USB, tels que les détails de présence et de connexion.
- `sound :` Paramètres de configuration de l'adaptateur audio virtuel.
- `tools.syncTime :` Indique si la synchronisation de l'heure avec le système hôte est activée.
- `uuid.bios :` Spécifie l'UUID du BIOS de la VM.
- `uuid.location :` Spécifie l'UUID d'emplacement de la VM.

## Comment ouvrir le fichier VMX?

L'ouverture manuelle d'un fichier VMX n'est pas recommandée. Lorsque vous exécutez une machine virtuelle à l'aide de VMware Fusion, le logiciel charge automatiquement les informations du fichier VMX.

Cependant, si vous souhaitez modifier manuellement le fichier VMX, vous pouvez le faire en utilisant n'importe quel éditeur de texte, par exemple Notepad (Windows) ou TextEdit (Mac).

## Quel est le format du fichier VMX ?

Un fichier VMX est un fichier texte brut avec un format spécifique. Le format suit une structure de paire clé-valeur où chaque ligne représente une option de configuration distincte.

Le format général du fichier VMX est le suivant :

```
key1 = value1
key2 = value2
key3 = value3
```

Chaque ligne se compose d'une clé suivie du signe égal (=) et de la valeur correspondante. La clé représente un paramètre de configuration spécifique et la valeur représente la valeur attribuée à ce paramètre.

Par exemple, « memSize = « 8192 » » dans le fichier VMX spécifie que la limite de mémoire de la machine virtuelle est de 8 192 Mo de RAM.

Le format du fichier VMX peut également inclure des commentaires, indiqués par un signe dièse (#) au début de la ligne, qui sont ignorés par le logiciel VMware lors de l'analyse du fichier. Les commentaires sont souvent utilisés pour fournir des informations supplémentaires ou des explications sur des paramètres spécifiques.

## Les références
* [Exemple de fichier VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




