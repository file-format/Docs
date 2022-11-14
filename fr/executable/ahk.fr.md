{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier AHK et les API qui peuvent créer et ouvrir des fichiers AHK.",
  "title" :"Format de fichier AHK - Fichier de script AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Qu'est-ce qu'un fichier AHK ?

Un fichier AHK est un fichier de script généré avec l'application logicielle AutoHotkey qui est utilisé pour l'automatisation des tâches dans Microsoft Windows. Il contient des instructions pour l'automatisation des tâches à l'aide de touches de raccourci qui peuvent être utilisées pour effectuer des actions instantanées. Le fichier est exécuté par AutoHotkey et toutes les actions sont effectuées de manière séquentielle. Les fichiers AHK sont suffisamment puissants pour effectuer des tâches complexes à l'aide des raccourcis clavier définis à l'aide des raccourcis clavier. Les fichiers AHK peuvent être ouverts avec des éditeurs de texte tels que Microsoft Notepad et Notepad++.

## Format de fichier AHK

Les fichiers AHK sont enregistrés sur le disque sous forme de fichiers texte brut et contiennent des lignes de code pouvant être exécutées par AutoHotkey. AutoHotkey est un langage de script gratuit et open source qui permet aux utilisateurs de créer des scripts simples à complexes pour effectuer des actions telles que remplir des formulaires, cliquer automatiquement, exécuter des macros, etc. Un fichier AHK au minimum peut effectuer une seule action puis quitter .

Il existe des outils disponibles qui peuvent être utilisés pour convertir AHK en fichiers [Exe](/fr/executable/exe/).

### Exemple AHK

L'exemple suivant utilise la touche Win+Z pour exécuter le Bloc-notes Microsoft ou le mettre au premier plan s'il est déjà en cours d'exécution.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Comment créer un fichier AHK ?

Les étapes suivantes peuvent être utilisées pour créer un fichier AHK. Ceux-ci supposent qu'AutoHotkey est déjà installé sur la machine.

* Faites un clic droit sur votre bureau.
* Trouvez "Nouveau" dans le menu.
* Cliquez sur "AutoHotkey Script" dans le menu "Nouveau".
* Donnez un nouveau nom au script.
* Trouvez le fichier nouvellement créé sur votre bureau et faites un clic droit dessus.
* Cliquez sur "Modifier le script".
* Une fenêtre devrait apparaître, probablement le Bloc-notes.
* Enregistrez le fichier.

## Références

* [AutoHotkey] (https://www.autohotkey.com/)
* [Fichier batch - par Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

