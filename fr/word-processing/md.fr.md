{
  "date" : "2019-10-11",
  "keywords" :[ "fichier md", "format de fichier md", "qu'est-ce qu'un fichier md", "fichier", "exemple md", "extension de fichier md","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - Fichier de langage MarkDown",
  "description":"En savoir plus sur le format de fichier MD et les API qui peuvent créer et ouvrir des fichiers MD.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier MD ?

Les fichiers texte créés avec les dialectes du langage Markdown sont enregistrés avec l'extension de fichier **.md** ou **.MARKDOWN**. Les fichiers MD sont enregistrés au format texte brut qui utilise le langage Markdown qui comprend également des symboles de texte en ligne, définissant la manière dont un texte peut être formaté, comme les indentations, le formatage des tableaux, les polices et les en-têtes. Les fichiers MD peuvent être convertis en HTML avec un programme appelé Markdown. Le langage Markdown est publié par John Gruber.

Les fichiers MD peuvent également être classés en tant que fichiers de développement qui sont principalement utilisés par Markdown, pour convertir des fichiers texte en versions HTML afin que les utilisateurs puissent créer des fichiers faciles à lire et à écrire. Voici les applications qui peuvent ouvrir un fichier .md :

* Bloc-notes Microsoft
* Bloc-notes2
* Apple TextEdit
* Microsoft Word Pad

Une mise en garde est de ne pas renommer l'extension des fichiers .md. Si c'est le cas, cela ne changera pas le type de fichier car il existe des logiciels de conversion spéciaux disponibles pour changer un fichier d'un type à un autre. Comme indiqué ci-dessus, les fichiers .MD sont les extensions de fichiers créés par le logiciel de langage Markdown. **Markdown** est un [langage de balisage léger](https://en.wikipedia.org/wiki/Lightweight_markup_language) destiné à un seul usage, à utiliser pour formater du texte sur le Web avec une syntaxe de formatage de texte brut. Qu'il soit clair que Markdown ne remplace pas HTML car sa syntaxe est très petite, contenant un très petit sous-ensemble de balises HTML. La raison derrière le Markdown est de faciliter la lecture, l'écriture et l'édition de prose. En d'autres termes, nous pouvons dire que HTML est un format de publication tandis que Markdown est un format d'écriture.

Markdown est aujourd'hui l'un des langages de balisage les plus populaires au monde. Lors de l'utilisation de Microsoft Word, le formatage des mots et des phrases se fait en cliquant sur des boutons et les modifications sont immédiatement visibles. Mais Markdown n'est pas comme ça. Lorsque le fichier au format Markdown est créé, la syntaxe Markdown est ajoutée au texte pour indiquer quels mots et expressions peuvent sembler différents. Par exemple, pour afficher un titre, un signe dièse est ajouté avant celui-ci (par exemple # Titre Un). Pour faire une phrase en gras, deux astérisques sont ajoutés avant et après (par exemple, **ce texte est en gras**). La syntaxe Markdown peut être vue après un certain temps dans le texte.

## Bref historique

John Gruber et Aaron Swartz ont créé en 2004 le langage Markdown avec l'idée de permettre aux gens "d'écrire en utilisant un format de texte brut facile à lire et à écrire et avec la possibilité de le convertir en XHTML ou HTML. L'objectif derrière sa conception est la lisibilité - le langage est lisible tel quel, sans donner l'impression qu'il a été balisé ou ajouté avec des instructions de formatage comme cela se fait dans les langages de balisage comme RTF ou HTML où les balises et les instructions de formatage sont évidentes. L'inspiration de base consiste à utiliser les conventions existantes pour marquer le texte brut dans les e-mails.

Depuis lors, Markdown a également été réimplémenté par d'autres, comme dans un [module](https://en.wikipedia.org/wiki/Modular_programming) Perl disponible sur [CPAN](https://en.wikipedia.org/wiki/CPAN) et dans divers autres langages de programmation. Il est distribué sous une [licence de type BSD](https://en.wikipedia.org/wiki/BSD_license) et est inclus ou disponible en tant que plug-in pour plusieurs [systèmes de gestion de contenu](https://en.wikipedia.org/wiki/Content_management_system).

## Spécifications techniques

Lorsque quelque chose est écrit dans Markdown, le texte est d'abord stocké dans un fichier en clair avec une extension de .md ou .markdown, puis une application de démarquage telle que Dillinger est utilisée pour le traitement du fichier Markdown afin de convertir le texte au format Markdown en HTML pour l'afficher sur le Web. navigateurs. Les applications Markdown utilisent un //processeur Markdown// (aussi communément appelé « analyseur » ou « implémentation ») pour prendre le texte au format Markdown et le sortir au format HTML. Le diagramme de flux du processus est le suivant :

En bref, il s'agit d'un processus en quatre étapes comme suit :

1. Tout d'abord, création de fichiers Markdown avec un éditeur de texte ou une application Markdown avec une extension .md ou .markdown.
1. Le fichier Markdown est ensuite ouvert dans une application Markdown.
1. L'application Markdown est utilisée pour convertir le fichier Markdown en un document HTML.
1. Le fichier HTML est ensuite visualisé dans un navigateur Web ou une application Markdown est utilisée pour le convertir dans un autre format de fichier, tel que PDF.

Markdown est rapide et facile à prendre des notes, à écrire du contenu pour le site Web, à produire des documents prêts à imprimer, à publier des livres, à générer des présentations et à créer des documents.

Certaines des versions en démarque ont eu un impact substantiel sur d'autres versions à tel point qu'on les verra souvent citées comme faisant partie d'autres versions. Par exemple, les bibliothèques mentionnent le support de CommonMark (GFM). Jetons un bref coup d'œil à ceux-ci.

### GFM
Markdown est si populaire auprès des développeurs parce que la plate-forme de partage open source Github a accepté et étendu le langage avec une version appelée Github Flavored Markup (GFM) qui comprend des blocs de code clôturés, des URL aultlinking, des barrés, des tableaux et des tâches de création.

### CommonMark
Les développeurs de Markdown ont récemment essayé de normaliser le markdown, ils se sont regroupés pour créer une version, des tests et une documentation du langage plus robuste et s'appelle CommonMark. Ce format est un peu nouveau et ne prend pas en charge beaucoup de fonctionnalités, mais bientôt de nombreuses fonctionnalités MultiMarkdown seront ajoutées.

### Multi-Markdown
Multi-Markdown a ajouté diverses fonctionnalités au langage qui sont prises en charge par d'autres versions. À l'origine, il a été écrit en Perl, mais a ensuite été déplacé vers C. Il prend en charge les blocs de code clôturés, la coloration syntaxique, les tableaux, les métadonnées, les fragments/liens de références croisées, les notes de bas de page, le barré, les listes de définitions, les mathématiques.

## Références

* [Maîtriser MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

