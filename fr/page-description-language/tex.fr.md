{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier TEX",
  "description":"En savoir plus sur le format de fichier TEX et les API qui peuvent créer et ouvrir des fichiers TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier TEX ? ##

**TeX** est un langage qui comprend de la programmation ainsi que des fonctionnalités de balisage, utilisé pour composer des documents. Donald Knuth, de l'Université de Stanford, est le créateur de ce système de composition ingénieux. Partout dans le monde, TeX est le choix ultime des auteurs et des éditeurs pour produire des documents techniques de haute qualité. TeX effectue un travail remarquable de formatage d'expressions mathématiques complexes. En conjonction avec une photocomposeuse de haute qualité, TeX rivalise avec les résultats générés par les meilleurs systèmes de composition traditionnels. Par conséquent considéré comme les systèmes typographiques numériques les plus classiques.

Les fichiers d'entrée TeX sont basés sur le code ASCII, permettant ainsi le partage de manuscrits entre auteurs, directeurs de publication et critiques. Une grande variété d'environnements informatiques, presque toutes les plates-formes modernes et de nombreuses plates-formes plus anciennes prennent en charge TeX. De plus, TeX est un logiciel gratuit, disponible pour un large éventail de consommateurs. De nombreuses installations UNIX utilisent à la fois troff UNIX et TeX comme système de formatage à des fins différentes. D'autres tâches de composition sont exécutées énormément sous la forme de LaTeX, ConTeXt et d'autres packages de macros.

## Bref historique ##

TeX a été conçu et écrit par Donald Knuth en 1978. Guy Steele du Massachusetts Institute of Technology a révisé les entrées/sorties de TeX pour le faire fonctionner sous le système d'exploitation incompatible comme Timesharing System (ITS). La première version de TeX a été développée sous le système d'exploitation WAITS de Stanford dans le langage de programmation (SAIL) et testée pour fonctionner sur un PDP-10. Knuth a introduit l'idée de la programmation littéraire pour les versions avancées. La programmation littéraire est un moyen de générer un code source compilable et composé (en TeX) pour une documentation croisée à l'aide du fichier d'origine. Le langage utilisé pour développer ces versions avancées de TeX s'appelle WEB, un mélange de programmes Pascal DEC PDP-10 pour assurer la portabilité.

Une nouvelle version révisée de TeX publiée en 1982 et s'appelait TeX82. Le changement majeur est le remplacement de l'algorithme de césure d'origine par l'algorithme nouvellement écrit par Frank Liang. Pour assurer la portabilité sur différentes plates-formes, au lieu d'utiliser la virgule flottante, TeX82 utilise l'arithmétique en virgule fixe avec un langage de programmation réel et complet. En 1989, une nouvelle version de TeX et Metafont est sortie. Ainsi, la version 3.0 de TeX facilite les entrées 8 bits, autorisant 256 caractères différents dans le texte. Après la version 3, les mises à jour sont indiquées en ajoutant un chiffre supplémentaire à la fin de la décimale, par exemple la version actuelle de TeX est indiquée comme 3.14159265. Cette version a été mise à jour pour la dernière fois le 12-1-2014.

## Entrée TeX ##

Un fichier d'entrée dans TEX peut être préparé avec un éditeur de texte en utilisant du texte ordinaire. Contrairement à un traitement de texte typique, ce fichier d'entrée interdit tout caractère de contrôle invisible. Un fichier peut être incorporé dans un autre fichier, contenant des définitions de macros et des définitions auxiliaires qui améliorent les capacités de TeX. Si une installation de TeX est livrée avec des fichiers de macro, les informations locales sur TeX montrent comment utiliser les fichiers de macro. La forme standard de TeX intègre une combinaison de macros et d'autres définitions connues sous le nom de plain TEX.

Sur la base d'une connaissance précise des tailles de tous les caractères et symboles, il calcule l'organisation optimale des lettres par ligne et des lignes par page. Au moment du traitement du document, un fichier .dvi est produit, où « dvi » signifie « indépendant de l'appareil ». Des programmes de pilote de périphérique sont nécessaires pour imprimer ou prévisualiser le document avec une extension dvi. De nos jours, la génération dvi est contournée par un pdf-TeX couramment utilisé. Aucune connaissance préalable des polices n'est disponible dans l'installation de TeX, donc les fichiers de polices externes, qui font partie de l'environnement TeX local, sont utilisés pour obtenir des informations pour le document.

## Système de composition ##

Environ 300 primitives (commandes) peuvent être comprises par le système TeX de base. Les primitives sont des commandes de bas niveau, par conséquent, un utilisateur commun les utilise rarement directement et la plupart des fonctionnalités sont exécutées par des fichiers de format. Ces fichiers de format sont des images mémoire préchargées de TeX qui sont suivies du chargement de grandes collections de macros. Le format par défaut d'origine du langage, c'est-à-dire plain TeX, ajoute environ 600 commandes.

Une barre oblique inverse groupée avec des accolades indique le début des commandes TeX. Étant donné que TeX est un langage basé sur des macros et des jetons, presque toutes les caractéristiques syntaxiques de TeX peuvent être modifiées au moment de l'exécution, y compris celles définies par l'utilisateur, à l'exception des jetons non extensibles qui sont ensuite exécutés. L'expansion elle-même est pratiquement sans problème. Certaines commandes doivent venir après des arguments qui aident à expliquer la fonction d'une commande. Par exemple, la commande \vskip ordonne à TEX de sauter vers le bas/vers le haut de la page suivi d'un argument déterminant la quantité d'espace à sauter.

## Versions ##

LaTeX est le format le plus fréquemment utilisé qui a été développé à l'origine par Leslie Lamport. LaTeX intègre différents styles de documents pour les fichiers, les lettres, les livres et les diapositives et propose un référencement et une numérotation automatique pour différentes sections et expressions mathématiques. AMS-TeX est un autre format populaire, développé par l'American Mathematical Society.

AMS-TeX offre des commandes beaucoup plus conviviales, qui peuvent être redéfinies par les revues pour s'adapter à leur style local. LaTeX peut profiter des avantages d'AMS-TeX en utilisant les "paquetages" AMS qui sont alors appelés AMS-LaTeX. ConTeXt est un autre format écrit par Hans Hagen utilisé principalement pour la publication assistée par ordinateur.

Le logiciel TeX offre plusieurs fonctionnalités qui n'étaient pas disponibles, ou de moindre qualité, dans d'autres systèmes de composition au moment de sa création. Certaines des caractéristiques innovantes de ce langage reposent sur des algorithmes intéressants dérivés des thèses des étudiants de Knuth. Alors que d'autres programmes de composition intègrent maintenant des fonctionnalités utiles de TeX dans leurs programmes.

## Références ##

* [Système de composition TeX](https://en.wikipedia.org/wiki/TeX)

