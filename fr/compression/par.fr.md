{
"date": "2023-07-18",
   "keywords":[
"PAR",
"Fichier PAR",
"comment ouvrir un fichier par",
"déposer",
"Extension de fichier PAR",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier PAR - Fichier d'index Parchive",
   "description":"Découvrez le format PAR et les API permettant de créer et d'ouvrir des fichiers PAR.",
"linktitle": "PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent": "compression"
}
},
"lastmod": "2023-07-18"
}

## Qu'est-ce qu'un fichier PAR ?

Dans les archives Parchive (PAR), un fichier .par fait référence à un fichier d'index qui contient un groupe de volumes de parité ou de blocs de parité. Ce fichier d'index est utilisé à des fins de détection d'erreurs et de récupération lorsqu'un ou plusieurs fichiers de l'archive sont perdus ou endommagés.

Une archive Parchive comprend généralement à la fois les fichiers de données originaux et les volumes de parité correspondants. Les volumes de parité sont créés à l'aide des algorithmes de correction d'erreurs Reed-Solomon. Ces volumes de parité contiennent des informations redondantes qui peuvent être utilisées pour récupérer les fichiers de données d'origine.

Le fichier .par, également appelé ensemble de volumes de parité, contient des informations sur la structure et l'emplacement des volumes de parité dans l'archive. Il sert d'index ou de carte pour le processus de récupération. En utilisant le fichier .par, un logiciel PAR spécialisé peut déterminer quels volumes de parité sont nécessaires et comment ils doivent être utilisés pour reconstruire les fichiers manquants ou endommagés.

Lorsqu'un ou plusieurs fichiers de l'archive Parchive deviennent inaccessibles ou corrompus, le fichier .par peut être utilisé conjointement avec les volumes de parité disponibles pour récupérer les données perdues. Le logiciel PAR lit le fichier .par, identifie les fichiers manquants ou endommagés et utilise les volumes de parité pour les reconstruire.

## Comment ouvrir un fichier PAR?

Pour ouvrir et utiliser les fichiers .par, vous aurez besoin d'un logiciel PAR spécialisé. Voici quelques options logicielles populaires capables de gérer les fichiers .par :

- **QuickPar :** QuickPar est un logiciel PAR largement utilisé pour Windows. Il vous permet de créer, vérifier et réparer des fichiers PAR. Vous pouvez ouvrir un fichier .par dans QuickPar pour vérifier son intégrité ou l'utiliser pour réparer des fichiers endommagés ou manquants dans une archive Parchive.

- **MultiPar :** MultiPar est un autre logiciel PAR populaire disponible pour Windows. Il prend en charge les formats de fichiers PAR et PAR2 et fournit des fonctionnalités avancées pour créer, vérifier et réparer des archives. MultiPar peut ouvrir des fichiers .par et effectuer des opérations de détection d'erreurs et de récupération en fonction des volumes de parité fournis.

- **MacPAR deLuxe :** MacPAR deLuxe est un logiciel PAR conçu spécifiquement pour macOS. Il prend en charge les formats de fichiers PAR et PAR2 et offre des fonctionnalités similaires à celles de QuickPar et MultiPar. MacPAR deLuxe peut ouvrir les fichiers .par et aider à vérifier les archives et à récupérer les fichiers endommagés ou manquants.

## Format de fichier PAR - Plus d'informations

Le format de fichier PAR, communément appelé Parchive, est un format de fichier spécifique utilisé pour créer des données de parité et effectuer la détection et la récupération des erreurs dans les archives de fichiers. Le format de fichier PAR se compose généralement de trois types : PAR, PAR2 et PAR3.

- **PAR :** Le format de fichier PAR original, également connu sous le nom de PAR1, a été développé par le projet Parchive. Il inclut les données de parité générées à partir des fichiers de données d'origine. Les fichiers PAR fournissent un niveau de base de détection et de récupération des erreurs, mais présentent des limites en termes de capacités de correction des erreurs.

- **PAR2 :** PAR2 est une version améliorée du format de fichier PAR. Il offre des capacités de correction d'erreurs plus avancées et des fonctionnalités de récupération améliorées. Les fichiers PAR2 sont généralement utilisés pour créer des données de parité permettant de récupérer des fichiers perdus ou endommagés dans une archive. Les fichiers PAR2 offrent une meilleure protection contre la corruption des données et sont largement utilisés à des fins d'archivage de fichiers.

- **PAR3 :** PAR3 est la dernière version du format de fichier PAR et offre de nouvelles améliorations en matière de correction d'erreurs et de récupération. Il offre des niveaux encore plus élevés de capacités de redondance et de correction d’erreurs par rapport au PAR2. Les fichiers PAR3 sont conçus pour fournir des options de protection et de récupération plus robustes pour les données stockées dans les archives.

Les formats de fichiers PAR2 et PAR3 sont largement pris en charge par le logiciel PAR et offrent la possibilité de vérifier l'intégrité des fichiers dans une archive et de récupérer les données perdues ou endommagées. Les fichiers PAR et PAR2 sont encore couramment utilisés, tandis que les fichiers PAR3 sont progressivement adoptés en raison de leurs capacités améliorées de correction d'erreurs.

## Les références
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

