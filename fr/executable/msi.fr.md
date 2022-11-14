{
  "date" : "2021-06-30",
  "keywords" :[ "fichier msi", "format de fichier MSI", "qu'est-ce qu'un fichier msi", "fichier", "exemple msi", "extension de fichier msi","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier MSI et les API qui peuvent créer et ouvrir des fichiers MSI.",
  "title" :"MSI - Fichier de package d'installation Windows",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Qu'est-ce qu'un fichier MSI ?
Un fichier MSI utilisé pour installer et lancer des programmes Windows ; un package complet pour Microsoft Windows qui contient des informations d'installation pour un programme logiciel typique, y compris les fichiers essentiels à installer et des informations sur l'emplacement d'installation. Les fichiers MSI peuvent également contenir le package pour les mises à jour logicielles. Les fichiers MSI sont similaires à [EXE](/fr/executable/exe/), mais EXE peut parfois ne pas inclure les informations d'installation et le logiciel peut s'exécuter directement lors de l'exécution du fichier EXE.

## Format de fichier MSI
Windows Installer est en fait une API (Application Programming Interface) et un composant logiciel de Microsoft Windows utilisé pour l'installation, la suppression et la maintenance d'un programme logiciel. Les informations d'installation et les fichiers facultatifs sont regroupés sous forme de packages d'installation et de bases de données vaguement relationnelles structurées en tant que stockages structurés COM ; bien connus sous le nom de **fichiers MSI**, ayant l'extension de fichier .msi. Les packages avec l'extension de fichier **.mst** contiennent **Transformation Scripts** de Windows Installer, les fichiers avec l'extension **.msm** contiennent **Merge Modules** et l'extension de fichier **.pcp** est utilisé pour les **Propriétés de création de patch**. Windows Installer devient plus avancé après avoir subi des modifications importantes par rapport à ses versions antérieures, l'API de configuration. Un cadre graphique et la génération automatique de la séquence de désinstallation sont les nouvelles fonctionnalités de Windows Installer. Il a été considéré maintenant comme une alternative aux frameworks d'installation exécutables autonomes.

### Structure logique des packages MSI
Un package désigne l'installation d'un ou plusieurs produits complets et est généralement identifié par un **GUID**. Un produit est constitué d'un ou plusieurs composants et regroupés en différentes fonctionnalités. Le programme d'installation de Windows ne gère pas les dépendances entre différents produits simultanément. La structure logique des packages se compose des éléments suivants :

- **Produits** : un programme de travail unique installé ou un ensemble de plusieurs programmes combinés est un produit. Un produit est identifié par un GUID unique.
- **Fonctionnalités** : peut contenir n'importe quel nombre de composants et d'autres sous-fonctionnalités. Les packages plus petits peuvent être constitués d'une seule fonctionnalité.
- **Composants** : le composant est traité par Windows Installer comme une unité ; peut contenir des fichiers de programme, des dossiers, des clés de registre, des composants COM et des raccourcis.
- **Chemins de clé** : un chemin de clé est un fichier spécifique, une source de données ODBC ou une clé de registre que l'auteur du package spécifie comme critique pour un composant donné.

## Références

* [Windows Installer - par Wikipédia](https://en.wikipedia.org/wiki/Windows_Installer)


