{
"date": "2023-09-27",
  "keywords": [
"cfg",
"fichier cfg",
"fichier de configuration cfg celestia",
"qu'est-ce qu'un fichier cfg",
"comment ouvrir le fichier cfg",
"déposer",
"extension de fichier cfg",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier CFG - Fichier de configuration Celestia",
  "description":"Découvrez le format de fichier de configuration CFG Celestia et les API permettant de créer et d'ouvrir des fichiers CFG.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent" : "settings"
}
},
"lastmod": "2023-09-27"
}

## Qu'est-ce qu'un fichier CFG ?

Un fichier de configuration Celestia est un fichier texte brut utilisé par Celestia, programme de simulation d'univers 3D. Ces fichiers sont essentiels pour personnaliser le comportement de Celestia, les objets célestes affichés et la façon dont le programme apparaît. Cependant, la modification de ces fichiers nécessite une attention particulière, car des modifications inappropriées peuvent perturber le processus de chargement de Celestia, l'empêchant de fonctionner correctement.

## Célestia

Celestia est un logiciel de simulation d'astronomie 3D gratuit et open source qui permet aux utilisateurs d'explorer et de visualiser l'univers de manière hautement réaliste et interactive. Il a été développé par Chris Laurel et a été publié pour la première fois au début des années 2000. Celestia est disponible pour les systèmes d'exploitation Windows, macOS et Linux.

Les principales caractéristiques et aspects de Celestia comprennent :

- **Visualisation 3D réaliste :** Celestia fournit une représentation détaillée et précise de notre système solaire, ainsi que des étoiles, des galaxies et d'autres objets célestes. Il utilise des modèles et des textures 3D de haute qualité pour créer une expérience visuellement immersive.

- **Base de données céleste étendue :** Le logiciel est livré avec une vaste base de données intégrée d'objets célestes connus, notamment des étoiles, des planètes, des lunes, des astéroïdes, des comètes et des vaisseaux spatiaux. Les utilisateurs peuvent facilement localiser et explorer ces objets.

- **Précision scientifique :** Bien que Celestia soit un outil de visualisation, il vise à représenter les objets et phénomènes célestes aussi précisément que possible, sur la base des données scientifiques disponibles.

## Formats de fichiers utilisés par Celestia

Celestia utilise différents formats de fichiers pour différents aspects de sa simulation d'astronomie 3D. Voici quelques-uns des principaux formats de fichiers utilisés par Celestia :

1. **Fichiers de configuration (.cel)**
- *Description* : fichiers en texte brut permettant aux utilisateurs de personnaliser le comportement, l'apparence et le contenu de Celestia.
- *Objectif* : Personnalisation des paramètres, définition des emplacements et spécification des objets célestes.

2. **Modèles et maillages 3D**
- *Formats* : [.3ds](/fr/3d/3ds/), [.obj](/fr/3d/obj/), [.dae](/fr/3d/dae/), .ac
- *Description* : formats de fichiers de modèles 3D pris en charge utilisés pour le rendu des corps célestes et des vaisseaux spatiaux.
- *Objectif* : Afficher des objets 3D dans Celestia.

3. **Fichiers de textures**
- *Formats* : [.jpg](/fr/image/jpeg/), [.png](/fr/image/png/), [.dds](/fr/image/dds/)
- *Description* : Ces fichiers fournissent des textures de surface pour les corps célestes.
- *Objectif* : Mapper des textures sur des modèles 3D pour une apparence réaliste.

4. **Catalogues Star et fichiers de données**
- *Formats* : formats personnalisés, [.csv](/fr/spreadsheet/csv/), [.tsv](/fr/spreadsheet/tsv/)
- *Description* : Fichiers de données utilisés pour représenter les étoiles et autres objets célestes, garantissant une simulation précise.
- *Objectif* : Représentation précise des objets célestes.

5. **Cartes de cubes de texture**
- *Description* : Les cartes cubiques sont utilisées pour simuler l'apparence d'objets célestes lointains comme les galaxies.
- *Objectif* : Rendu d'objets distants avec des textures réalistes.

6. **Fichiers de script**
- *Description* : Ces fichiers contiennent des scripts personnalisés écrits dans le langage de script de Celestia.
- *Objectif* : Permettre aux utilisateurs de créer des événements et des animations dynamiques au sein de l'univers de Celestia.

## Fichier de configuration Celestia

Voici un aperçu de base de ce que vous pouvez faire avec le fichier de configuration de Celestia :

1. **Définition de votre emplacement** : vous pouvez spécifier votre emplacement sur Terre à l'aide des paramètres de latitude, de longitude et d'altitude. Cela permet à Celestia d'afficher avec précision le ciel nocturne depuis votre position.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Personnalisation de vos options d'affichage :** Vous pouvez ajuster diverses options d'affichage telles que le champ de vision, les paramètres d'heure et les préférences de rendu.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Chargement d'objets célestes :** Vous pouvez ajouter des objets célestes tels que des étoiles, des planètes, des astéroïdes, des vaisseaux spatiaux et bien plus encore à votre simulation. Chaque objet est défini dans le fichier de configuration avec ses propriétés.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Définir des vaisseaux spatiaux :** Vous pouvez créer votre propre vaisseau spatial fictif ou en utiliser de vrais en spécifiant leurs paramètres tels que la position, l'orientation et les modèles 3D.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Création de scripts :** Vous pouvez écrire des scripts dans le langage de script personnalisé de Celestia pour créer des événements et des animations dynamiques.

## Comment ouvrir le fichier CFG?

Programmes qui ouvrent ou référencent des fichiers CFG

- Celestia (gratuit) pour (Windows, Mac, Linux)

## Autres fichiers CFG

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.cfg**.

**Paramètres**
- [CFG - Fichier de configuration Celestia](/fr/settings/cfg-celestia/)
- [CFG - Fichier de connexion au serveur Citrix](/fr/settings/cfg-citrix/)
- [CFG - Fichier de configuration MAME](/fr/settings/cfg-mame/)
- [CFG - Fichier de configuration LightWave](/fr/settings/cfg-lightwave/)

**Jeu**
- [CFG - Fichier de langage de balisage Wesnoth](/fr/game/cfg-wesnoth/)
- [CFG - Fichier de configuration MUGEN](/fr/game/cfg-mugen/)
- [CFG - Fichier de configuration du moteur source](/fr/game/cfg-sourceengine/)

**Système et divers**
- [CFG - Fichier CFG](/fr/system/cfg/)
- [CFG - Fichier de configuration du modèle Cal3D](/fr/misc/cfg-cal3d/)

## Les références
* [Célestia](https://en.wikipedia.org/wiki/Celestia)

