{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier FIT - Fichier d'activité Garmin",
  "description":"En savoir plus sur le format de fichier FIT et les API qui peuvent créer et ouvrir des fichiers FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Qu'est-ce qu'un fichier FIT ?

Un fichier FIT est un fichier SIG créé par les appareils portables de sport Garmin. Il est utilisé pour enregistrer les activités de la personne lorsqu'elle se déplace en portant ces appareils. Les données d'activité comprennent l'emplacement et l'heure enregistrés par le dispositif GPS. Les fichiers FIT sont également utilisés pour transférer les données d'activité enregistrées à l'aide d'API Web. C'est la raison pour laquelle les fichiers FIT sont le format de fichier le plus couramment utilisé pour partager des données de fitness avec d'autres plateformes de fitness. Les autres formats de fichiers courants incluent [GPX](/fr/gis/gpx/), TCX et [KML](/fr/gis/kml/).

## Format de fichier FIT - Plus d'informations

Les fichiers FIT sont enregistrés sur le disque sous forme de fichiers binaires avec les informations enregistrées par les appareils Garmin pour l'activité. Les informations stockées dans un fichier FIT incluent :

* Date et heure
* Types de sports
* Données de tour et de fractionnement
* Piste GPS
* Données du capteur
* Événements pour la session active

Les données d'activité peuvent être enregistrées dans le fichier en temps réel ou exportées une fois l'enregistrement d'activité terminé.

### Messages d'activité FIT

Un fichier d'activité FIT peut inclure certains types de messages requis. Voici les messages requis pour un fichier d'activité.

|Message|Objectif|
---|---|
|Identifiant de fichier| Le message File Id est requis par tous les types de fichiers FIT et devrait être le premier message du fichier. Pour les fichiers d'activité, la propriété Type doit être définie sur 4.|
|Activité| Un seul message d'activité est requis dans un fichier d'activité FIT. Le message d'activité comprend les propriétés d'horodatage local et de nombre de sessions. L'horodatage local est utilisé pour déterminer le décalage de fuseau horaire qui peut être appliqué à tous les horodatages du fichier. La plupart des appareils enregistrent les fichiers FIT en temps réel et le nombre de sessions sera inconnu jusqu'à la fin de l'enregistrement. Pour cette raison, le message d'activité sera souvent le dernier message du fichier.|
|Séance| Les fichiers d'activité contiendront un ou plusieurs messages de session. Un message de session est un type de message de résumé. L'heure de début, le temps total écoulé, le temps total de la minuterie et l'horodatage sont des champs obligatoires pour tous les messages de résumé.|
|Tour| Les messages de tour représentent des tours ou des intervalles au sein de la session. Un message Tour est un message de type Résumé. L'heure de début, le temps total écoulé, le temps total de la minuterie et l'horodatage sont des champs obligatoires pour tous les messages de résumé.|
|Enregistrer| Les messages d'enregistrement incluent les coordonnées GPS, la vitesse, la distance, la fréquence cardiaque, la puissance, etc. |

## Ressources utiles du fichier FIT

* [Décodage des fichiers d'activité FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Encodage des fichiers d'activité FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Références ##

* [Fichier d'activité FIT](https://developer.garmin.com/fit/file-types/activity/)

