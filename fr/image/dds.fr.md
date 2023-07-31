{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier DDS - Fichier d'image de surface DirectDraw",
  "description":"En savoir plus sur le format de fichier DDS et les API qui peuvent créer et ouvrir des fichiers DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Qu'est-ce qu'un fichier DDS ?

Un fichier DDS est un fichier d'image raster qui utilise le format de conteneur DirectDraw Surface (DDS). Il stocke les textures non compressées et compressées (DXTn) et implémente différents types pour stocker différents types de données. Il prend également en charge plusieurs types de données différents tels que les textures à une seule couche, les textures avec mipmaps, les cartes de cube, les cartes de volume et les tableaux de texture. Cela permet aux fichiers DDS de stocker des modèles d'unités de texture de jeux vidéo en plus des photos numériques et des arrière-plans de bureau Windows. Le format de fichier DDS a été développé par Microsoft pour être utilisé avec DirectX SDK.

## Format de fichier DDS

Les fichiers DDS sont enregistrés sous forme de fichiers binaires et peuvent être utilisés avec DirectX SDK. Il utilise la puissance de DirectX pour développer des applications de rendu en temps réel telles que des jeux 3D.

### Disposition du fichier DDS

La [mise en page du fichier DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) a été documentée en détail par Microsoft. Un fichier DDS binaire contient les informations suivantes.

* Un DWORD (numéro magique) contenant la valeur de code à quatre caractères 'DDS' (0x20534444).
* Une description des données dans le fichier.

Le DDS_HEADER décrit les données et le DDS_PIXELFORMAT décrit le format de pixel. Celles-ci remplacent toutes les deux les structures obsolètes DDSURFACEDESC2, DDSCAPS2 et DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

Le [guide de programmation du format de fichier DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) détaille les détails techniques de ce format de fichier.

## Références

* [DDS - Par Wikipédia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Manuel de référence technique du format de fichier ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

