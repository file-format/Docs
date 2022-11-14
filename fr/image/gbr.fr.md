{
  "date" : "2019-10-11",
  "keywords" :[ "fichier gbr", "format de fichier gbr", "qu'est-ce qu'un fichier gbr", "fichier", "exemple gbr", "extension de fichier gbr","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier GBR - Format de fichier Gerber pour PCB",
  "description":"En savoir plus sur le format de fichier GBR et les API qui peuvent créer et ouvrir des fichiers GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier GBR ?

Un fichier avec l'extension .gbr est un format de fichier image Gerber pour l'échange de transfert de données de conception de carte de circuit imprimé (PCB). Il a été développé par Ucamco. Les données de conception de PCB sont le principal composant requis par l'industrie de fabrication pour la manipulation. Un fichier GRB contient des données PCB telles que les couches de cuivre, le masque de soudure, la légende et les données de perçage et de routage. Il peut être utilisé pour transférer des données telles que les caractéristiques de fabrication des PCB, y compris l'épaisseur ou la finition dans un format standardisé. Tous les systèmes de conception de PCB génèrent des fichiers Gerber qui peuvent être gérés par les systèmes de fabrication de PCB. Les fichiers GBR sont désormais devenus la norme de facto pour le transfert de données de conception de cartes de circuits imprimés (PCB). Ucamco a fourni une [visionneuse en ligne gratuite](https://gerber-viewer.ucamco.com/) pour ouvrir et afficher les formats de fichiers GBR.

## Format de fichier GBR

GBR est un format UTF-8 lisible par l'homme qui se compose de seulement 27 commandes. En raison de cette courte liste de commandes et de sa compacité, GBR est facile à déboguer. Gerber est à la base un format vectoriel ouvert pour les images binaires 2D. Les méta-informations sont transférées avec les images via les attributs. Un seul fichier GRB spécifie une seule image et ne nécessite aucun fichier d'accompagnement ou paramètre externe pour être interprété. Une image n'a besoin que d'un seul fichier. Il utilise des caractères ASCII 7 bits pour toutes les commandes et tous les noms définis dans la spécification qui sont imprimables. Cela couvre entièrement la génération d'image complète.

### Exemple de fichier GBR

Voici un exemple de fichier Gerber qui crée un cercle de 1,5 mm de diamètre centré sur l'origine. Il y a une commande par ligne.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Références

* [Format Gerber](https://www.ucamco.com/en/gerber)

