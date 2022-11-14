{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "fichier amf", "format de fichier amf", "format de fichier", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier AMF et les API qui peuvent ouvrir et créer des fichiers AMF.",
  "title" :"AMF - Dossier Fabrication Additive",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier AMF ?
Un fichier AMF est constitué de lignes directrices pour la description des objets afin d'être utilisés par les processus de fabrication additive. Il contient une ouverture<amf> balise XML et se termine par un</amf> élément. Elle est précédée d'une ligne de déclaration XML spécifiant la version XML et l'encodage du fichier. Les déclarations peuvent inclure des informations sur les unités de mesure et, en l'absence de telles informations, les millimètres sont utilisés comme unité par défaut.


## Format de fichier AMF

Le format de fichier de fabrication additive (**AMF**) définit des normes ouvertes pour la description des objets afin d'être utilisés par des processus de fabrication additive tels que l'impression 3D. Les programmes de CAO utilisent le format de fichier AMF en utilisant des informations telles que la géométrie, la couleur et le matériau des objets. AMF est différent du format STL car le latéral ne prend pas en charge la couleur, les matériaux, les réseaux et les constellations.

### Éléments d'un fichier AMF

Les cinq éléments de niveau supérieur définis avec le<AMF> les balises sont détaillées ci-dessous. La présence d'un seul élément d'objet est indispensable pour un fichier AMF entièrement fonctionnel.

`<object> ` - L'élément objet définit un volume ou des volumes de matériau, chacun étant associé à un ID de matériau pour l'impression. Au moins un élément d'objet doit être présent dans le fichier. Les objets supplémentaires sont facultatifs.

`<material> ` - L'élément de matériau facultatif définit un ou plusieurs matériaux à imprimer avec un ID de matériau associé. Si aucun élément de matériau n'est inclus, un seul matériau par défaut est supposé.

`<texture> ` - L'élément de texture facultatif définit une ou plusieurs images ou textures pour le mappage de couleurs ou de textures, chacune avec un ID de texture associé.

`<constellation> ` - L'élément de constellation facultatif combine hiérarchiquement des objets et d'autres constellations dans un motif relatif pour l'impression.

`<metadata> ` - L'élément de métadonnées facultatif spécifie des informations supplémentaires sur le ou les objets et éléments contenus dans le fichier.

## Exemple AMF

Voici un exemple de fichier AMF qui peut être copié dans un fichier [texte](/fr/word-processing/txt/) et enregistré en tant que fichier compressé [zip](/fr/compression/zip/) pour l'ouverture.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Références

* [AMF - Wikipédia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Spécifications AMF sur ISO](https://www.iso.org/standard/67472.html)

