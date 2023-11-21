{
"date": "20/07/2023",
   "keywords":[
"POUBELLE",
"Fichier BIN",
"déposer",
"Extension de fichier BIN",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier BIN - Fichier codé MacBinary",
   "description":"Découvrez le format BIN et les API permettant de créer et d'ouvrir des fichiers BIN.",
"linktitle": "BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
"parent": "compression"
}
},
"lastmod": "20/07/2023"
}

## Qu'est-ce qu'un fichier BIN ?

Un fichier BIN, dans le contexte des ordinateurs Macintosh, peut faire référence à un fichier enregistré au format MacBinary. MacBinary est un format de fichier spécialement conçu pour transférer des fichiers Macintosh via Internet, courrier électronique, FTP ou support portable. Le but de MacBinary est de préserver la structure complète des fichiers et les attributs des fichiers Macintosh, y compris à la fois la branche de données et la branche de ressources, au sein d'un seul fichier.

Le format MacBinary y parvient en encapsulant la branche de ressources et la branche de données du système de fichiers hiérarchique Macintosh (HFS) dans un fichier compressé. Il comprend également un en-tête de recherche contenant des métadonnées importantes sur le fichier. En combinant tous ces composants en un seul fichier, MacBinary garantit que le fichier conserve son intégrité et peut être facilement transféré et partagé sur différentes plates-formes.

Avec les progrès des systèmes de fichiers et des protocoles de transfert de fichiers d'Apple, l'utilisation des fichiers BIN et du format MacBinary est devenue moins courante. L'introduction de formats de fichiers tels que ZIP et la transition vers des systèmes de fichiers plus modernes, tels que HFS+ et APFS, ont réduit le besoin de fichiers codés en MacBinary. Ces systèmes de fichiers plus récents offrent des moyens plus efficaces de gérer les attributs de fichiers, les branches de ressources et les branches de données, rendant le format MacBinary moins nécessaire dans le paysage informatique actuel.

## Format de fichier BIN - Plus d'informations

Au début des ordinateurs Macintosh, les fichiers étaient stockés dans deux « forks » distincts en raison de limitations de données. La « branche de ressources » contenait des données structurées, tandis que la « branche de données » contenait des données non structurées. Alors que le Mac OS classique traitait ces forks comme un seul fichier, le transfert de fichiers vers des systèmes non Mac entraînait une perte de données car ils ne reconnaissaient pas les forks comme une entité unique. Pour résoudre ce problème, le format MacBinary a été créé par des individus comme les Dennis Brothers, Harry Chesley et Yves Lempereur. MacBinary a compressé et combiné les forks en un seul fichier, appelé fichier BIN, pour le transfert vers des systèmes non Mac. Au retour sur Mac OS, les fourches seraient à nouveau séparées. Avec l'abandon du HFS basé sur un fork dans les années 2000, l'utilisation du format MacBinary a considérablement diminué. Aujourd'hui, il est rare de rencontrer un fichier BIN codé en MacBinary, à moins que vous ne rencontriez un ancien fichier sur un système non Mac ou que vous n'en téléchargiez un sur Internet.

Le format MacBinary a connu plusieurs versions au fil du temps pour s'adapter aux changements dans les systèmes Macintosh et dans la gestion des fichiers. Voici quelques-unes des différentes versions du format MacBinary :

- **MacBinary I :** La version initiale de MacBinary, introduite à la fin des années 1980. Il combinait la branche de ressources et la branche de données en un seul fichier binaire, permettant le transfert multiplateforme de fichiers Macintosh.

- **MacBinary II :** Cette version, publiée au début des années 1990, a amélioré le format MacBinary original en ajoutant des informations supplémentaires, telles que le type de fichier et les codes de créateur, à l'en-tête du fichier binaire. Ces codes ont permis de maintenir l'intégrité et l'identification des fichiers Macintosh pendant le transfert.

- **MacBinary III :** Le format MacBinary III, introduit au milieu des années 1990, a encore amélioré les versions précédentes en incluant des métadonnées supplémentaires, telles que le nom du fichier et les dates de création et de modification du fichier, dans l'en-tête du fichier binaire. Cela a permis une préservation plus complète des attributs des fichiers Macintosh pendant le transfert.

- **MacBinary IV :** MacBinary IV a été développé pour résoudre les problèmes de compatibilité avec le système d'exploitation émergent Mac OS X au début des années 2000. Il a incorporé des modifications pour s'adapter à la nouvelle structure et aux nouveaux attributs du système de fichiers introduits dans Mac OS X.

## Comment ouvrir un fichier BIN ?

Les fichiers BIN codés MacBinary peuvent être ouverts à l'aide de divers utilitaires de compression. Pour les utilisateurs de macOS, **Apple Archive Utility** est une option appropriée. Les utilisateurs Windows peuvent utiliser un logiciel tel que **Smith Micro StuffIt Deluxe** pour extraire le contenu d'un fichier BIN codé MacBinary. Une autre option pour les utilisateurs de macOS est **The Unarchiver**, qui est un outil polyvalent capable de gérer plusieurs formats de fichiers, y compris MacBinary.

Il est important de noter que l'extension de fichier .bin est utilisée par différents formats de fichiers, pas seulement MacBinary. Par conséquent, si vous rencontrez un fichier BIN qui ne peut pas être ouvert avec les utilitaires susmentionnés, il peut être enregistré dans un format différent. Dans de tels cas, vous devrez peut-être identifier le format de fichier spécifique et utiliser le logiciel ou l'utilitaire approprié conçu pour ce format pour accéder au contenu du fichier.

## Autres fichiers BIN

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.bin**.

- [BIN - Fichier image de disque binaire](/fr/disc-and-media/bin/)
- [BIN - Fichier exécutable Unix](/fr/executable/bin/)
- [BIN - Fichier de stratégie informatique BlackBerry](/fr/settings/bin/)
- [BIN - ROM du jeu Sega Genesis](/fr/game/bin/)
- [BIN - Image du BIOS PSX PlayStation](/fr/game/bin-pcsx/)

## Les références

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

