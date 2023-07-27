{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier MP - Fichier LaTeX MetaPost",
  "description":"En savoir plus sur le format de fichier MP et les API qui peuvent créer et ouvrir des fichiers MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Qu'est-ce qu'un fichier MP ?

Un fichier MP est un fichier d'image vectorielle généré par le langage de programmation MetaPost pour créer des images. Les images vectorielles créées à l'aide du format de fichier MP sont enregistrées en tant que fichiers [EPS](/fr/page-description-language/eps/) (Encapsulated PostScript). De plus, MetaPost est distribué avec les frameworks TeX et Metafont et les fichiers MP peuvent être générés à partir des fichiers TEX et LTX utilisés par ces applications. Les fichiers MP contiennent des instructions de dessin et un dessin algorithmique mathématique pour le rendu du fichier EPS de sortie. Le moteur PDFTex peut utiliser l'EPS créé pour générer directement des fichiers [PDF](/fr/pdf/).

## Format de fichier MP

Les fichiers MP sont enregistrés sur le disque en tant que fichiers binaires et génèrent une sortie EPS lorsqu'ils sont exportés au format de fichier d'image vectorielle de sortie. Les dessins créés à l'aide de MetaPost sont inclus sous forme formatée dans les documents techniques et les publications de journaux créés avec LaTex.

### Exemple de fichier MP MetaPost

Voici un exemple, référencé à partir de [Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), qui contient une flèche et la lettre "A" juste au-dessus du milieu du La Flèche.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Références ##

* [MetaPost par Wikipédia](https://en.wikipedia.org/wiki/MetaPost)
* [Échantillon de latex Metapost par Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

