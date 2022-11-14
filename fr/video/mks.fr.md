{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier MKS",
  "keywords" :[ "mks", "vidéo matroska", "format mkv", "fichier", "format", "vidéo"],
  "description":"En savoir plus sur le format de fichier MKS pour les sous-titres créés uniquement par Matroska et les API qui peuvent créer et ouvrir des fichiers MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Qu'est-ce qu'un fichier MKS ?

Les fichiers MKS sont généralement appelés fichiers Matroska contenant uniquement des sous-titres. Bien que le Matroska soit un conteneur de fichiers général, il évite de conserver les informations de formats spécifiques. Étant donné que les sous-titres sont utilisés dans certains conteneurs audio ou vidéo, Matroska veille à stocker certains formats de sous-titres courants. Cela aide Matroska à être cohérent avec le taux de croissance. Vous devez suivre les points ci-dessous pour stocker les sous-titres dans Matroska :

- Le « .mks ». l'extension sera utilisée par le fichier Matroska (contenant uniquement des sous-titres).
- **CodecPrivate** est utilisé pour stocker toutes les informations relatives aux codecs qui sont globales à un flux entier.
- Supprimez les horodatages de début et de fin qui sont utilisés dans un format de stockage natif d'horodatage. Utilisez plutôt l'horodatage et la durée des blocs.
- Vous pouvez utiliser n'importe quoi avec un calque transparent, y compris une vidéo.

## Formats de sous-titres courants

Voici quelques brèves notes sur les formats de sous-titres les plus courants stockés dans Matroska :

### Images Sous-titres
Le format de sous-titre VobSub est le premier format de sous-titre d'image à importer dans Matroska. Ce format est généré en exportant les sous-titres d'un DVD. Les pistes doivent être séparées lors du stockage dans Matroska si le VobSub se compose d'un ensemble de plusieurs flux.

### Sous-titres SRT
Le SRT est le plus simple et le plus basique de tous les formats de sous-titres. Il se compose de quatre parties comme indiqué ci-dessous :
 



1. Un nombre qui indique la séquence du sous-titre.
2. Temps d'apparition et de disparition des sous-titres à l'écran.
3. Le sous-titre lui-même.
4. Une ligne vide pour indiquer le début du sous-titre suivant.
 



### Sous-titres SSA/ASS
Sub Station Alpha (SSA) est un format de fichier utilisé par le célèbre éditeur de sous-titres SubStation Alpha. Les sous-titres SSA sont largement utilisés par les fansubbers. Il a la capacité d'afficher des fonctionnalités modernes, par exemple le karaoké, le positionnement, le style, etc.
 



### Sous-titres WebVTT
Le World Wide Web Consortium (W3C) a développé le WebVTT qui est abrégé en "Web Video Text Tracks Format". Ce format est utilisé pour baliser les ressources de pistes de texte externes en relation avec l'élément HTML.

### Sous-titres graphiques de présentation HDMV
Le format de sous-titres graphiques de présentation HDMV (HDMV PGS) est une série de bitmaps et nous ne pouvons pas dire du tout qu'il s'agit de texte. En d'autres termes, vous pouvez dire qu'il ne s'agit que d'une séquence chronométrée d'images graphiques. Pour extraire les informations, la conversion de PGS en SRT est un processus nécessaire.

### Sous-titres texte HDMV
Le texte HDMV est connu comme le format de sous-titre textuel utilisé sur les Blu-ray. Matroska n'autorise que le jeu de caractères UTF-8 lors du stockage des sous-titres TextST.

### Sous-titres de diffusion vidéo numérique (DVB)
Le format de sous-titre DVB a été introduit pour réguler la transmission et l'affichage de plusieurs langues de sous-titrage sur les signaux TV. Un format de sous-titrage typique permettrait également à tout téléspectateur de regarder des transmissions sous-titrées DVB, quel que soit le fabricant des systèmes de transmission.


## Références ##

- [Sous-titres Matroska](https://www.matroska.org/technical/subtitles.html)

