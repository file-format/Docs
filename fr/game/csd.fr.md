{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format et les API du fichier de sauvegarde des données de jeu CSD Steam.",
  "title" :"Format de fichier CSD - Fichier de sauvegarde des données de jeu Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Qu'est-ce qu'un fichier CSD ?

Un fichier CSD est un fichier de sauvegarde de jeu généré par le service de jeu **Steam** qui permet aux utilisateurs de télécharger et de gérer les jeux **Valve**. Il contient les données de sauvegarde liées aux jeux qui peuvent être utilisées pour restaurer un jeu supprimé. Steam ne peut restaurer le jeu à partir d'un fichier CSD que si le jeu a été téléchargé, installé et corrigé via Steam. Pour restaurer le jeu à partir d'un fichier CSD, utilisez l'option Steam → Sauvegarder et restaurer Gamesteam et sélectionnez le fichier.

## Format de fichier CSD - Plus d'informations

La structure interne du format de fichier CSD n'est pas disponible publiquement et ses spécifications de format de fichier ne sont pas disponibles pour la référence du développeur. Les fichiers CSD sont accompagnés des fichiers CSM et ISS qui sont également des formats de fichiers de jeu Steam.

### Où trouver les fichiers de sauvegarde Steam ?

L'intégralité des fichiers de sauvegarde Steam se trouve aux emplacements suivants :

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Configurations personnalisées et scripts de configuration
* \downloads\ - Contenu personnalisé pour les jeux multijoueurs
* \maps\ - Cartes personnalisées qui ont été installées ou téléchargées pendant les parties multijoueurs
* \materials\ - Textures et habillages personnalisés
* \SAVE\ - Parties sauvegardées pour un joueur

Cependant, l'emplacement des jeux créés par des tiers peut être différent et est déterminé par le développeur du jeu.

### Restauration à partir du fichier de sauvegarde CSD

Installez Steam et connectez-vous au bon compte Steam (voir Installer Steam pour plus d'instructions)
* Lancer Steam
* Cliquez sur "Steam" dans le coin supérieur gauche de l'application Steam
* Sélectionnez "Sauvegarder et restaurer les jeux..."
* Sélectionnez "Restaurer une sauvegarde précédente"
* Accédez à l'emplacement des fichiers de sauvegarde du jeu
* Continuez à travers les fenêtres Steam pour installer les jeux nécessaires.

## Références

* [Utilisation de la fonction de sauvegarde Steam](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

