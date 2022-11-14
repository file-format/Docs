{
  "date" : "2019-10-11",
  "keywords" :[ "fichier xpm", "format de fichier xpm", "qu'est-ce qu'un fichier xpm", "fichier", "exemple xpm", "extension de fichier xpm","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - Format de fichier X PixMap",
  "description":"En savoir plus sur le format de fichier XPM et les API qui peuvent créer et ouvrir des fichiers XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier XPM ?

Un fichier avec l'extension .xpm est un format de fichier image utilisé par le système X Windows. Il prend en charge les pixels transparents et cible généralement la création de pixmaps d'icônes. Il prend en charge les données monochromes, à l'échelle gra et couleur pixmap. Ceux-ci ont été conçus pour être modifiables à la main et peuvent être inclus dans le code [C](/fr/programming/c/). À cette fin, les fichiers XPM sont au format de fichier texte brut et suivent la syntaxe du langage de programmation C. Les fichiers XPM peuvent être ouverts avec une variété d'applications de visualisation d'images telles que
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView et Canvas X.

## Format de fichier XPM

Le format de fichier XPM utilise la syntaxe C afin que ceux-ci soient intégrés dans les programmes C et C++. Il se compose des six sections différentes suivantes.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Les sections sont en fait un tableau de chaînes comme suit.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Voici les détails de chaque section.

`<Values> ` - Cette section est une chaîne contenant quatre ou six entiers en base 10 et correspondant à :

* largeur et hauteur du pixmap
* nombre de couleurs
* nombre de caractères par pixel
* Coordonnées facultatives du point d'accès et balise XPMEXT

`<Colors> ` - Cette section contient autant de chaînes qu'il y a de couleurs. Chaque chaîne est la suivante :

```
<chars>{<key><color> }+
```
`<Pixels> ` - Cette section est composée de<height> cordes et<width> \*<chars_per_pixel> personnages. Tous<chars_per_pixel> longueur chaîne doit être l'un des groupes précédemment définis dans le<Colors> section.

`<Extension> ` - La section d'extension doit être étiquetée, si elle n'est pas vide, dans<Values> section. Il peut être composé de plusieurs<Extension> sous-sections qui peuvent être des deux types suivants :

* une chaîne autonome composée comme suit : XPMEXT<extension-name><extension-data>
* ou un bloc composé de plusieurs chaînes :XPMEXT<extension-name><related extension-data composed of several strings>

## Références

* [XPM - Wikipédia](https://en.wikipedia.org/wiki/X_PixMap)
* [Manuel XPM](http://www.xfree86.org/current/xpm.pdf)

