{
  "date" : "2019-10-11",
  "keywords" :[ "chm","fichier chm", "format de fichier chm", "type de fichier chm", "fichier", "type", "qu'est-ce qu'un fichier chm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - Format de fichier d'aide HTML compilé",
  "description" :"Découvrez ce qu'est un fichier CHM et les API qui peuvent les créer et les ouvrir.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier CHM ?

Le format de fichier CHM représente le fichier d'aide Microsoft **[HTML](/fr/web/html/)** qui se compose d'un ensemble de pages HTML. Il fournit un index pour accéder rapidement aux rubriques et naviguer dans les différentes parties du document d'aide. Le fichier CHM peut être recherché pour son contenu via l'option de recherche fournie. CHM est un format de fichier d'aide en ligne propriétaire de Microsoft qui est souvent utilisé pour la documentation des logiciels. En outre, il est utilisé dans plusieurs autres applications telles que des guides de formation, des livres interactifs et des bulletins électroniques. La plupart des environnements de développement Microsoft modernes prennent en charge la génération de documentation CHM à partir des informations disponibles dans l'application.

La capacité unique du format de fichier CHM à implémenter une table des matières et un index combinés le distingue des autres pages HTML standard. Le fichier CHM généré est de taille relativement petite et, par conséquent, peut facilement être distribué avec des progiciels. L'outil de création d'aide, HTML Help Workshop, fournit un système facile à utiliser pour créer et gérer des projets d'aide et leurs fichiers associés. Les fichiers CHM peuvent inclure du texte, des images et des hyperliens ; visualisable dans un navigateur Web ; utilisé par Windows et d'autres programmes comme solution d'aide en ligne.

## Format de fichier CHM

La forme finale du fichier CHM généré dépend de la façon dont le système d'aide est conçu et s'il est destiné à une application ou à un site Web. Un fichier CHM prend en charge la compression des données avec la compression LZX pour générer les fichiers HTML compressés. Il a le moteur de recherche intégré pour une recherche rapide de contenu ainsi que la possibilité de fusionner plusieurs fichiers .CHM. Un fichier CHM se compose d'un ensemble de fichiers HTML, d'une table des matières liée et d'un fichier d'index.

### Fichiers HTML

Que vous créiez des rubriques d'aide à distribuer avec un programme ou sur le Web, les documents que vous créez sont créés à l'aide d'un langage de formatage spécial appelé Hypertext Markup Language (HTML). Les fichiers de rubrique HTML ont une extension de nom de fichier .htm ou .html.

Bien que chaque rubrique d'aide ou page Web que vous créez semble être un document contenant du texte, des graphiques ou des images animées, les fichiers .htm sont en fait des documents texte qui ont des codes de formatage HTML spéciaux. Ces codes, appelés balises, indiquent au navigateur comment afficher chaque page. Seul le texte qui apparaît dans une rubrique ou une page Web se trouve réellement dans le fichier .htm. Tous les graphiques, sons, images animées ou autres éléments qui apparaissent sont des fichiers distincts vers lesquels pointe votre fichier HTML. Le navigateur copie ou télécharge les graphiques, les sons ou d'autres éléments lorsqu'il voit les balises lui demandant de le faire.

### Table des matières (TOC)
Le fichier de table des matières de l'aide (.hhc) est un fichier HTML qui contient les titres de rubrique de votre table des matières. Lorsqu'un utilisateur ouvre la table des matières dans un fichier d'aide compilé (ou sur une page Web) et clique sur un titre de rubrique, le fichier HTML associé à ce titre s'ouvre.

### Fichier d'index
Le fichier d'index (.hhk) est un fichier HTML qui contient les entrées d'index (mots clés) de votre index. Lorsqu'un utilisateur ouvre l'index dans un fichier d'aide compilé ou sur une page Web et clique sur un mot-clé, le fichier HTML associé au mot-clé s'ouvre.

## Composants d'aide HTML

L'aide HTML est composée de plusieurs composants. Il s'agit notamment des éléments suivants :

* `HTML Help Workshop`: un outil de création d'aide avec une interface graphique facile à utiliser pour créer des fichiers de projet, des fichiers de rubrique HTML, des fichiers de contenu, des fichiers d'index et tout ce dont vous avez besoin pour créer un système d'aide en ligne ou un site Web .
* `HTML Help ActiveX control` : un petit programme modulaire utilisé pour insérer la navigation d'aide et la fonctionnalité de fenêtre secondaire dans un fichier HTML.
* `La visionneuse d'aide HTML` : une fenêtre à trois volets entièrement fonctionnelle et personnalisable dans laquelle les rubriques d'aide en ligne peuvent apparaître.
* `Microsoft HTML Help Image Editor` : un outil graphique en ligne pour créer des captures d'écran ; et pour convertir, éditer et visualiser des fichiers image.
* `The HTML Help Java Applet` : un petit programme basé sur Java qui peut être utilisé à la place d'un contrôle ActiveX pour insérer une navigation d'aide dans un fichier HTML.
* `Le programme exécutable de l'aide HTML` : le programme qui affiche et exécute l'aide lorsque vous cliquez sur un fichier d'aide compilé.
* `Le compilateur d'aide HTML` : le programme qui compile le projet, le contenu, l'index, la rubrique et d'autres fichiers dans un fichier d'aide compilé.
* `The HTML Help Authoring Guide` : un guide en ligne conçu pour aider les auteurs d'aide à utiliser l'aide HTML pour concevoir un système d'aide. Le guide contient également une référence d'aide HTML complète pour les développeurs et une référence de balise HTML pour les auteurs.

## Références

* [Aide Microsoft HTML](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Aide HTML compilée Microsoft](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

