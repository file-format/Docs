{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "fichier", "extension", "format", "format de fichier d'échange audio", "musique" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier WMA et les API qui peuvent créer et ouvrir des fichiers WMA.",
  "title" :"WMA - Fichier audio Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Qu'est-ce qu'un fichier WMA ?

Un fichier avec l'extension .wma représente un fichier audio enregistré au format Advanced Systems Format (ASF). ASF est le format propriétaire de Microsoft qui contient des flux binaires encodés par Windows Media Audio 9. En plus du contenu audio, un fichier WMA contient également des objets de métadonnées tels que le titre, l'album, l'artiste et le genre de la piste. Les fichiers WMA sont principalement utilisés pour la diffusion en continu sur le Web, comme les fichiers [.mp3](/fr/audio/mp3/).

## Format de fichier WMA

Un fichier WMA est un format de fichier binaire et est contenu dans le format de fichier ASF. Il spécifie l'encodage des métadonnées sur le fichier similaire aux balises ID3 utilisées par les fichiers MP3. Le codec WMA est utilisé par Microsoft dans son format de fichier interopérable protégé (PIFF) depuis 2008. Cependant, il n'a pas été déclaré codec audio normalisé par les normes industrielles connexes telles que DECE UltraViolet et MPEG-DASH.

### Données spécifiques au type WMA

Les informations spécifiques au type pour le codec Windows Media Audio sont stockées au format suivant dans le cadre des données spécifiques au type de l'objet de propriétés de flux.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Références

* [Présentation ASF - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

