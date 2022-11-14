{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "extension", "fichier", "format", "système", "fichier LNK", "lien", "fichiers LNK", "documents LNK", "application", "programmes" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Format de fichier de lien",
  "description":"En savoir plus sur le format de fichier LNK et les API qui peuvent créer et ouvrir des fichiers LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Qu'est-ce qu'un fichier LNK ? ##

Un fichier LNK, analogue à une identité sur le système Mac, est une alternative Windows ou un "lien" qui sert de connexion à un dossier de document image original ou à un programme. Il contient le type, la position et le nom de fichier de la destination du raccourci, ainsi que l'application qui ouvre le document cible et une touche de raccourci supplémentaire.

Sous Windows, créez un fichier, un dossier ou un programme exécutable et choisissez Créer un raccourci. L'emplacement du format de fichier et le répertoire "Beginning" sont deux caractéristiques de base des fichiers LNK. Le format de fichier des fichiers LNK est masqué et une flèche incurvée indique qu'il s'agit de raccourcis.

## Format de fichier LNK ##

Les formats de fichiers LNK ont généralement la même icône que leurs fichiers de destination, mais avec l'ajout d'une petite flèche recourbée pour montrer que le fichier pointe vers un emplacement différent. Lorsque le raccourci est double-cliqué, il se comporte comme si l'utilisateur avait double-cliqué sur le fichier réel.

Les fichiers LNK contenant des raccourcis d'application peuvent avoir des propriétés qui affectent l'exécution du programme. Pour modifier les attributs, cliquez avec le bouton droit sur le fichier de raccourci et choisissez **Propriétés**, puis modifiez le champ Cible.

Au lieu d'être des extensions de fichiers, les fichiers LNK sont des extensions de l'Explorateur Windows. En tant qu'extension de terminal, les documents .lnk ne peuvent être utilisés que dans l'Explorateur Windows pour remplacer un fichier, et ils ont d'autres objectifs dans l'Explorateur Windows en plus de servir de raccourci vers un document local. Ces fichiers commencent également par la lettre "L".

Bien que les raccourcis soient liés à des fichiers et répertoires spécifiques lors de leur création, ils peuvent devenir inopérants si la cible est modifiée vers un emplacement différent. Explorer commencera à réparer un dossier de raccourcis qui pointe vers une cible morte lorsqu'il est ouvert.


## Spécification technique ##

Ce n'est que lorsque le paramètre d'affichage du dossier "Masquer les extensions pour les types de fichiers reconnus" n'est pas coché que Windows n'affiche pas l'extension de document .lnk pour les raccourcis de document. Bien que cela ne soit pas conseillé, vous pouvez activer l'affichage de l'extension de fichier en supprimant la propriété "NeverShowExt" de l'élément de registre Windows du fichier HKEY_CLASSES_ROOT\lnk.

Pour ce faire, procédez comme suit :

* Ouvrez "Registration Editor" en entrant "Regedit" dans le champ de recherche de la barre des tâches et en choisissant le programme
* Dans l'application, accédez à l'emplacement Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Faites une sauvegarde de l'élément en cliquant dessus avec le bouton droit de la souris et en choisissant Exporter
* Sélectionnez et supprimez l'attribut "NeverShowExt"
* Windows doit être redémarré


## Référence ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
