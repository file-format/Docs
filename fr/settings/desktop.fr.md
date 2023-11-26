{
"date": "2023-05-31",
  "keywords": [
"fichier de bureau",
"qu'est-ce qu'un fichier de bureau",
"que contient le fichier de bureau",
"exemple de fichier de bureau",
"comment ouvrir le fichier du bureau",
"quel est le format du fichier de bureau",
"déposer",
"extension de fichier de bureau",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier DESKTOP - Fichier d'entrée de bureau",
  "description":"Découvrez le format DESKTOP et les API permettant de créer et d'ouvrir des fichiers DESKTOP.",
"linktitle": "BUREAU",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent": "paramètres"
}
},
"lastmod": "2023-05-31"
}

## Qu'est-ce qu'un fichier BUREAU ?

Un fichier .desktop est un fichier de configuration utilisé par les environnements de bureau Linux pour définir des raccourcis et des lanceurs d'applications. Il fournit des métadonnées sur une application telles que son nom, son icône, la commande à exécuter et d'autres propriétés. Ces fichiers sont généralement utilisés pour créer des raccourcis dans les menus d'applications, les lanceurs de bureau ou les panneaux des systèmes Linux.

## Que contient le fichier DESKTOP ?

Un fichier .desktop suit un format spécifique et contient plusieurs champs clés :

- **[Desktop Entry] :** Il s'agit de l'en-tête de section principale du fichier .desktop.
- **Nom :** Spécifie le nom de l'application.
- **Commentaire :** Fournit une brève description ou un commentaire sur l'application.
- **Exec :** Définit la commande à exécuter lors du lancement de l'application.
- **Icône :** Spécifie le chemin d'accès au fichier icône associé à l'application.
- **Terminal :** Spécifie si l'application doit être exécutée dans une fenêtre de terminal.
- **Type :** Spécifie le type d'entrée tel que « Application » ou « Lien ».
- **Catégories :** Spécifie les catégories ou groupes sous lesquels l'application doit être affichée dans le menu.
- **StartupNotify :** Spécifie si l'environnement de bureau doit afficher une notification de démarrage pour l'application.
- **NoDisplay :** Spécifie si l'application doit être masquée dans les menus.
- **Actions :** Définit des actions supplémentaires pouvant être effectuées sur l'application, telles que l'ouverture d'un fichier spécifique.

## Exemple de fichier BUREAU

Voici un exemple de fichier .desktop pour un éditeur de texte fictif appelé « MyTextEditor » :

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Dans cet exemple, le fichier .desktop définit l'application « MyTextEditor » avec ses propriétés associées. Il comprend également deux actions supplémentaires, « Ouvrir une nouvelle fenêtre » et « Ouvrir un fichier existant », accessibles à partir du menu contextuel du lanceur d'applications.

En plaçant un fichier .desktop dans des répertoires spécifiques tels que `/usr/share/applications` ou `~/.local/share/applications`, l'environnement de bureau le reconnaîtra et affichera l'application en conséquence dans les menus ou lui permettra d'être lancée depuis bureau.

## Comment ouvrir le fichier DESKTOP?

Plusieurs logiciels peuvent ouvrir et gérer les fichiers .desktop. Ces programmes sont généralement des gestionnaires de fichiers ou des environnements de bureau sur des systèmes Linux. Voici quelques exemples:

- **Nautilus (Fichiers) :** Le gestionnaire de fichiers par défaut pour l'environnement de bureau GNOME.
- **Nemo :** Le gestionnaire de fichiers pour l'environnement de bureau Cinnamon.
- **Dolphin :** Le gestionnaire de fichiers par défaut pour l'environnement de bureau KDE Plasma.
- **Thunar :** Le gestionnaire de fichiers par défaut pour l'environnement de bureau Xfce.
- **Éditeur de menu KDE :** Un outil spécifique à l'environnement de bureau KDE Plasma qui vous permet d'afficher et de modifier des fichiers .desktop.

Ces gestionnaires de fichiers et environnements de bureau fournissent une interface graphique pour gérer les fichiers .desktop. Ils vous permettent d'afficher et de modifier les propriétés des fichiers .desktop, de créer des lanceurs d'applications et d'organiser des raccourcis dans les menus d'application ou sur le bureau.

Les fichiers .desktop sont des fichiers texte brut, vous pouvez donc également les ouvrir et les modifier avec un éditeur de texte de votre choix. Faites simplement un clic droit sur le fichier .desktop et sélectionnez « Ouvrir avec » ou « Ouvrir avec une autre application » pour choisir un éditeur de texte dans la liste des programmes installés.

## Quel est le format du fichier DESKTOP ?

Le format de fichier .desktop suit une structure et un format spécifiques. Il s'agit d'un fichier texte brut avec un ensemble de paires clé-valeur organisées en sections. Voici un aperçu du format :

- **En-têtes de section :** Chaque section commence par un en-tête entre crochets ([]). La section principale est généralement nommée [Desktop Entry] et contient les principales métadonnées de l'application ou du lanceur.
- **Paires clé-valeur :** Dans chaque section, vous définissez des propriétés à l'aide de paires clé-valeur. Le format est "Clé=Valeur". La clé identifie la propriété et la valeur fournit les données correspondantes.
- **Syntaxe des propriétés :** Les valeurs des propriétés peuvent être de différents types, notamment des chaînes, des valeurs booléennes, des chemins de fichiers ou des listes. Le format de chaque valeur de propriété dépend de son type.
- **Commentaires :** Vous pouvez inclure des commentaires dans le fichier .desktop en utilisant le symbole « # ». Tout ce qui suit « # » en ligne est considéré comme un commentaire et est ignoré.

## Les références
* [Fichiers d'entrée de bureau](https://www.baeldung.com/linux/desktop-entry-files)

