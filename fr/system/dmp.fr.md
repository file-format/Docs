{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "extension", "fichier", "format", "système", "MemoryDump", "Minidump", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Format de fichier MemoryDump",
  "description":"En savoir plus sur le format de fichier DMP et les API qui peuvent créer et ouvrir des fichiers DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Qu'est-ce qu'un fichier DMP ? ##

Le fichier DMP est principalement associé au format de fichier MemoryDump ou Minidump. Il est utilisé dans le système d'exploitation Microsoft Windows pour stocker les données qui ont été extraites de l'espace mémoire de l'ordinateur. Habituellement, les fichiers DMP sont créés lorsqu'un fichier plante ou qu'une erreur se produit. Parfois, les fichiers DMP sont très importants pour les experts techniques ou les utilisateurs d'ordinateurs avancés pour résoudre les problèmes auxquels vous êtes confrontés et résoudre tout type de problème d'application. Les fichiers DMP sont stockés sous un format propriétaire dans Microsoft qui est utilisé par le système d'exploitation pour déboguer toute application installée sur le système.


## Spécification technique du format de fichier DMP

Sous Windows, l'outil système "savedump.exe" génère des fichiers .dmp qui peuvent ensuite être traités par divers utilitaires de débogage disponibles. Le mini dump (64/128 Ko) est stocké par Windows dans le répertoire '%SystemRoot%\Minidump'. D'autre part, la mémoire du noyau et les vidages de mémoire complète sont stockés à la racine du système en tant que fichiers 'Memory.dmp'. Les fichiers de vidage mémoire sont des fichiers relativement volumineux et peuvent donc occuper une quantité suffisante d'espace de stockage. Il est donc conseillé de supprimer les fichiers .dmp inutiles qui, selon vous, ne seront pas utiles pour résoudre les problèmes.

Vous pouvez supprimer les fichiers .dmp manuellement ou en utilisant l'"assistant de nettoyage de disque" par défaut sur votre ordinateur. Les extensions DMP sont utilisées par les produits de base de données Oracle pour utiliser les fichiers .dmp dans les fichiers de base de données de sauvegarde et de récupération créés et utilisés. Les fichiers DMP créés par Oracle sont des sauvegardes de base de données qui peuvent être utilisées pour importer ou restaurer dans une instance de base de données en cours d'exécution via un serveur de base de données. Dans la plupart des cas, les fichiers .dmp ont des horodatages comme noms de fichiers.

### Contenu du fichier DMP

Un fichier de vidage mémoire contient :

* L'instruction stop et ses paramètres ;
* Une liste des pilotes chargés ;
* Le contexte du processeur (PRCB) pour les processus qui ont interrompu le fonctionnement normal de Windows ;
* Le contexte du noyau et les informations sur le processeur (EPROCESSES) pour les processus qui ont été arrêtés ;
* Le contexte du noyau et les informations sur le processeur (ETHREAD) pour le thread qui s'est arrêté ;
* La pile d'appels en mode noyau pour le thread qui a mis fin à l'exécution du processus.


## Exemple de DMP

L'erreur d'arrêt 0XC0000218 (Registry_File_Failure) crée un fichier DMP comme suit :

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## Référence ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

