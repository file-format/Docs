{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier MKV",
  "keywords" :[ "mkv", "vidéo matroska", "format mkv", "comment lire des fichiers mkv", "vidéo", "fichier", "format" ],
  "description":"En savoir plus sur le format de fichier MKV et les API qui peuvent créer et ouvrir des fichiers MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Qu'est-ce qu'un fichier MKV ? ##

MKV (Matroska Video) est un conteneur multimédia similaire aux formats [MOV](/fr/video/mov/) et [AVI](/fr/video/avi/) mais il prend en charge plusieurs pistes audio et de sous-titres dans le même fichier. Un fichier MKV est le format de conteneur multimédia Matroska utilisé pour la vidéo. MKV est basé sur Extensible Binary Meta Language et prend en charge plusieurs formats de compression vidéo et audio. La principale différence entre MKV et les autres formats vidéo est que MKV est un conteneur et non un codec. Les fichiers MKV sont enregistrés avec l'extension de fichier .mkv. MKV peut incorporer de l'audio, de la vidéo et des sous-titres dans un seul fichier, même si ces éléments utilisent différents types d'encodage. Par exemple, vous pouvez avoir un fichier MKV contenant de la vidéo H.264 et MP3 ou AAC pour l'audio. MKV prend également en charge les descriptions, les classements, les couvertures et même les points de chapitre. Il existe plusieurs caractéristiques clés qui font que MKV est à l'épreuve du temps. Ces fonctionnalités incluent :

- Prise en charge de la recherche rapide.
- Possibilité de sélectionner différents flux audio et vidéo.
- Prise en charge des sous-titres (codés en dur et codés en douceur).
- Prise en charge des métadonnées, des chapitres et des menus.
- Possibilité de diffuser en ligne.
- Possibilité de récupérer des fichiers erronés offrant la possibilité de lire des fichiers corrompus.

## Bref historique ##

Le fichier MKV est né en 2002 en Russie. Le développeur principal était Lasse Kärkkäinen qui a travaillé avec le fondateur de Matroska, Steve Lhomme, et une équipe de programmeurs. MKV a été développé en tant que projet de normes ouvertes, ce qui signifie qu'il est open source et gratuit. Au fil du temps, le format a été amélioré et est devenu la base du format multimédia WebM en 2010.

## Conception Matroska ##

Matroska ajoute les contraintes suivantes à la spécification EBML.

- Le **docType** de l'**EBML Header** doit être 'matroska'.
- Le **EBMLMaxIDLength** de l'**en-tête EBML** doit être 4.
- La **EBMLMaxSizeLength** de l'**EBML Header** doit être comprise entre 1 et 8 (inclus).

Tous les éléments de niveau supérieur sont codés sur 4 octets.

- Codes de langue : Matroska (version 1 à 3) utilise des codes de langue qui peuvent être soit la forme bibliographique à 3 lettres ISO-639-2 (comme "fre" pour le français), soit un code de pays supplémentaire peut être utilisé comme "fre-ca " pour le français canadien. À partir de Matroska version 4, ISO 639-2 ou BCP 47 PEUVENT être utilisés pour les codes de langue, bien que BCP 47 soit recommandé.
- Types physiques : ils ont une signification différente pour les fichiers audio et vidéo. Par exemple, ChapterPhysicalEquiv = 60 signifie (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) pour l'audio et (DVD / VHS / LASERDISC) pour la vidéo.
- Structure de bloc - En-tête de bloc : l'en-tête de bloc contient des informations concernant le numéro de piste, les horodatages, le type de laçage, etc.
- Lacing : Il s'agit d'un mécanisme permettant d'économiser de l'espace lors du stockage de données qui est généralement utilisé pour de petits blocs de données (frames). Il existe 3 types de laçage :
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Structure SimpleBlock : elle s'inspire de la **structure en bloc**, la principale différence étant l'ajout des indicateurs **Keyframe** et **Discardable**. A part ça, tout est pareil.

## Structure Matroska ##

Un document Matroska doit être composé d'au moins un **document EBML** utilisant le **type de document Matroska**. Chaque **document EBML** doit commencer par un **en-tête EBML** suivi de l'**élément racine EBML** défini comme un segment. Matroska définit plusieurs éléments de niveau supérieur qui peuvent apparaître dans le **segment**.

EBML utilise un système d'éléments pour composer un document EBML. Voici la liste des éléments de niveau supérieur dans le fichier Matroska :

- **Document EBML** : wrapper pour l'ensemble du fichier.
- **En-tête EBML** : Il contient les informations d'en-tête du fichier comme DocType.
- **Segment** : l'élément supérieur qui contient tous les autres éléments de niveau supérieur.
- **SeekHead** : Il contient la position des segments d'autres éléments de niveau supérieur.
- **Info** : contient des informations générales sur le segment.
- ** Pistes ** : un élément d'information de niveau supérieur avec de nombreuses pistes décrites.
- **Chapitres** : Il est utilisé pour définir les menus de base et les données de partition.
- **Cluster** : l'élément de niveau supérieur contenant la structure de bloc.
- **Indices** : un élément de niveau supérieur qui contient toutes les entrées locales au segment qui accélèrent la recherche d'accès.
- **Pièces jointes** : contient des fichiers joints.
- **Tags** : cet élément contient des métadonnées décrivant les pistes, les éditions, les chapitres, les pièces jointes ou le segment dans son ensemble.

Le tableau suivant montre la structure du document Matroska avec la plupart des éléments affichés dans une hiérarchie :

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| En-tête EBML | | | |
| Segmenter | Chercher Tête| Chercher | SeekID |
| | | | ChercherPosition |
| | Infos | UID de segment | |
| | | NomFichierSegment | |
| | | UID précédent | |
| | | NomFichierprécédent | |
| | | SuivantUID | |
| | | NomFichierSuivant | |
| | | SegmentFamille | |
| | | ChapitreTraduire | |
| | | Échelle d'horodatage | |
| | | Durée | |
| | | DateUTC | |
| | | Titre | |
| | | MuxingApp | |
| | | Application d'écriture | |
| | Pistes | TrackEntry | Numéro de piste |
| | | | TrackUID |
| | | | Type de piste |
| | | | Nom |
| | | | Langue |
| | | | CodecID |
| | | | CodecPrivé |
| | | | NomCodec |
| | | | Vidéo | DrapeauEntrelacé |
| | | | | FieldOrder |
| | | | | StéréoMode |
| | | | | AlphaMode |
| | | | | PixelLargeur |
| | | | | PixelHeight |
| | | | | AfficherLargeur |
| | | | | Hauteur d'affichage |
| | | | | AspectRatioType |
| | | | | Couleur |
| | | | Audio | Fréquence d'échantillonnage |
| | | | | Chaînes |
| | | | | BitDepth |
| | Chapitres | ÉditionEntrée | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | ÉditionDrapeauCommandé |
| | | | ChapitreAtom | ChapitreUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | ChapitreDrapeauCaché |
| | | | | ChapitreAffichage | ChapString |
| | | | | | ChapLangue |
| | Grappe | Horodatage |
| | | Pistes silencieuses |
| | | Poste |
| | | Taille précédente |
| | | SimpleBloc |
| | | Groupe de blocs |
| | | Bloc chiffré |
| | Queues | Point de repère | CueTime |
| | | | CueTrackPositions |
| | Pièces jointes | AttachedFile | DescriptionFichier |
| | | | NomFichier |
| | | | FichierMimeType |
| | | | FichierUID |
| | | | FileReferral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Balises | Balise | Cibles | ValeurTypeCible |
| | | | | TypeCible |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapitreUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | Nom de balise |
| | | | | TagLanguage |
| | | | | BaliseDefault |
| | | | | TagString |
| | | | | TagBinaire |
| | | | | SimpleTag |


### Utilisation de codecs ###

Si vous ne voulez pas de nouveau lecteur multimédia et préférez utiliser votre lecteur existant, vous devrez installer certains codecs (abréviation de compression/décompression). Même si le téléchargement de codecs est une option valable, vous devez faire attention à la source et ceux-ci peuvent contenir des logiciels malveillants.

## Références ##

- [Matroska par Wikipédia](https://en.wikipedia.org/wiki/Matroska)

