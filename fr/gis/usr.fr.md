{
"date": "03/08/2023",
  "keywords": [
"usr",
"fichier usr",
"qu'est-ce qu'un fichier usr",
"comment ouvrir le fichier usr",
"déposer",
"extension de fichier usr",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier USR - Fichier de données GPS Lowrance",
  "description":"Découvrez le format USR et les API permettant de créer et d'ouvrir des fichiers USR.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
"parent" : "gis"
}
},
"lastmod": "2023-08-03"
}

## Qu'est-ce qu'un fichier USR ?

L'extension de fichier « .usr » est également liée aux appareils GPS Lowrance. En particulier, il est utilisé pour stocker les données GPS dans un format connu sous le nom de « Format de données utilisateur » (format USR) qui est utilisé par les appareils GPS Lowrance.

Lorsque vous utilisez un appareil GPS Lowrance, vous pouvez enregistrer vos waypoints, tracés et itinéraires sous forme de fichiers « .usr ». Ces fichiers contiennent généralement des informations telles que la latitude, la longitude, l'altitude, l'horodatage et d'autres données liées à vos activités GPS.

Voici quelques utilisations courantes des fichiers .usr avec les appareils GPS Lowrance :

- **Waypoints :** Les waypoints sont des emplacements spécifiques marqués sur le GPS, tels que des points de repère, des lieux de pêche préférés ou des points d'intérêt. Vous pouvez enregistrer ces emplacements sous forme de fichiers .usr et ils peuvent être importés, exportés ou partagés avec d'autres utilisateurs de GPS Lowrance.

- **Pistes :** Les pistes représentent le chemin enregistré de vos mouvements GPS. Vous pouvez enregistrer vos journaux de suivi sous forme de fichiers .usr, ce qui vous permet de consulter et d'analyser vos itinéraires ultérieurement ou de les partager avec d'autres.

- **Itinéraires :** Les itinéraires sont des chemins prédéfinis que vous pouvez créer et enregistrer sur votre appareil GPS. Ces itinéraires peuvent également être enregistrés sous forme de fichiers .usr pour une utilisation ou un partage ultérieur.

Pour gérer les fichiers .usr sur votre appareil GPS Lowrance, vous utilisez généralement un logiciel tel que « Insight Planner » ou « Lowrance GPS Utility » de Lowrance pour importer, exporter et manipuler vos données GPS.

## Format de fichier USR - Plus d'informations

Dans les appareils GPS Lowrance iFinder, les fichiers .usr sont créés et enregistrés sur la carte mémoire MultiMediaCard (MMC) insérée dans l'appareil. Ces fichiers contiennent des données utilisateur telles que des waypoints, des traces et des itinéraires.

Pour transférer les fichiers .usr de la MMC vers un ordinateur, vous pouvez suivre ces étapes :

- **Retirez la MMC :** Retirez délicatement la MultiMediaCard (MMC) du périphérique GPS Lowrance iFinder.

- **Insérez MMC dans l'ordinateur :** Utilisez un lecteur de carte MMC approprié pour insérer la carte mémoire dans l'emplacement du lecteur de carte de votre ordinateur.

- **Localiser les fichiers .usr :** Une fois la MMC reconnue par votre ordinateur, vous devriez pouvoir accéder aux fichiers qui y sont stockés. Recherchez les fichiers .usr qui contiennent vos données GPS.

- **Conversion avec GPSBabel :** Pour convertir les fichiers .usr dans un autre format GPS, vous pouvez utiliser GPSBabel, qui est un outil gratuit et open source permettant de travailler avec différents formats de fichiers GPS. GPSBabel prend en charge une large gamme de formats d'entrée et de sortie, vous permettant de convertir les fichiers .usr en formats compatibles avec d'autres logiciels ou appareils GPS.

Vous pouvez télécharger GPSBabel depuis le site officiel (http://www.gpsbabel.org/) et l'installer sur votre ordinateur. Une fois installé, vous pouvez utiliser l'interface de ligne de commande du logiciel ou l'interface utilisateur graphique (si disponible) pour effectuer la conversion.

Par exemple, si vous souhaitez convertir des fichiers .usr au format GPX, vous pouvez utiliser une commande telle que :

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

La commande ci-dessus demande à GPSBabel de lire le fichier d'entrée "input.usr" au format Lowrance USR et d'écrire le fichier de sortie "output.gpx" au format GPX.

- **Importation/utilisation de fichiers convertis :** Après la conversion, vous aurez vos données GPS dans le nouveau format (par exemple, GPX), que vous pourrez utiliser avec d'autres logiciels GPS ou appareils prenant en charge ce format.

## Comment ouvrir le fichier USR?

Les programmes qui ouvrent ou font référence aux fichiers USR incluent

- GPSBabel (Windows)
-GPSBabel (Mac)
- GPSBabel (Linux)

## Les références
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

