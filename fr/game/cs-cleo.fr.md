{
"date": "04/01/2023",
   "keywords":[
"cs",
"fichier cs",
"script personnalisé cs cleo",
"comment ouvrir un fichier cs",
"déposer",
"extension de fichier CS",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier CS - Script personnalisé CLEO",
   "description":"Découvrez le format de script personnalisé CS CLEO et les API permettant de créer et d'ouvrir des fichiers CS.",
"linktitle": "CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo",
"parent" : "game"
}
},
"lastmod": "2023-01-04"
}

## Qu'est-ce qu'un fichier CS ?

Un fichier .CS dans le contexte de CLEO (abréviation de CLEO Library) fait généralement référence à un fichier de script personnalisé utilisé dans la série de jeux vidéo Grand Theft Auto (GTA). CLEO est un framework de modding populaire qui permet aux joueurs de créer et d'ajouter des scripts personnalisés aux jeux GTA, leur permettant de modifier le gameplay, d'ajouter de nouvelles fonctionnalités et d'améliorer l'expérience de jeu globale.

## Présentation du fichier CS

Voici un aperçu de base de ce qu'un fichier .cs dans CLEO peut contenir :

1. **Code de script** : un fichier .cs contient un code de script écrit dans le langage de script CLEO. Ce langage de script est spécifique à CLEO et est utilisé pour définir le comportement des scripts personnalisés dans le jeu. Le code peut être écrit à l’aide d’un éditeur de texte et suit généralement une syntaxe spécifique.
    









2. **Modifications** : les scripts CLEO peuvent apporter diverses modifications au jeu, telles que changer le comportement des objets du jeu, créer des missions personnalisées, ajouter de nouveaux véhicules, armes et bien plus encore. Les possibilités sont étendues et dépendent de la créativité et des compétences en programmation de l'auteur du scénario.
    









3. **Déclencheurs** : les scripts CLEO incluent souvent des déclencheurs qui déterminent quand et comment le script personnalisé doit s'exécuter. Ces déclencheurs peuvent être basés sur des événements en jeu, les actions des joueurs ou des conditions spécifiques.
    









4. **Variables et fonctions** : les scripts CLEO peuvent utiliser des variables pour stocker et manipuler des données, ainsi que des fonctions pour encapsuler et réutiliser du code. Ces variables et fonctions sont utilisées pour contrôler le comportement du script.

## Exemple de fichier CS

Voici un exemple simple de script CLEO .cs qui modifie la météo dans le jeu :

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## Bibliothèque CLEO

La **Bibliothèque CLEO**, souvent appelée simplement « CLEO », est un framework de modding populaire et puissant pour la série de jeux vidéo Grand Theft Auto (GTA). Il permet aux joueurs et aux moddeurs de créer et d'ajouter des scripts personnalisés aux jeux GTA, leur permettant de modifier le gameplay, d'ajouter de nouvelles fonctionnalités et d'améliorer l'expérience de jeu globale. CLEO est particulièrement connu pour sa flexibilité et sa facilité d'utilisation dans la communauté de modding GTA.

Voici quelques caractéristiques et aspects clés de la bibliothèque CLEO :

1. **Langage de script** : CLEO présente son langage de script, spécifique au framework de modding. Le langage de script est conçu pour être relativement facile à comprendre et à utiliser, le rendant accessible aux moddeurs débutants et expérimentés.
    









2. **Scripts personnalisés** : Avec CLEO, vous pouvez créer des scripts personnalisés pouvant exécuter un large éventail de fonctions dans le monde du jeu. Ces scripts peuvent modifier le comportement dans le jeu, ajouter de nouvelles missions, introduire de nouveaux véhicules ou armes, modifier la physique du jeu et bien plus encore.
    









3. **Déclencheurs et événements** : les scripts CLEO peuvent être déclenchés par divers événements dans le jeu, actions des joueurs ou conditions spécifiques. Cela permet aux moddeurs de créer du contenu dynamique et interactif dans le jeu.
    









4. **Prise en charge de plusieurs versions de GTA** : CLEO propose des versions adaptées à différents jeux GTA, notamment GTA III, GTA Vice City, GTA San Andreas, GTA IV et autres. Cela signifie que les moddeurs peuvent créer et partager leurs scripts personnalisés pour différents titres GTA.

## Formats de fichiers utilisés par la bibliothèque CLEO

Dans le modding CLEO pour les jeux Grand Theft Auto (GTA), plusieurs formats de fichiers sont couramment utilisés pour créer et installer des mods. Ces formats de fichiers servent à diverses fins, allant du contenu de scripts réels au stockage de ressources supplémentaires telles que des textures, des modèles ou de l'audio. Voici quelques-uns des formats de fichiers clés utilisés dans le modding CLEO :

1. **.cs (Custom Script)** : les fichiers CLEO .cs sont des fichiers de script personnalisés écrits dans le langage de script CLEO. Ces fichiers contiennent du code qui définit le comportement et les fonctionnalités du mod. Les fichiers .cs sont au cœur du modding CLEO et sont exécutés par le jeu pour implémenter des fonctionnalités personnalisées.
    









2. **.csa (Custom Script Archive)** : les fichiers .csa sont des archives qui peuvent stocker plusieurs fichiers de script .cs. Ils sont souvent utilisés pour regrouper des scripts associés pour faciliter l’installation et la gestion.
    









3. **.fxt (fichiers texte)** : les fichiers .fxt sont des fichiers texte qui peuvent être utilisés pour localiser ou fournir des traductions de texte pour les mods CLEO. Ils contiennent des chaînes de texte qui peuvent être affichées dans le jeu, rendant les mods accessibles aux joueurs dans différentes langues.
    









4. **[.bmp](/fr/image/bmp/), [.png](/fr/image/png/), [.jpg](/fr/image/jpeg/) (Formats d'image)** : Ces formats d'image sont utilisé pour stocker des textures et des images pour les mods. Ils peuvent être utilisés pour des skins personnalisés, des textures de véhicules, des éléments HUD et bien plus encore. Selon le jeu, différents formats d'image peuvent être préférés.

## Comment ouvrir le fichier CS?

Pour ouvrir et afficher le contenu d'un fichier CLEO .cs (Custom Script), vous pouvez utiliser un éditeur de texte ou un éditeur de code de votre choix. Les choix courants incluent :

- **Notepad** : un éditeur de texte simple préinstallé avec Windows.
- **Notepad++** : Un éditeur de texte plus riche en fonctionnalités conçu pour le codage et les scripts.
- **Visual Studio Code** : un éditeur de code populaire, gratuit et hautement extensible.
- **Sublime Text** : Un autre éditeur de code connu pour sa rapidité et sa polyvalence.
- **Atom** : Un éditeur de code open source développé par GitHub.

## Autres fichiers CS

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.cs**.

**Fichiers de données et jeu**
- [CS - Schéma de couleurs ColorSchemer Studio](/fr/data/cs-colorschemer/)
- [CS - Script personnalisé CLEO](/fr/game/cs-cleo/)

**La programmation**
- [CS - Fichier de code CSharp](/fr/programming/cs/)

## Les références
* [Bibliothèque CLEO](https://cleo.li/)

