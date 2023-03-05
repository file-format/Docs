{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier MDMP - Format de fichier Windows Minidump",
  "description":"En savoir plus sur le format de fichier MDMP et les API qui peuvent créer et ouvrir des fichiers MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Qu'est-ce qu'un fichier MDMP ?

Un fichier MDMP est un vidage mémoire d'une application sur Microsoft Windows qui est créé lorsque l'application se ferme anormalement ou se bloque. Il contient des informations et des vidages de données qui peuvent être utilisés pour déboguer la cause du crash. Les fichiers MDMP sont applicables sur les applications créées par n'importe quelle plate-forme telle que Java, C++, .NET et autres. En plus du MDMP,

Les applications qui peuvent ouvrir les fichiers MDMP incluent Microsoft Visual Studio Debugger.

## Format de fichier MDMP

Les fichiers MDMP sont enregistrés sous forme de fichiers binaires sur le disque et peuvent être ouverts avec le débogueur Microsoft Visual Studio. Il contient les informations suivantes pour vous aider à identifier la raison de l'incident.

* Détails du message d'arrêt, de ses paramètres et d'autres données
* Liste des pilotes chargés
* Contexte du processeur (PRCB) pour le processeur qui a cessé de fonctionner
* Informations sur le processus et contexte du noyau (EPROCESS) pour le processus qui s'est arrêté
* Traiter les informations et le contexte du noyau (ETHREAD) pour le thread qui s'est arrêté
* Pile d'appels en mode noyau pour le thread qui s'est arrêté

Ces informations permettent de découvrir ce qui s'est passé, de résoudre le problème et d'éviter qu'il ne se reproduise.

### Analyser le minidump

Windows nécessite un fichier d'échange sur le volume de démarrage pour créer un fichier de vidage mémoire. Le fichier d'échange est créé sur le volume de démarrage et doit avoir une taille d'au moins 2 mégaoctets (Mo). Le fichier de vidage est créé lorsqu'une application plante. En cas de deuxième problème, un deuxième petit fichier de vidage mémoire est créé tandis que le précédent est conservé. Le nom du fichier de vidage est distinct pour éviter tout écrasement.

Windows conserve une liste de tous les fichiers de vidage mémoire dans le dossier %SystemRoot%\Minidump. Vous pouvez analyser les fichiers MDMP en les exécutant dans Visual Studio Debugger comme indiqué dans les étapes ci-dessous.

## Comment ouvrir un fichier MDMP dans Visual Studio ?

Les étapes suivantes peuvent être utilisées pour ouvrir un fichier MDMP dans Visual Studio.

* Dans Visual Studio, dans le menu Fichier, choisissez Ouvrir | Vidage sur incident .
* Accédez au fichier de vidage que vous souhaitez ouvrir.
* Sélectionnez Ouvrir.

## Référence

* [Comment lire le petit fichier de vidage de la mémoire créé par Windows en cas de plantage](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -dossier)

