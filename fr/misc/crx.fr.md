{
"date": "08/06/2023",
  "keywords": [
"fichier crx",
"qu'est-ce qu'un fichier crx",
"comment installer le fichier crx dans Google Chrome",
"comment ouvrir le fichier crx",
"que contient le fichier crx",
"quel est le format du fichier crx",
"déposer",
"extension de fichier crx",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier CRX - Extension Google Chrome",
  "description":"Découvrez le format CRX et les API permettant de créer et d'ouvrir des fichiers CRX.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent" : "misc"
}
},
"lastmod": "2023-06-08"
}

## Qu'est-ce qu'un fichier CRX ?

Le format de fichier CRX est associé aux extensions du navigateur Google Chrome. Un fichier CRX est essentiellement un package compressé contenant les fichiers et métadonnées nécessaires pour qu'une extension soit installée et exécutée dans Google Chrome. Il améliore la fonctionnalité ou l'apparence d'un navigateur Web en fournissant une fonctionnalité ou un thème supplémentaire.

Lorsqu'un fichier CRX est téléchargé et installé dans Google Chrome, le navigateur vérifie l'intégrité de l'extension à l'aide de la clé publique et de la signature. Si la vérification réussit, Chrome extrait le contenu du fichier CRX et installe l'extension, le rendant ainsi disponible. Les utilisateurs peuvent gérer leurs extensions via la page Chrome Extensions, qui permet d'activer, de désactiver ou de supprimer les extensions installées.

## Comment installer le fichier CRX dans Google Chrome ?

Pour installer un fichier CRX dans Google Chrome, vous pouvez suivre ces étapes :

1. Ouvrez le navigateur Chrome.
2. Tapez « chrome://extensions » dans la barre d'adresse et appuyez sur Entrée.
3. Activez le commutateur à bascule « Mode développeur » situé dans le coin supérieur droit de la page Extensions.
4. Cliquez sur le bouton "Charger décompressé".
5. Localisez et sélectionnez le dossier contenant le contenu extrait du fichier CRX (ou sélectionnez simplement le fichier CRX lui-même).
6. Cliquez sur "Ouvrir" pour installer l'extension.

## Que contient le fichier CRX ?

Un fichier CRX contient les fichiers et métadonnées nécessaires requis pour l'extension Google Chrome. Voici une répartition du contenu typique trouvé dans un fichier CRX :

- **Fichier manifeste (manifest.json) :** Ce fichier est un fichier au format JSON qui inclut des informations sur l'extension telles que son nom, sa version, sa description, ses autorisations et ses scripts d'arrière-plan. Il définit la structure et le comportement de l'extension.
- **Fichiers JavaScript :** Ces fichiers contiennent le code qui définit la fonctionnalité de l'extension. Ils peuvent inclure des scripts permettant de gérer des événements, de modifier des pages Web ou d'interagir avec les API de Chrome.
- **Fichiers HTML, CSS et image :** Les extensions incluent souvent des éléments d'interface utilisateur, tels que des fenêtres contextuelles ou des pages d'options. Les fichiers HTML définissent la structure de ces interfaces, tandis que les fichiers CSS contrôlent leur apparence. Les fichiers image sont utilisés pour les icônes ou d’autres éléments graphiques.
- **Fichiers de ressources facultatifs :** Les extensions peuvent inclure des ressources supplémentaires, telles que des fichiers de localisation pour la prise en charge de plusieurs langues. Ces fichiers contiennent des traductions du texte utilisé dans l'interface utilisateur de l'extension.
- **Scripts d'arrière-plan :** Si une extension comporte des processus ou des scripts en arrière-plan qui s'exécutent indépendamment de la page Web active, ces scripts seront inclus dans le fichier CRX.
- **Scripts de contenu :** Les scripts de contenu sont des scripts qui peuvent être injectés dans des pages Web pour modifier leur comportement ou interagir avec leur contenu. Si l'extension utilise des scripts de contenu, les fichiers nécessaires à ces scripts seront présents dans le fichier CRX.
- **Autres éléments :** En fonction des exigences spécifiques de l'extension, des fichiers supplémentaires tels que des fichiers audio ou vidéo, des polices ou des fichiers de données peuvent être inclus.

Le format de fichier CRX est essentiellement un package compressé qui contient tous ces fichiers et dossiers de manière structurée. Lorsque le fichier CRX est installé dans Google Chrome, le navigateur extrait le contenu et le place aux emplacements appropriés, permettant ainsi à l'extension d'être chargée et exécutée dans le navigateur.

## Quel est le format du fichier CRX ?

Le format de fichier CRX est un format spécifique pour l'empaquetage et la distribution des extensions Google Chrome. Il s'agit essentiellement d'une archive ZIP compressée avec une extension de fichier différente. La structure de base du fichier CRX est la suivante :

- **Signature du fichier :** Les 4 premiers octets du fichier contiennent le nombre magique "Cr24" (hexadécimal : 43 72 32 34) qui sert de signature pour identifier le fichier comme fichier CRX.
- **Numéro de version :** Les 4 octets suivants représentent le numéro de version du format CRX.
- **Longueur de la clé publique :** Les 4 octets suivants indiquent la longueur de la clé publique codée utilisée pour la vérification de la signature d'extension.
- **Longueur de la signature :** Les 4 octets suivants spécifient la longueur de la signature de l'extension.
- **Clé publique :** Cette section contient la clé publique codée utilisée pour vérifier l'intégrité de l'extension.
- **Signature :** Cette section contient la signature de l'extension, qui est générée en signant le contenu de l'extension à l'aide d'une clé privée correspondant à la clé publique mentionnée ci-dessus.
- **Archive ZIP :** Les octets restants du fichier CRX comprennent une archive ZIP compressée. Cette archive contient tous les fichiers et dossiers d'extension nécessaires, y compris le fichier manifeste, les fichiers JavaScript, les fichiers HTML, les fichiers CSS, les images et toute autre ressource.

## Les références
* [Spécification du format CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

