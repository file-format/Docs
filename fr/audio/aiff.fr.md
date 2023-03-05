{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "fichier", "extension", "format", "format de fichier d'échange audio", "musique", "format de fichier aiff", "aiff en mp3", "aiff vs wav", "convertir aiff en mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier AIFF et les API qui peuvent créer, convertir et ouvrir des fichiers AIFF.",
  "title" :"AIFF - Format de fichier d'échange audio",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Qu'est-ce qu'un fichier AIFF ?
L'AIFF (Audio Interchange File Format) est un format de fichier audio non compressé développé par Apple en 1998, mais basé sur **EA IFF 85** (Standard for Interchange Format Files développé par Electronic Arts), un format wrapper utilisé sur les systèmes Amiga . Ce format de fichier propose une norme pour le stockage des sons échantillonnés. Le format est suffisamment flexible et permet le stockage de sons échantillonnés monauraux ou multicanaux à différentes fréquences d'échantillonnage et largeurs d'échantillonnage. Étant donné que les fichiers AIFF ne sont pas compressés, cela les rend plus gros que d'autres formats avec perte tels que [MP3](https://docs.fileformat.com/audio/mp3/).

Les fichiers AIFF se composent de 2 canaux d'audio stéréo non compressé avec une taille d'échantillon de 16 bits, enregistrés à 44,1 khz. En raison de la qualité audio élevée, un fichier audio de 5 minutes peut occuper jusqu'à 50 Mo d'espace disque, ce qui est similaire au format de fichier [WAV](https://docs.fileformat.com/audio/wav/).

## AIFF contre WAV

L'AIFF et le WAV sont presque les mêmes en terme de qualité. Les deux utilisent le même encodage PCM (modulation par impulsions codées), ce qui les rend plus grands par rapport à d'autres formats avec perte, tels que [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Certaines des différences générales sont écrites dans le tableau ci-dessous :

|AIFF|WAV|
---|---|
|Utilisé principalement pour MAC|Principalement utilisé pour les PC|
|Permet les métadonnées| N'autorise pas les métadonnées|

## Structure des fichiers AIFF

L'**EA IFF 85** établit une structure globale pour le stockage des données dans des fichiers. Un fichier **EA IFF 85** se compose d'un certain nombre de blocs de données. Un morceau est un bloc de construction de fichier AIFF composé de certaines informations d'en-tête suivies de données :
{{< figure src="../chunk.png" alt="Bloc AIFF" >}}

Un fichier AIFF est une collection d'un certain nombre de différents types de morceaux. Il existe deux types généraux de blocs qui sont importants pour former un bloc de fichier AIFF :
- **Common Chunk** : Contient des paramètres importants décrivant le son échantillonné, tels que sa longueur et sa fréquence d'échantillonnage.
- **Sound Data Chunk** : Contient les échantillons audio réels.
Il existe de nombreux autres blocs facultatifs qui répertorient les paramètres de l'instrument, définissent des marqueurs, stockent des informations spécifiques à l'application, etc.

### Types de blocs locaux

Les types de blocs pour former AIFF sont donnés dans le tableau ci-dessous :

|Type de bloc| Descriptif|
---|---|
|Common Chunk|Le Common Chunk décrit les paramètres fondamentaux du son échantillonné|
|Sound Data Chunk|Le Sound Data Chunk contient les trames d'échantillonnage réelles|
|Marker Chunk|Le Marker Chunk contient des marqueurs qui pointent vers des positions dans les données sonores|
|Instrument Chunk|Instrument Chunk définit les paramètres de base qu'un instrument, tel qu'un échantillonneur, pourrait utiliser pour lire les données sonores|
|MIDI Data Chunk|Le MIDI Data Chunk peut être utilisé pour stocker des données MIDI|
|Bloc d'enregistrement audio|Le bloc d'enregistrement audio contient des informations relatives aux appareils d'enregistrement audio|
|Application Specific Chunk|Le Application Specific Chunk peut être utilisé à quelque fin que ce soit par les fabricants d'applications|
|Comments Chunk|Le Comments Chunk est utilisé pour stocker les commentaires au format FORM AIFF|
|Blocs de texte - Nom, Auteur, Copyright, Annotation| Tous sont des morceaux de texte |

## Références ##

* [Format de fichier d'échange audio - Par Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

