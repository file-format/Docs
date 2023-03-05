{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier OSU et les API qui peuvent créer et ouvrir des fichiers OSU.",
  "title" :"Fichier OSU - Format de fichier de script Osu!",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Qu'est-ce qu'un fichier OSU ?

Un fichier OSU est un script de jeu écrit pour osu ! jeu de rythme. Il contient des informations sur une beatmap utilisée dans le jeu, telles que le niveau de difficulté, la chanson à jouer et les horaires des objets touchés avec lesquels le joueur doit se synchroniser avec la musique. Il permet aux joueurs de rythme de développer des défis personnalisés et de les partager avec la communauté du jeu.

**Type MIME du format de fichier OSR :** x-osu-beatmap

## Format de fichier OSU

Les fichiers OSU sont enregistrés sous forme de fichiers texte brut sur le disque et sa structure est très clairement définie dans le [format de fichier OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) par osu!.

### Sections dans le fichier OSU

Un fichier OSU typique comporte les sections suivantes.

|Section |Description |Type de contenu|
---|---|---|
|[Général]| Informations générales sur la beatmap | clé : paires de valeurs |
|[Editeur]| Paramètres enregistrés pour l'éditeur de beatmap | clé : paires de valeurs |
|[Métadonnées] |Informations utilisées pour identifier la beatmap| clé:paires de valeurs|
|[Difficulté] |Paramètres de difficulté| clé:paires de valeurs|
|[Événements]| Événements graphiques beatmap et storyboard | Listes séparées par des virgules |
|[Points de synchronisation]| Chronométrage et points de contrôle| Listes séparées par des virgules |
|[Couleurs]| Combo et couleurs de peau | clé : paires de valeurs|
|[HitObjets]| Frapper des objets| Listes séparées par des virgules |

## Références

* [OSU ! Jeu de rythme](https://osu.ppy.sh/home)
* [Format de fichier OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)

