{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier Torrent - Fichier BitTorrent",
  "description":"En savoir plus sur les fichiers TORRENT et les API qui peuvent créer et ouvrir des fichiers TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Qu'est-ce qu'un fichier TORRENT ?

Un fichier TORRENT est un fichier texte utilisé par BitTorrent et d'autres programmes P2P (peer-to-peer) pour le téléchargement et l'échange de contenu. Le contenu téléchargeable peut inclure des documents, des vidéos, des jeux, des films et d'autres médias disponibles sur Internet. Il comprend des informations de métadonnées sur le contenu et l'emplacement du média à télécharger. Un logiciel comme BitTorrent utilise les informations de ce fichier telles que le nom, la taille du fichier et la structure du dossier pour le téléchargement des données. Les fichiers torrent peuvent être convertis en d'autres formats de fichiers tels que [PDF](/fr/pdf/) en ligne.

## Qu'est-ce que le Torrent ? Le format de fichier TORRENT pour l'échange de données

Le torrenting est le concept d'échange (téléchargement et envoi) de fichiers de données utilisant le réseau BitTorrent. Contrairement aux serveurs conventionnels où les données sont téléchargées pour que d'autres puissent y accéder et les télécharger, les fichiers torrent sont récupérés et envoyés à l'aide du réseau torrent. Lorsqu'un utilisateur ouvre un fichier .torrent dans des applications telles que BitTorrent, le logiciel commence à télécharger le contenu du fichier au niveau du bit. Si plusieurs utilisateurs ont le même fichier, BitTorrent répartit les téléchargements entre tous les utilisateurs pour accélérer le processus de téléchargement. En même temps, l'ordinateur de l'utilisateur qui télécharge le fichier devient également la source du fichier pour l'envoyer à d'autres utilisateurs qui téléchargent également le même fichier.

### Structure d'un fichier TORRENT

Un fichier torrent est une combinaison d'une liste de fichiers et d'informations de métadonnées sur tous les éléments du fichier à télécharger. Il contient les informations suivantes sous forme de clés.

- `announce` - L'URL du tracker qui est annoncée aux autres pairs pour informer de la disponibilité du fichier
- `info` — Correspond à un dictionnaire dont les clés dépendent du fait qu'un ou plusieurs fichiers sont partagés :
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — taille du fichier en octets.
- `path` - une liste de chaînes correspondant aux noms de sous-répertoires, dont le dernier est le nom de fichier réel
- `length` - la taille du fichier en octets (uniquement lorsqu'un fichier est partagé)
- `name` — nom de fichier où le fichier doit être enregistré
- `longueur de morceau` — nombre d'octets par morceau. C'est généralement 28 KiB = 256 KiB = 262 144 B.
- `pieces` — une liste de hachage qui est une concaténation du hachage SHA-1 de chaque morceau.

## Le torrenting est-il sûr et légal ?

Le protocole de torrenting pour l'échange de données entre utilisateurs P2P est sûr car c'est juste le moyen de partager n'importe quel type de fichier. Ainsi, le protocole lui-même n'est ni dangereux ni illégal. Cependant, le contenu partagé via le réseau peut contenir des fichiers ou des médias qui peuvent violer le statut juridique des documents partagés. Dans ce cas, l'échange de ces données peut entraîner des actions en justice contre les parties impliquées dans le partage public de ces fichiers.

## Références

* [Fichier TORRENT - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

