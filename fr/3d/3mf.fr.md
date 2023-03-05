{
  "date" : "2019-12-09",
  "keywords" :[ "fichier 3mf", "format de fichier 3mf", "qu'est-ce qu'un fichier 3mf", "fichier", "exemple 3mf", "extension de fichier 3mf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"En savoir plus sur le format de fichier 3MF et les API qui peuvent ouvrir et créer des fichiers 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Qu'est-ce qu'un fichier 3MF ?

3MF, 3D Manufacturing Format, est utilisé par les applications pour restituer des modèles d'objets 3D à une variété d'autres applications, plates-formes, services et imprimantes. Il a été conçu pour éviter les limitations et les problèmes des autres formats de fichiers 3D, comme [STL](/fr/cad/stl/), pour travailler avec les dernières versions des imprimantes 3D. 3MF est un format de fichier relativement nouveau qui a été développé et publié par le consortium 3MF. Il est suffisamment riche pour décrire complètement un modèle, en conservant les informations internes, la couleur et d'autres caractéristiques qui le rendent extensible pour prendre en charge de nouvelles innovations dans l'impression 3D. Le format est extensible, capable d'être largement adopté et exempt de problèmes affectant d'autres formats de fichiers largement utilisés.

## Bref historique du format de fichier 3MF

Les limitations existantes dans les formats de fichiers descriptifs de modèles disponibles, tels que STL et autres, conduisent les grandes marques à se réunir et à formuler un format de fichier plus extensible pour l'impression 3D. Une considération importante était de savoir comment les applications devaient transmettre les données du modèle aux imprimantes 3D. Le consortium 3MF a donc vu le jour pour soutenir un nouveau format de fichier 3D appelé 3MF dans le but de le rendre suffisamment extensible pour répondre aux besoins de l'impression 3D. Plusieurs entreprises faisaient partie de ce consortium dont Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP et autres. Microsoft a fait don de son travail en cours sur le format de fichier 3D comme point de départ du développement collaboratif de la spécification par le consortium 3MF.

## Format de fichier 3MF - Plus d'informations

3MF est un format de données basé sur XML - XML compressé lisible par l'homme - qui inclut des définitions pour les données liées à la fabrication 3D, y compris l'extensibilité tierce pour les données personnalisées. Le format de fichier 3MF a été conçu en gardant à l'esprit les limitations et les problèmes rencontrés par les autres formats de fichiers 3D. Cela a conduit à la formulation du format de fichier 3MF qui est :

* **Complète :** Contenant toutes les informations nécessaires sur le modèle, les matériaux et les propriétés dans une seule archive
* **Lisible par l'utilisateur :** Utilisation de structures courantes telles que OPC, [ZIP](/fr/compression/zip/) et XML pour faciliter le développement
* **Simple :** Une spécification courte et claire, facilitant le développement et accélérant la validation
* **Extensible :** L'exploitation des espaces de noms XML permet des extensions publiques et privées tout en maintenant la compatibilité
* ** Sans ambiguïté : ** Un langage clair et des tests de conformité garantissent qu'un fichier est toujours cohérent du numérique au physique
* **Gratuit :** L'accès et la mise en œuvre de la spécification 3MF est et sera toujours libre de redevances, de brevets et de licences

Les spécifications du format de fichier 3MF sont hébergées sur [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) pour un accès public et des mises à jour continues. La version actuelle publiée est la 1.2.3 qui décrit l'ensemble des conventions pour l'utilisation de XML et d'autres technologies largement disponibles pour décrire le contenu et l'apparence d'un ou plusieurs modèles 3D. Les développeurs qui souhaitent créer des systèmes de traitement des formats de fichiers 3MF peuvent se référer à ces spécifications à des fins de mise en œuvre.

## Spécifications du format de fichier 3MF

Le format de fichier 3MF utilise les spécifications Open Packaging sous forme d'archive ZIP pour son modèle physique. Il comprend un ensemble bien défini de parties et de relations qui remplissent un objectif particulier dans le document. Cela permet également au format de suivre la fonctionnalité du package, y compris les signatures numériques et les vignettes.

### Le document 3MF - Un aperçu

Un document 3MF typique se présente comme suit :

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

La charge utile comprend l'ensemble complet des pièces requises pour le traitement de la pièce de modèle 3D. Tout le contenu à utiliser pour fabriquer un objet décrit dans la charge utile 3D DOIT être contenu dans le document 3MF. La description de chaque partie de document ainsi que son statut comme requis ou en option sont indiqués dans le tableau suivant.


|**Nom**|**Description**|**Source de la relation**|**Obligatoire/Facultatif**
--- | --- | --- | ---
|Modèle 3D|Contient la description d'un ou plusieurs objets 3D pour la fabrication.|Package|REQUIS
|Core Properties|La partie OPC qui contient diverses propriétés de document.|Package|FACULTATIF
|Origine de la signature numérique|La partie OPC qui est la racine des signatures numériques dans le package.|Package|FACULTATIF
|Signature numérique|Parties OPC contenant chacune une signature numérique.|Origine de la signature numérique|FACULTATIF
|Certificat de signature numérique|Pièces OPC contenant un certificat de signature numérique.|Signature numérique|FACULTATIF
|PrintTicket|Fournit les paramètres à utiliser lors de la sortie du ou des objets 3D dans la partie modèle 3D.|Modèle 3D|FACULTATIF
|Vignette|Contient une petite image JPEG ou PNG qui représente les objets 3D dans le package ou le package dans son ensemble.|Package|FACULTATIF
|Texture 3D|Contient une texture utilisée pour appliquer une couleur à un objet 3D dans la partie Modèle 3D (disponible pour les extensions)|Modèle 3D|FACULTATIF
|Parties personnalisées|Parties OPC associées aux métadonnées|Package|FACULTATIF

Les [Pièces et relations](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [Modèles 3D](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Ressources d'objets](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Ressources matérielles](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) et [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) sections des spécifications document donnent des informations détaillées sur le document 3MF.

## Références ##

* [Spécifications du format de fichier 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - Par Wikipédia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

