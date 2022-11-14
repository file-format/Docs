{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","qu'est-ce qu'un fichier cd","comment ouvrir un fichier cd", "extension", "fichier", "fichier cd","format de fichier cd", "extension de fichier cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Fichier de diagramme de classes Visual Studio",
  "description":"En savoir plus sur le format de fichier CD et les API permettant de créer et d'ouvrir des fichiers CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Qu'est-ce qu'un fichier CD ?

Un fichier avec l'extension .cd est un fichier de diagramme de classes Visual Studio qui fournit des informations sur la structure et la relation entre toutes les classes de la solution actuelle. Une solution Visual Studio (représentée par [.sln](/fr/programming/sln/)) peut contenir un ou plusieurs projets, chacun ayant plusieurs classes différentes. Le fichier de diagramme de classes peut être généré en cliquant avec le bouton droit sur le projet et en sélectionnant l'option de diagramme de classes.

## Format de fichier de diagramme de classes (.cd) - Plus d'informations

Un fichier de diagramme de classes est enregistré au format de fichier XML standard qui représente les classes d'un projet sous forme de nœuds XML. Si Visual Studio n'est pas disponible, ces fichiers de diagramme de classes peuvent être ouverts dans n'importe quel programme d'application prenant en charge l'ouverture de fichiers XML.

### Comment ajouter des diagrammes de classes au projet Visual Studio

Dans Visual Studio, ouvrez la solution/le projet pour lequel vous souhaitez ajouter le diagramme de classes. Cliquez ensuite avec le bouton droit sur le nœud du projet, puis choisissez Ajouter > Nouvel élément. Ou appuyez sur Ctrl+Maj+A.

* La boîte de dialogue Ajouter un nouvel élément s'ouvre.

* Développez Éléments communs > Général, puis sélectionnez Diagramme de classes dans la liste des modèles. Pour les projets Visual C++, recherchez dans la catégorie Utilitaire pour trouver le modèle de diagramme de classes.

### Exporter des diagrammes de classes (CD) vers des images

Visual Studio permet de convertir/exporter des diagrammes de classes vers des images telles que [PNG](/fr/image/png/), [JPEG](/fr/image/jpeg/) et [BMP](/fr/image/bmp/). Ces fichiers de diagramme de classes exportés peuvent être utilisés à des fins de documentation et de conservation des enregistrements du pack de données techniques (TDP). Pour convertir un diagramme de classes en image, les étapes suivantes peuvent être utilisées à partir de Microsoft Visual Studio.

1. Ouvrez votre fichier de diagramme de classes (.cd).
1. Dans le menu Diagramme de classes ou le menu contextuel de la surface du diagramme, choisissez Exporter le diagramme en tant qu'image.
1. Sélectionnez un diagramme.
1. Sélectionnez le format souhaité.
1. Choisissez Exporter pour terminer l'exportation.

## Références

* [Classes de conception dans Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

