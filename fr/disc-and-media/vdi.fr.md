{
  "date" : "2021-08-11",
  "keywords" :["fichier vdi", "format de fichier vdi", "qu'est-ce qu'un fichier vdi", "fichier", "exemple vdi", "extension de fichier vdi","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier VDI et les API qui peuvent créer et ouvrir des fichiers VDI.",
  "title" :"VDI - Fichier d'image de disque virtuel VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Qu'est-ce qu'un fichier VDI ?
Un fichier avec l'extension .vdi est une image de disque virtuel ; spécifique au programme de virtualisation de bureau open source d'Oracle appelé VirtualBox. Les fichiers VDI sont utilisés pour démarrer la machine virtuelle VirtualBox. Les machines virtuelles permettent aux utilisateurs d'exécuter des systèmes d'exploitation ou des programmes supplémentaires sur un seul ordinateur. Par conséquent, l'avantage des fichiers VDI est que les utilisateurs peuvent enregistrer ces fichiers d'image de disque sur leur disque dur et les exécuter à l'aide d'émulateurs chaque fois qu'ils en ont besoin.

## Format de fichier VDI
L'image de disque virtuel (VDI) est le principal format de fichier de disque pour une machine virtuelle Oracle open source activement développée connue sous le nom de VirtualBox, qui est un produit de virtualisation de classe entreprise. Le format de fichier VDI est conçu pour créer une image de disque portable qui peut être facilement exécutée à l'aide d'autres programmes de virtualisation. Il prend en charge le stockage à allocation dynamique et à taille fixe. Il vous permet de développer un fichier image après sa création, même s'il contient déjà des données.

### Virtualisation de disque
Le système émule les disques durs au format d'image disque VDI. Une machine virtuelle VirtualBox peut utiliser des disques antérieurs créés dans Microsoft Virtual PC ou VMware, ainsi que son propre format natif. La VirtualBox est également capable de se connecter aux cibles iSCSI et de partitionnement brut sur l'hôte, en utilisant l'un ou l'autre comme disques durs virtuels. VirtualBox émule IDE (contrôleurs PIIX4 et ICH6), SATA (contrôleur ICH8M), contrôleurs SAS auxquels des disques durs peuvent être connectés et SCSI.

Le support est disponible pour Open Virtualization Format (OVF) depuis la version 2.2.0 de VirtualBox. Les périphériques physiques connectés à l'hôte et les images ISO peuvent être montés en tant que lecteurs de CD ou de DVD.
Par défaut, VirtualBox prend en charge les graphiques via une carte graphique virtuelle personnalisée compatible VESA.

### Prise en charge de la virtualisation pour Ethernet
VirtualBox virtualise les cartes d'interface réseau suivantes pour un adaptateur réseau Ethernet :
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Ordinateur de bureau Intel Pro/1000 MT (82540EM)
- Serveur Intel Pro/1000 MT (82545EM)
- Serveur Intel Pro/1000 T (82543GC)
- Adaptateur réseau paravirtualisé (virtio-net)

Les cartes réseau émulées permettent aux systèmes d'exploitation invités de s'exécuter sans qu'il soit nécessaire de rechercher et d'installer des pilotes pour le matériel réseau, car ils sont disponibles dans le cadre du système d'exploitation invité. Un adaptateur réseau spécial paravirtualisé améliore les performances du réseau en réduisant le besoin de faire correspondre une interface matérielle spécifique. Par conséquent, il nécessite un support de pilote spécial dans l'invité.


## Références

* [VirtualBox - par Wikipédia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


