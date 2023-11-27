{
"date": "02/02/2023",
  "keywords": [
"fichier d'application",
"qu'est-ce qu'un fichier d'application",
"déposer",
"comment ouvrir le fichier d'application",
"extension de fichier d'application",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
  "description":"Découvrez le format de fichier APP et les API permettant de créer et d'ouvrir des fichiers APP.",
"title": "Format de fichier APP - Ensemble d'applications macOS",
"linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
"parent" : "executable"
}
},
"lastmod": "02/02/2023"
}

## Qu'est-ce qu'un fichier APP ?

Un fichier .app sur macOS est un type spécial de répertoire qui contient tous les fichiers nécessaires à l'exécution d'une application spécifique, y compris le code exécutable, les ressources et les métadonnées. L'extension .app signale au système d'exploitation que ce répertoire doit être traité comme une seule unité, plutôt que comme une collection de fichiers séparés, et qu'il peut être lancé directement depuis le Finder ou le Dock.

Finder est l'application de gestion de fichiers par défaut sur macOS. Il vous permet de parcourir et d'organiser les fichiers et répertoires sur votre ordinateur. Le Dock est une fonctionnalité de macOS qui permet un accès rapide aux applications et documents fréquemment utilisés. Le Finder et le Dock vous permettent de lancer des applications en cliquant sur leurs fichiers .app, ce qui ouvrira le bundle d'applications correspondant. Lorsque vous lancez une application, le code exécutable du bundle .app est exécuté, rendant l'application disponible pour utilisation. Le fichier .app est la représentation de l'application sur le système de fichiers et permet à l'utilisateur d'accéder et de lancer l'application.

Lorsque vous cliquez avec le bouton droit sur un fichier .app dans le Finder sur un système macOS et sélectionnez « Afficher le contenu du package », vous pourrez voir la structure interne du bundle d'applications. Ceci est utile si vous souhaitez accéder aux ressources ou aux fichiers utilisés par l'application, ou si vous souhaitez inspecter le contenu de l'application à des fins de dépannage. Le contenu du package d'un fichier .app inclut généralement des répertoires de ressources telles que des images et des sons, ainsi que le code exécutable de l'application. En explorant le contenu d'un fichier .app, vous pouvez mieux comprendre comment l'application est conçue et ce qu'elle fait.

## Comment ouvrir le fichier APP?

Pour ouvrir un fichier .app sur macOS, double-cliquez simplement sur le fichier dans le Finder. Cela lancera l'application contenue dans le bundle .app. Si l'application est installée sur votre système et a été associée au type de fichier .app, double-cliquez sur le fichier pour démarrer automatiquement l'application. Si l'application n'est pas associée au type de fichier .app, vous devrez peut-être cliquer avec le bouton droit sur le fichier et sélectionner « Ouvrir avec » pour choisir une application appropriée avec laquelle l'ouvrir.

Vous pouvez ouvrir un fichier .app sur le terminal sous macOS en utilisant la commande « ouvrir ». Pour ce faire, accédez au répertoire où se trouve le fichier .app à l'aide de la commande « cd », puis exécutez la commande suivante :

```
open <AppName>.app 
```

où<AppName> est le nom de l'application que vous souhaitez lancer. Cela démarrera l'application comme si vous aviez double-cliqué dessus dans le Finder. La commande « ouvrir » est un utilitaire à usage général qui peut être utilisé pour ouvrir de nombreux types de fichiers différents, notamment des applications, des documents et des répertoires. Lorsque vous utilisez la commande « ouvrir » sur un fichier .app, elle lance l'application contenue dans le bundle.

## Les références
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
