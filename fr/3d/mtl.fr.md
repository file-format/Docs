{
"date": "2023-10-11",
   "keywords":[
"mtl",
"fichier mtl",
"fichier de bibliothèque de modèles de matériaux mtl obj",
"comment ouvrir un fichier mtl",
"déposer",
"extension de fichier mtl",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier MTL - Fichier de bibliothèque de modèles de matériaux OBJ",
   "description":"Découvrez le format de fichier de la bibliothèque de modèles de matériaux MTL OBJ et les API qui peuvent créer et ouvrir des fichiers MTL.",
"linktitle": "MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
"parent" : "3d"
}
},
"lastmod": "2023-10-11"
}

## Qu'est-ce qu'un fichier MTL ?

Le fichier MTL, abréviation de **Material Template Library**, est un format de fichier compagnon utilisé en infographie et en modélisation 3D. Il est souvent associé au **format de fichier Wavefront OBJ**, qui est un format courant pour stocker des modèles 3D ainsi que leurs matériaux et textures associés.

## Bibliothèque de modèles de matériaux

Voici des informations importantes sur les fichiers MTL :

1. **Définitions des matériaux** : Le fichier ".mtl" contient des définitions des matériaux appliqués aux objets 3D dans le fichier OBJ correspondant. Chaque définition de matériau spécifie diverses propriétés, telles que la couleur, la brillance, la transparence et les cartes de texture.
    





2. **Format basé sur texte** : les fichiers ".mtl" sont généralement des fichiers texte brut, ce qui signifie qu'ils peuvent être facilement modifiés avec un éditeur de texte. Chaque définition de matériau se compose d'un ensemble d'instructions et ces instructions définissent les attributs du matériau.
    





3. **Mappage de textures** : L'une des fonctions essentielles d'un fichier ".mtl" est de définir comment les textures (fichiers image) sont mappées sur les surfaces du modèle 3D. Il spécifie le chemin du fichier de texture et comment il doit être enveloppé ou appliqué au modèle.
    





4. **Exemples d'instructions MTL** : Voici quelques exemples d'instructions que vous pourriez trouver dans un fichier ".mtl" :
    





- `newmtl MaterialName` : Ceci définit un nouveau matériau portant le nom "MaterialName".
- `Ka rgb` : Couleur ambiante du matériau, spécifiée en valeurs RVB.
- `Kd rgb` : Couleur diffuse du matériau, spécifiée en valeurs RVB.
- `Ks rgb` : Couleur spéculaire du matériau, spécifiée en valeurs RVB.
- `Valeur Ns` : Brillance ou exposant spéculaire du matériau.
- `map_Kd texturefile.jpg` : Spécifie la carte de texture diffuse pour le matériau.
5. **Matériaux multiples** : Un fichier OBJ peut référencer plusieurs matériaux et chaque matériau est défini dans le fichier ".mtl". Cela permet de créer des modèles 3D complexes avec différents matériaux appliqués à différentes pièces.
    





6. **Compatibilité** : les fichiers ".mtl" sont largement pris en charge par les logiciels de modélisation 3D et les moteurs de rendu, permettant de transférer des modèles 3D et leurs matériaux entre différentes applications logicielles.

## Comment ouvrir un fichier MTL ?

Les fichiers MTL sont des fichiers texte, ils peuvent donc être ouverts avec n'importe quel éditeur de texte, y compris

- Bloc-notes (Windows)
- Bloc-notes++ (Windows)
-Code Visual Studio
- Texte sublime
- Atome
- TextEdit (macOS)

Les programmes qui ouvrent ou font référence aux fichiers MTL incluent

-Adobe Photoshop 2023
-Autodesk Maya 2023
- MeshLab
- Guépard3D

**Sous-type :** Fichiers d'images 3D

## Les références
* [Fichier Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

