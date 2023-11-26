{
"date": "07/03/2023",
  "keywords": [
"fichier regtrans-ms",
"qu'est-ce qu'un fichier regtrans-ms",
"déposer",
"extension de fichier regtrans-ms",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier REGTRANS-MS - Fichier journal des transactions du registre",
  "description":"Découvrez le format REGTRANS-MS et les API permettant de créer et d'ouvrir des fichiers REGTRANS-MS.",
"linktitle": "REGTRANS-MS",
  "menu": {
    "docs": {
      "identifier": "system-regtrans-ms",
"parent": "système"
}
},
"derniermod": "07/03/2023"
}

## Qu'est-ce qu'un fichier REGTRANS-MS ?

REGTRANS-MS est un type de fichier associé au registre Windows. Il s'agit d'un fichier journal des transactions utilisé par Registry Transaction Manager pour suivre les modifications apportées au registre. Le Registry Transaction Manager est un composant du système d'exploitation Windows qui permet de garantir la cohérence et l'intégrité du registre.

Le fichier REGTRANS-MS est créé lorsqu'une modification est apportée au registre et contient des informations sur la modification, telles que la clé qui a été modifiée, la valeur qui a été ajoutée ou supprimée et le type de modification apportée. Le fichier est utilisé par Registry Transaction Manager pour suivre les modifications en attente dans le registre et pour annuler les modifications si nécessaire.

En général, le fichier REGTRANS-MS n'est pas destiné à être ouvert ou modifié directement par les utilisateurs. Il s'agit d'un fichier système géré par le système d'exploitation et il se trouve généralement dans le dossier `%SystemRoot%\System32\Config\TxR` sur le lecteur système.

Si vous rencontrez des problèmes avec le fichier REGTRANS-MS ou le Registry Transaction Manager, vous pouvez suivre quelques étapes de dépannage, telles que l'exécution d'une analyse du vérificateur de fichiers système, la recherche de logiciels malveillants ou de virus ou la restauration du système à un point de restauration précédent. . Il n'est généralement pas recommandé de supprimer ou de modifier manuellement le fichier REGTRANS-MS, car cela pourrait entraîner des problèmes avec le registre et la stabilité du système d'exploitation.

## Format de fichier REGTRANS-MS - Plus d'informations

Le Registry Transaction Manager est un composant du système d'exploitation Windows qui gère les transactions vers le registre Windows. Le registre Windows est une base de données hiérarchique qui stocke les paramètres et options de configuration du système d'exploitation Windows et des applications installées.

Le gestionnaire de transactions de registre garantit la cohérence et l'intégrité du registre en suivant les modifications apportées au registre et en fournissant un moyen d'annuler les modifications si nécessaire. Pour ce faire, il crée des journaux de transactions, qui sont stockés dans le dossier `%SystemRoot%\System32\Config\TxR` sur le lecteur système. Les journaux de transactions sont enregistrés dans des fichiers portant les extensions de fichier « .log » et « .jrs », et un fichier « REGTRANS-MS » est utilisé pour suivre les transactions en attente.

Lorsque des modifications sont apportées au registre, le gestionnaire de transactions du registre écrit les modifications dans les fichiers journaux des transactions et dans le fichier REGTRANS-MS. Si une transaction n'est pas terminée ou est interrompue, la transaction peut être annulée en utilisant les informations contenues dans les fichiers journaux des transactions et le fichier REGTRANS-MS.

Le gestionnaire de transactions de registre est un élément important du système d'exploitation Windows et contribue à garantir la stabilité et la fiabilité du système. Cependant, s'il y a des problèmes avec le fichier REGTRANS-MS ou les fichiers journaux des transactions, cela peut entraîner des problèmes avec le registre et le système d'exploitation. Dans certains cas, il peut être nécessaire de supprimer les fichiers journaux des transactions et le fichier REGTRANS-MS pour résoudre les problèmes liés au registre. Toutefois, cela ne doit être fait qu’en dernier recours et sous la direction d’un technicien qualifié.

## Puis-je supprimer le fichier REGTRANS-MS ?

La suppression de ce fichier peut entraîner des erreurs ou des problèmes avec le système d'exploitation ou les logiciels installés. Il est possible que vous rencontriez également des problèmes de stabilité, de performances ou de fonctionnalités du système. Cependant, les fichiers regtrans-ms créés avant le dernier démarrage du système peuvent être supprimés en toute sécurité.

## Les références
* [Registre Windows](https://en.wikipedia.org/wiki/Windows_Registry)

