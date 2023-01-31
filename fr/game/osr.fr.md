{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier OSR et les API qui peuvent créer et ouvrir des fichiers OSR.",
  "title" :"Fichier OSR - osu! Format de fichier de relecture",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Qu'est-ce qu'un fichier OSR ?

Un fichier OSR est un fichier de relecture de jeu créé par [osu! jeu] (https://osu.ppy.sh/home). Osu ! est un jeu de rythme où les utilisateurs associent les clics de souris à la musique. La chanson jouée par l'utilisateur, les succès et les échecs, l'heure et la date de la chanson jouée et le classement général sont enregistrés dans le fichier OSR. Ce fichier OSR peut ensuite être partagé avec d'autres à des fins de relecture. Le fichier OSR nécessite que le fichier beatmap soit présent dans le dossier "Songs".

**Type MIME du format de fichier OSR :** x-osu-replay

## Format de fichier OSR

Les fichiers OSR sont enregistrés sous forme de fichiers binaires avec des champs de données de longueur fixe et variable.

|Type de données| Format|
---|---|
|Byte |Mode de jeu du replay (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Entier |Version du jeu lors de la création du replay (ex. 20131216)|
|Chaîne |osu! beatmap hachage MD5 |
|Chaîne| Nom du joueur|
|Chaîne| osu ! replay MD5 hash (inclut certaines propriétés de la relecture) |
|Court| Nombre de 300 |
|Court| Nombre de 100 en standard, 150 en Taiko, 100 en CTB, 100 en manie|
|Court| Nombre de 50 en standard, petits fruits en CTB, 50 en manie|
|Court| Nombre de Gekis en standard, Max 300s en mania |
|Court| Nombre de Katus en standard, 200s en manie |
|Court| Nombre d'échecs |
|Entier| Score total affiché sur le rapport de score|
|Court| Meilleur combo affiché sur le rapport de score |
|octet| Combo parfait/complet (1 = pas de ratés, pas de pauses de curseur et pas de curseurs terminés en avance) |
|Entier| Modes utilisés. Voir ci-dessous pour la liste des valeurs de mod.|
|Chaîne| Graphique à barres de vie : paires séparées par des virgules u/v, où u est le temps en millisecondes dans la chanson et v est une valeur à virgule flottante de 0 à 1 qui représente la durée de vie que vous avez à un moment donné (0 = la barre de vie est vide, 1= la barre de vie est pleine) |
|Longue| Horodatage (tic de Windows) |
|Entier| Longueur en octets des données de relecture compressées |
|Byte |Tableau Données de relecture compressées|
|Longue| ID de score en ligne|
|Double| Informations supplémentaires sur les mods. Présent uniquement si Target Practice est activé.|

## Références

* [OSU ! Jeu de rythme] (https://osu.ppy.sh/home)
* [Format de fichier OSR] (https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

