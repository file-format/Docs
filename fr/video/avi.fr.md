{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Vidéo audio compressée", "Fichier", "Extension", "Format de fichier", "Conteneur multimédia", "XVid", "DivX", "Codecs", "Format de fichier d'échange de ressources", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier AVI - Un fichier audio vidéo entrelacé",
  "description":"En savoir plus sur le format de fichier AVI et les API qui peuvent créer et ouvrir des fichiers AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Qu'est-ce qu'un fichier AVI ? ##

Le format de fichier **AVI** est un format de fichier conteneur multimédia audio vidéo introduit par Microsoft. Il contient les données audio et vidéo créées et compressées à l'aide de plusieurs codecs (codeurs/décodeurs) tels que **XVid** et **DivX**. Étant donné que différents codecs peuvent être utilisés pour encoder le contenu AVI, les applications de récupération, c'est-à-dire les lecteurs AVI, ne devraient pouvoir les ouvrir que si elles disposent des codecs requis avec lesquels les contenus AVI ont été créés. Le format est pris en charge par défaut sur toutes les plates-formes **Microsoft Windows** ainsi que sur presque toutes les autres plates-formes majeures. Plusieurs applications et API offrent la possibilité de créer/sauvegarder, lire et convertir AVI vers d'autres formats populaires tels que MP4, MOV, WMV, etc.

## Format de fichier AVI ##

Un fichier ayant une extension .avi est un fichier AVI. C'est un sous-format du format RIFF (Resource Interchange File Format). RIFF organise les données en blocs, ou "morceaux", qui sont identifiés par une balise FourCC. Un fichier AVI est simplement un "morceau" dans un fichier au format RIFF.

Dans le premier sous-morceau, l'en-tête du fichier est identifié par la balise "hdrl" ; son contenu comprend la largeur, la hauteur et la fréquence d'images de la vidéo. Dans le deuxième sous-bloc, la balise de mouvement représente la fréquence d'images de la vidéo. La vidéo AVI est composée des données audio/visuelles réelles de ce bloc. Il existe également un troisième sous-bloc facultatif avec la balise "idx1", qui indique la position dans le fichier des blocs de données individuels qui appartiennent au fichier.

### Limites ###

* Les informations de format d'image ne peuvent pas être encodées dans la spécification AVI d'origine, bien que la dernière spécification OpenDML (AVI 2.0) offre une méthode standardisée
* Bien que les fichiers AVI soient largement utilisés dans la post-production cinématographique et télévisuelle, diverses approches pour leur ajouter un code temporel sont en concurrence, ce qui affecte la convivialité du format.
* Un fichier vidéo encodé en AVI ne peut pas utiliser une technique de compression qui nécessite des données d'images futures au-delà de l'image en cours d'encodage (trame B)
* Il est problématique d'utiliser des fichiers AVI avec des débits binaires variables (VBR) (tels que l'audio MP3 à des taux d'échantillonnage inférieurs à 32 kHz)
* Un fichier AVI encodant des longs métrages en définition standard tels qu'ils sont normalement utilisés est susceptible d'entraîner une surcharge d'environ 5 Mo par heure, selon la manière dont le fichier est utilisé
* Les sous-titres doivent être codés en dur dans le flux vidéo ou distribués dans un fichier séparé au cas où les fichiers AVI ne peuvent pas accepter les pièces jointes telles que les polices et les sous-titres

## Bref historique ##

AVI a été introduit par Microsoft en 1992 dans le but de fournir un format de fichier audio et vidéo plus robuste et avancé. Le format est rapidement devenu populaire avec l'utilisation d'Internet, permettant aux individus de partager des fichiers vidéo directement et indirectement via un stockage multimédia basé sur le cloud.

## Références ##

* [AVI - Par Wikipédia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

