{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Périphérique eBook Rocket de Nuvo Media", "fichier", "extension", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier RB pour l'appareil Rocket eBook de Nuvo Media et les API qui peuvent créer et ouvrir des fichiers RB.",
  "title" :"RB - Fichier de livre électronique Rocket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Qu'est-ce qu'un fichier RB ?

Le fichier avec l'extension .rb contient le contenu du Rocket eBook. Le Rocket eBook est en fait un appareil fabriqué par Nuvo Media ; ils ont sorti cet appareil en 1998. Bien que Rocket eBook soit capable d'afficher des images, mais uniquement en noir et blanc. Il dispose d'un écran de 106 dpi soit 480 x 320 pixels sur une dalle tactile de 4,5 x 3 pouces. Le Rocket eBook se connecte à un ordinateur via une connexion de port série pour télécharger des eBooks au format de fichier RB. Les fichiers RB sont capables d'utiliser DRM mais cette technologie n'est pas utilisée dans les livres électroniques modernes. Le fichier RB contient classiquement un fichier HTML avec les images et un fichier pseudo-OPF avec l'ensemble des métadonnées (.info).

## Spécification technique du format de fichier RB ##

Un nombre magique (en hexadécimal) apparaît dans les 4 premiers octets du fichier : B0 0C B0 0C.

Il semble que les deux octets suivants soient un numéro de version, comme "02 00", qui signifie version majeure 2 et version mineure 0.

Les quatre octets suivants contiennent le texte "NUVO", suivi de 4 octets de 00h.

Les 4 octets suivants correspondent à la date de création du livre, encodée en int16. Cela nous met à l'offset 0Eh. L'ancienne version d'ORocketLibrary encodait la valeur complète de l'année (par exemple, 1999 était "CF 07", 2000 était "D0 07"). Dans la version récente, tm_year est stocké textuellement, c'est-à-dire 100 pour l'année 2000 ("64 00"). Après l'année vient un int8 représentant le numéro de mois relatif à 1 et un int8 représentant le jour du mois.

Les 6 octets suivants sont 00h. Pour le réglage de l'heure, ceux-ci peuvent être réservés.

Le décalage absolu de la "Table des matières" est contenu dans un int32 au décalage 18h.

Après c'est un int32 contenant la longueur du fichier .rb. Ceci est utilisé pour déterminer si les fichiers sont complets ou non.

Ce bloc entier d'octets (20h à 128h) semble n'être nécessaire qu'à un titre crypté. Dans les titres non cryptés, ils sont toujours nuls.

Dans la plupart des cas, la table des matières suit (au décalage 128). Il commence par un décompte int32 du nombre d'entrées "page" (sections de fichier .rb) dans la table des matières. Chaque entrée se compose d'un nom (remplissage de zéros à 32 octets), suivi de 3 int32 : la longueur du segment de données, la position dans le fichier .rb et un indicateur pour cette entrée. A ce jour, les valeurs connues sont : 1 (chiffré), 2 (page d'informations) et 8 (dégonflé). Les noms sont tous adaptés, si nécessaire, pour s'assurer qu'ils sont tous uniques.

## Références

* [E-Reader - Par MobileRead](https://en.wikipedia.org/wiki/E-reader)

