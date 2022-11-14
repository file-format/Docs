{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "fichier", "extension", "format", "Codage audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier AAC et les API qui peuvent créer et ouvrir des fichiers AAC.",
  "title" :"AAC - Fichier de codage audio avancé",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Qu'est-ce qu'un fichier AAC ?

AAC (Advanced Audio Coding) fait référence à la norme de codage audio numérique qui représente les fichiers audio basés sur une compression audio avec perte. Il a été lancé en tant que successeur du format de fichier **[MP3](/fr/audio/mp3/)** en gardant à l'esprit que le latéral a rencontré des problèmes pour la mise en œuvre de nouvelles idées dans le processus d'encodage basé sur le développement de méthodes de compression de données. AAC atteint une meilleure qualité sonore par rapport au MP3 au même débit binaire. Il a été défini dans MPEG-2 Partie 7 (ISO/IEC 13818-7) et sous une forme mise à jour dans MPEG-4 Partie 3 (ISO/IEC 14496-3).

Le format AAC a été adopté comme format multimédia par défaut par YouTube, iPhone, iPod, iPad, Apple iTunes et plusieurs autres plates-formes. Plusieurs applications et API sont disponibles pour la conversion du format de fichier AAC vers d'autres formats tels que MP3, WMA, M4A, **[WAV](/fr/audio/wav/)** et autres.

### Bref historique du fichier AAC

Le format de fichier AAC est une version améliorée de MP3 avec quelques améliorations. Contribué par plusieurs sociétés, dont l'Institut Fraunhofer (Fraunhofer IIS - développeurs de MP3), Nokia, Dolby, AT&T et Sony, le format a été déclaré standard international par Moving Picture Experts Group (MPEG) en avril 1997. Plus tard en 1999, le MPEG-2 Part 7 a été mis à jour et inclus dans la famille de normes MPEG-4. Il était connu sous le nom de MPEG-4 Part 3, identifié comme ISO/IEC 14496-3 : 1999 ou MPEG-4 Audio.

## Spécifications du format de fichier AAC

Les spécifications du format de fichier AAC permettent une plus grande flexibilité de conception de codec que le MP3, ce qui se traduit par davantage de stratégies d'encodage simultanées et une compression efficace. Le format a été choisi par un certain nombre de plates-formes matérielles pour ses améliorations par rapport au MP3 en termes de prise en charge de plus d'options, même à des débits inférieurs. Les spécifications du format de fichier AAC sont disponibles sous [MPEG-2 Part 7](https://www.iso.org/standard/43345.html) et [MPEG-4 Part 3](https://www.iso.org /standard/53943.html) (téléchargement payant). Le format utilise les types de médias suivants :

* audio/aac
* audio/aacp
* audio/3gpp
* audio/3gpp2
* audio/mp4
* audio/mp4a-latm
* audio/mpeg4-générique

## AAC vs MP3 - Améliorations ##

Les principales différences entre AAC et MP3 en termes d'améliorations sont les suivantes :

* AAC prend en charge une plus large gamme de canaux (jusqu'à 48) et de taux d'échantillonnage (de 8 kHz à 96 kHz)
* AAC a de meilleures fréquences de codage au-dessus de 16 kHz
* AAC a des limites de variation plus larges dans la résolution fréquence-temps d'une banque de filtres qui ont conduit à un codage amélioré des transitoires et des parties stationnaires du signal audio
* Banc de filtres plus efficace et plus simple : un banc de filtres hybride a été remplacé par le standard MDCT (modified discrete cosine transform)
* Prend en charge l'efficacité améliorée de la compression en utilisant la mise en forme du bruit temporel (TNS), les coefficients de prédiction du temps MDCT (prédiction à long terme), la stéréo paramétrique, la substitution de bruit perceptuel, la réplication de bande spectrale (SBR).
* stéréo commune plus flexible (différentes méthodes peuvent être utilisées dans différentes gammes de fréquences);

## Références ##

* [AAC - Par Wikipédia](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

