{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier ADM - Format de fichier de modèle d'administration",
  "description":"Découvrez le format de fichier ADM et comment ouvrir les fichiers ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Qu'est-ce qu'un fichier ADM ?

Un fichier ADM est un fichier modèle utilisé par le logiciel de stratégies de groupe Microsoft pour spécifier l'emplacement des paramètres de stratégie basés sur le registre dans le fichier de registre. Il est utilisé par les administrateurs système pour définir la politique de gestion d'un groupe d'ordinateurs faisant partie du groupe. Ces informations font partie des objets de stratégie de groupe (GPO) créés pour la gestion du groupe.

Vous pouvez ouvrir les fichiers ADM à l'aide de l'éditeur d'objets de stratégie de groupe Microsoft.

## Format de fichier ADM - Plus d'informations

Les fichiers ADM sont stockés sous forme de fichiers texte au format Unicode. Ceux-ci étaient principalement utilisés pour décrire l'emplacement des paramètres de stratégie basés sur le registre dans le registre Windows Vista et Windows 7.

Les fichiers ADM ne sont plus pris en charge et ont été remplacés par les fichiers [ADMX](/fr/system/admx/). GPA ignore les fichiers ADM par défaut suivants sur les ordinateurs exécutant Microsoft Windows Vista Service Pack 1 ou version ultérieure.

* système.adm
* inetres.adm
* conf.adm
* wmplayer.adm
*wuau.adm

## Les références

* [Fichiers de modèles administratifs - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestion des fichiers de modèles d'administration](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

