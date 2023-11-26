{
"date": "2023-10-11",
   "keywords":[
"chr",
"fichier chr",
"fichier de caractères chr cryengine",
"comment ouvrir un fichier chr",
"déposer",
"extension de fichier chr",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier CHR - Fichier de caractères CryENGINE",
   "description":"Découvrez le format de fichier CHR CryENGINE Character et les API permettant de créer et d'ouvrir des fichiers CHR.",
"linktitle": "CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
"parent": "3d"
}
},
"lastmod": "2023-10-11"
}

## Qu'est-ce qu'un fichier CHR ?

Le fichier CHR dans le contexte de CryENGINE fait référence à un **fichier de caractères CryENGINE**. CryENGINE est un moteur de jeu développé par Crytek et ces fichiers sont utilisés pour stocker des modèles de personnages et des données associées à utiliser dans les jeux vidéo et autres applications en temps réel.

## Fichier de caractères CryENGINE

Un fichier de caractères CryENGINE contient généralement les composants suivants :

1. **Modèle de personnage** : Il s'agit d'un modèle 3D de personnage, comprenant sa géométrie, ses textures et ses animations. Ces modèles sont souvent créés à l'aide de logiciels comme Autodesk Maya ou Blender puis importés dans CryENGINE.
    




















2. **Données d'animation** : CryENGINE prend en charge les animations complexes pour les personnages, donc le fichier ".chr" peut inclure diverses animations telles que marcher, courir, sauter et plus encore. Ces animations sont généralement stockées sous forme de données d'images clés.
    




















3. **Informations sur le gréement** : Le gréement fait référence au processus de création d'une structure squelette pour le modèle de personnage, qui permet d'appliquer des animations au modèle. Le fichier ".chr" peut contenir des informations sur la hiérarchie des os et sur la manière dont le maillage du personnage est connecté à ce squelette.
    




















4. **Données sur les matériaux et les textures** : Les informations sur les matériaux utilisés sur le modèle de personnage et les cartes de texture associées peuvent être incluses dans le fichier ".chr". CryENGINE prend en charge le rendu basé sur la physique, de sorte que ces matériaux peuvent être assez détaillés.
    




















5. **Données physiques** : Si le personnage est destiné à interagir avec le monde du jeu, le fichier ".chr" peut inclure des données physiques telles que des formes de collision ou des contraintes pour la physique du ragdoll.
    




















6. **Paramètres de configuration** : Divers paramètres de configuration liés au comportement du personnage dans le monde du jeu, tels que le comportement de l'IA ou les événements scriptés, peuvent également faire partie du fichier ".chr".

## CryENGINE

CryENGINE est un puissant moteur de jeu développé par Crytek, société allemande de jeux vidéo. Il est connu pour ses capacités graphiques de pointe et a été utilisé pour créer des jeux vidéo visuellement époustouflants et technologiquement avancés. Voici quelques fonctionnalités et informations clés sur CryENGINE :

1. **Graphiques et rendu** : CryENGINE est réputé pour ses capacités graphiques avancées. Il prend en charge des fonctionnalités telles que l'éclairage global en temps réel, l'éclairage et les ombres dynamiques de haute qualité, le rendu physique (PBR) et les textures haute résolution. Ces fonctionnalités contribuent à créer des mondes de jeu visuellement époustouflants et réalistes.
    




















2. **Moteur physique** : CryENGINE comprend un moteur physique intégré qui permet des interactions réalistes entre les objets du monde du jeu. Il prend en charge des fonctionnalités telles que la physique des corps rigides, la physique des corps mous et la physique des ragdolls, ce qui le rend adapté à la création d'environnements dynamiques et immersifs.
    




















3. **Terrain et végétation** : CryENGINE fournit des outils pour créer des environnements extérieurs vastes et détaillés. Il prend en charge l'édition de terrain, le placement de la végétation et les systèmes météorologiques dynamiques, permettant aux développeurs de créer des environnements extérieurs étendus et réalistes.
    




















4. **Animation de personnages** : CryENGINE comprend des outils robustes pour l'animation de personnages. Il prend en charge les configurations de personnages complexes, l'animation faciale et le système d'arbre de mélange qui permettent aux développeurs de créer des mouvements et des animations de personnages réalistes.
    




















5. **Système IA** : Le moteur dispose d'un système d'IA qui permet la création de PNJ intelligents (personnages non-joueurs) et d'IA ennemis. Les développeurs peuvent scripter le comportement et les interactions de l'IA pour créer des expériences de jeu stimulantes et immersives.
       





















6. **Scripting** : CryENGINE utilise un langage de script appelé « Schematyc » qui permet aux développeurs de créer une logique de jeu et des interactions. De plus, il prend en charge le C++ pour des besoins de programmation plus avancés.

## Formats de fichiers utilisés par CryENGINE

Voici quelques types de fichiers courants associés à CryENGINE :

1. **cryproj** : fichiers du projet CryENGINE. Ces fichiers stockent les paramètres et configurations spécifiques au projet pour un projet de jeu particulier.
    




















2. **.level** : les fichiers de niveau contiennent des données du monde du jeu 3D, notamment le terrain, les objets, l'éclairage et d'autres paramètres spécifiques au niveau. Les niveaux sont un élément fondamental de la conception de jeux dans CryENGINE.
    




















3. **.cgf** : Format de géométrie des caractères. Ces fichiers contiennent des données de modèle 3D pour les personnages, les objets et d'autres éléments du jeu. Les fichiers CGF peuvent inclure des données de géométrie, de textures et d'animation.
    




















4. **.chrparams** : fichiers de paramètres de caractères. Ces fichiers stockent les paramètres et configurations des modèles de personnages et de leurs animations.
    




















5. **.dds** : format de texture DirectX. CryENGINE utilise couramment des fichiers DDS pour stocker des textures, notamment des cartes diffuses, des cartes normales et d'autres types de textures.
    




















6. **.cryshader** : fichiers CryENGINE Shader. Ces fichiers définissent la manière dont les matériaux et les objets sont rendus dans le monde du jeu, en spécifiant les shaders, les propriétés des matériaux, etc.
    




















7. **.crytif** : fichier d'informations sur les textures. Ces fichiers stockent des informations supplémentaires sur les textures, telles que les paramètres de compression, les mipmaps et d'autres détails liés aux textures.
    




















8. **.cdf** : Fichier de définition de personnage. Les fichiers CDF sont utilisés pour définir les ressources des personnages et leurs propriétés, y compris les pièces jointes, les états d'animation et les paramètres liés aux personnages.
    




















9. **.dds** : CryENGINE utilise également des fichiers DDS (DirectDraw Surface) pour diverses cartes de texture, telles que les cartes normales, les cartes spéculaires et les cartes diffuses.
    




















10. **.anim** : fichiers d'animation. Ces fichiers stockent des données d'animation pour les personnages et les objets, notamment les images clés, les positions des os et les séquences d'animation.
    




















11. **.xml** : les fichiers XML peuvent être utilisés pour diverses configurations et définitions de données dans CryENGINE, telles que la logique du jeu, le comportement de l'IA, etc.
    




















12. **.pak** : [fichiers PAK](/fr/game/pak/) sont des fichiers d'archives utilisés pour regrouper les ressources et les ressources du jeu, ce qui le rend plus efficace pour la distribution et le chargement du jeu.

## Comment ouvrir le fichier CHR?

Les programmes qui ouvrent les fichiers CHR incluent

- **Crytek CryENGINE SDK** (essai gratuit) pour Windows

**Sous-type :** Fichiers d'images 3D

## Autres fichiers CHR

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.chr**.

**3D**
- [CHR - Fichier de personnage CryENGINE](/fr/3d/chr-cryengine/)
- [CHR - Fichier de personnages 3ds Max](/fr/3d/chr-3ds/)

**Police et jeu**
- [CHR - Jeu de caractères Borland](/fr/font/chr/)
-[CHR - Club de littérature Doki Doki ! Fichier de personnage](/fr/game/chr-doki/)

## Les références
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

