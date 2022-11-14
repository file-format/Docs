{
  "date" : "2021-08-10",
  "keywords" :[ "fichier .ovf", "format de fichier", "qu'est-ce qu'un fichier .ovf", "fichier", "extension de fichier"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Découvrez ce qu'est un format de fichier .ovf et les API qui peuvent créer et ouvrir des fichiers OVF.",
  "title" :"Format de fichier OVF - Ouvrir le fichier de virtualisation",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Qu'est-ce qu'un fichier OVF ?

Un fichier OVF est un fichier texte qui contient des informations sur l'empaquetage et la distribution d'un logiciel qui s'exécute sur une machine virtuelle. Il est formaté selon les [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) qui décrit toutes les exigences (telles que la sécurité, la portabilité, l'efficacité et l'extensibilité) pour l'exécution d'applications sur des machines virtuelles. L'Organisation internationale de normalisation (ISO) a adopté OVF comme norme ISO 17203.

## Bref historique du format de fichier OVF

Le format de fichier OVF a été introduit par DMTF (Distributed Management Task Force) qui crée des normes de gérabilité ouvertes. Il est indépendant de toute architecture particulière d'hyperviseur ou de jeu d'instructions. Le package OVF contient un ou plusieurs systèmes virtuels, chacun pouvant être déployé sur une machine virtuelle.

## Format de fichier OVF - Plus d'informations

Un package OVF se compose de plusieurs fichiers placés dans un seul répertoire. Parmi ceux-ci, il contient exactement un fichier descripteur OVF (avec l'extension .ovf) qui est stocké au format de fichier [XML](/fr/web/xml/). Il décrit les informations de machine virtuelle packagées et les informations de métadonnées sur le package OVF, telles que :

* Nom
* Exigences matérielles
* références aux autres fichiers du package OVF, et
* descriptions lisibles par l'homme

Les autres fichiers pouvant être trouvés dans un package OVF incluent une ou plusieurs images de disque et éventuellement des fichiers de certificat et d'autres fichiers auxiliaires.

## Références

* [Format de virtualisation ouvert - DMTF](https://www.dmtf.org/standards/ovf)
* [Spécifications du format de fichier OVF] (https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

