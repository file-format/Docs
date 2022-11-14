{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "fichier", "extension", "format", "audio", "smaf", "extension mmf", "fichiers mmf", "fichier de musique mobile", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier MMF et les API qui peuvent créer et ouvrir des fichiers MMF.",
  "title" :"MMF - Format de fichier de musique mobile",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Qu'est-ce qu'un fichier MMF ?

MMF est une extension de fichier associée à un fichier SMAF. Le MMF signifie Mobile Music File tandis que le SMAF signifie Synthetic-music Mobile Application Format. Les fichiers MMF d'un smartphone contiennent des sonneries système, du son et peuvent également contenir des graphiques et un affichage de texte. Le MMF contient en outre trois types de paramètres d'instrument, notamment FM, PCM et Stream PCM. Ces formats de fichiers sont compatibles avec la plate-forme système Windows. Les fichiers MMF sont classés en tant que fichiers de données. Généralement, Microsoft Mail prend en charge les fichiers MMF. Le fichier ayant le suffixe MMF peut être copié sur n'importe quel appareil mobile ou plate-forme système.

De plus, ces fichiers sont beaucoup plus petits que les fichiers au format MIDI standard. Les fichiers [WAV](/fr/audio/wav/) et [MID](/fr/audio/mid/) peuvent être convertis au format MMF, puis partagés et distribués en tant que contenu audio. Ces fichiers peuvent être reçus par e-mail directement sur les téléphones et les PC.


## Bref historique du format de fichier MMF

Yamaha a développé des outils SMAF sous forme de fichiers audio afin que les smartphones puissent stocker un plus grand nombre de sonneries uniques. Yamaha a présenté SMAF avec la production de ses puces sonores MA-1, MA-2, MA-3, MA-5 et MA-7 LSI. Tous ces formats sont devenus assez familiers parmi les téléphones mobiles du marché de l'Asie de l'Est au début des années 2000.

Au niveau international, le format MMF a été autorisé par Samsung. Avec l'aide du format MMF, Samsung a pu concevoir une large gamme de sonneries polyphoniques à utiliser dans les smartphones Samsung.

Yamaha a voulu rendre le format encore plus populaire et donc sur les fichiers officiels Yamaha SMAF, il a publié plus d'outils compatibles avec ce format. Avec cela, les utilisateurs peuvent désormais lire facilement des fichiers MMF sur leurs ordinateurs.


## Spécifications du format de fichier MMF ##

Les fichiers MMF sont classés en sections de données. Une structure préfixée autour d'un 8 octets est utilisée pour décrire chaque segment.
L'étiquette de 4 octets comprend CNTI, OPDA, MSTR, MTR et ATR. La taille des données plus 8 octets correspond à la taille du bloc ; la taille totale du fichier est calculée en additionnant toutes les tailles de bloc. Si un fichier n'a pas été endommagé, la taille de fichier additionnée doit être la même que la taille d'un en-tête principal.

### Entête ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Voici un exemple de fichier MMF :

![](../mmf.png)

## Références

* [MMF - Par Wikipédia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

