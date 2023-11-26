{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier ADMX - Format de fichier de modèle d'administration de stratégie de groupe",
  "description":"Découvrez le format de fichier ADMX et comment ouvrir les fichiers ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Qu'est-ce qu'un fichier ADMX ?

Un fichier ADMX est un fichier de configuration de stratégie utilisé par le logiciel de stratégie de groupe Microsoft Windows qui gère un groupe d'ordinateurs dans un groupe. Il s'agit d'un fichier de modèle d'administration basé sur XML et a été introduit avec Windows Vista Service Pack 1. Les fichiers ADMX contiennent des paramètres de configuration pour les comptes d'utilisateurs, les configurations du système d'exploitation et les applications. Les fichiers ADMX sont utilisés pour stocker et déployer les configurations pour la gestion centralisée de nombreux systèmes informatiques.

Vous pouvez créer ou modifier des fichiers ADMX à l'aide de n'importe quel éditeur de texte ou éditeur d'objets de stratégie de groupe Microsoft compatible XML.

## Format de fichier ADMX - Plus d'informations

Les fichiers ADMX sont stockés au format de fichier universel [XML](/fr/web/xml/) lisible par l'homme. Il s'agit d'un format de fichier multilingue qui permet aux administrateurs système de différentes langues de travailler avec les mêmes fichiers ADMX. Les fichiers ADMX ont remplacé l'ancien format de fichier [ADM](/fr/system/adm/), qui est un format de fichier texte au format Unicode. Les fichiers ADMX spécifient les clés de registre qui sont modifiées lorsqu'un certain paramètre de stratégie de groupe est modifié.

### Que puis-je faire avec le fichier ADMX ?

Les fichiers ADMX définissent les actions qui doivent être autorisées sur les ordinateurs des utilisateurs faisant partie d'un groupe. La politique de groupe impose les règles définies en combinaison avec le logiciel Active Directory. Les fichiers ADMX sont gérés à partir du magasin central sur le système d'exploitation Windows qui constitue un emplacement central dans le domaine.

Un fichier ADMX déployé dans un environnement de travail peut permettre aux administrateurs de mettre en œuvre des politiques telles que :

* Contrôler l'utilisation d'Internet
* Téléchargement de certains types de fichiers
* Utilisation de périphériques amovibles sur les systèmes

## Les références

* [Fichiers de modèles administratifs - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestion des fichiers de modèles d'administration](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

