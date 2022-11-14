{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "fichier", "extension", "format", "format de fichier d'échange audio", "musique" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier WAV et les API qui peuvent créer et ouvrir des fichiers WAV.",
  "title" :"WAV - Format de fichier audio de forme d'onde",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Qu'est-ce qu'un fichier WAV ?

WAV, connu pour WAVE (Waveform Audio File Format), est un sous-ensemble de la spécification RIFF (Resource Interchange File Format) de Microsoft pour le stockage de fichiers audio numériques. Le format n'applique aucune compression au flux binaire et stocke les enregistrements audio avec différents taux d'échantillonnage et débits. Il a été et est l'un des formats standard pour les CD audio. Les fichiers Wave sont plus volumineux que les nouveaux formats de fichiers audio tels que [MP3](/fr/audio/mp3/) qui utilise une compression avec perte pour réduire la taille du fichier tout en conservant la même qualité audio. Cependant, les fichiers WAV peuvent être compressés à l'aide des codecs Audio Compression Manager (ACM). Il existe plusieurs API et applications disponibles qui peuvent convertir des fichiers WAV vers d'autres formats de fichiers audio populaires.

**Le saviez-vous?**
Vous pouvez devenir un contributeur sur FileFormat.com pour tenir la communauté des formats de fichiers au courant de vos découvertes. Si vous devez partager quoi que ce soit sur les formats de fichiers WAV ou audio, vous pouvez publier vos découvertes dans la section [Audio File Format News](https://news.fileformat.com/t/audio) pour que les gens restent informés.

## Format de fichier WAV ##

Le format de fichier WAVE, étant un sous-ensemble de la spécification RIFF de Microsoft, commence par un en-tête de fichier suivi d'une séquence de blocs de données. Un fichier WAVE a un seul morceau "WAVE" qui se compose de deux sous-morceaux :

* un morceau "fmt" - spécifie le format de données
* un morceau de "données" - contient les données réelles de l'échantillon

### En-tête de fichier WAV ###

L'en-tête d'un fichier WAV (RIFF) fait 44 octets et a le format suivant :


|Positions|Valeur d'échantillon|Description
---|---|---|
|1 - 4|"RIFF"|Marque le fichier comme fichier riff. Les caractères font chacun 1 octet de long.
|5 - 8|Taille du fichier (entier)|Taille du fichier global - 8 octets, en octets (entier 32 bits). En règle générale, vous remplissez ceci après la création.
|9 -12|"WAVE"|En-tête de type de fichier. Pour nos besoins, il est toujours égal à "WAVE".
|13-16|"fmt "|Marqueur de bloc de format. Inclut la valeur nulle de fin
|17-20|16|Longueur des données de format comme indiqué ci-dessus
|21-22|1|Type de format (1 est PCM) - Entier de 2 octets
|23-24|2|Nombre de canaux - Entier de 2 octets
|25-28|44100|Taux d'échantillonnage - Entier de 32 octets. Les valeurs courantes sont 44100 (CD), 48000 (DAT). Taux d'échantillonnage = nombre d'échantillons par seconde, ou Hertz.
|29-32|176400|(Taux d'échantillonnage * Bits par échantillon * Canaux) / 8.
|33-34|4|(BitsParSample * Canaux) / 8.1 - 8 bits mono2 - 8 bits stéréo/16 bits mono4 - 16 bits stéréo
|35-36|16|Bits par échantillon
|37-40|"data"|en-tête de bloc "data". Marque le début de la section des données.
|41-44|Taille du fichier (données)|Taille de la section des données.
|Des exemples de valeurs sont donnés ci-dessus pour une source stéréo 16 bits.

## Références ##

* [WAV - Par Wikipédia](https://en.wikipedia.org/wiki/WAV)

