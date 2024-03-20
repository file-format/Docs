{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Spécifications du papier XML", "Fichier", "Extension", "Format de fichier", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Format de fichier de mise en page",
  "description":"En savoir plus sur le format de fichier XPS et les API qui peuvent créer et ouvrir des fichiers XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Qu'est-ce qu'un fichier XPS ? ##

Un fichier XPS représente des fichiers de mise en page basés sur les spécifications papier XML créées par Microsoft. Il a été développé en remplacement du format de fichier EMF et est similaire au format de fichier [PDF](/fr/pdf/), mais utilise XML dans la mise en page, l'apparence et les informations d'impression d'un document. Il est, en fait, plus justifié de dire que XPS est une tentative sur PDF, mais qu'il n'a pas pu obtenir suffisamment de popularité en tant que propriété de PDF pour de nombreuses raisons. Microsoft fournit XPS Document Writer par défaut à partir de Windows 7 pour la création de fichiers XPS. Les fichiers XPS peuvent être générés en sélectionnant "Microsoft XPS Document Writer" comme imprimante lors de l'impression du document.

Les visionneuses XPS sont intégrées dans Windows Vista, Windows 7, Windows 8 et Internet Explorer 6 ou version ultérieure. Les fichiers XPS deviennent en lecture seule une fois qu'ils sont générés. Cela ajoute à la confiance de l'utilisateur dans les documents reçus envoyés en tant que XPS pour l'authenticité du document. Un document XPS peut contenir une ou plusieurs pages converties à partir du document d'origine.

## Bref historique ##

Microsoft a soumis la spécification XPS à Ecma International. En juin 2007, le comité technique Ecma 46 (TC46) a été créé pour développer une norme basée sur les spécifications papier OpenXPS. Ecma International a approuvé la norme Ecma (ECMA-388) [spécifications XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) en juin 2009 lors de la 97e Assemblée générale.

## Format de fichier XPS ##

Le format XPS consiste en un balisage XML qui définit la composition d'un document et l'apparence visuelle de chaque page ainsi que des règles de rendu pour l'affichage ou l'impression du document. Il conserve toutes les informations pour recréer un document sur n'importe quel système, ce qui le rend indépendant des ressources disponibles sur ce système. Le format est essentiellement une archive ZIP et si vous renommez l'extension de fichier en ZIP, vous verrez les fichiers constitutifs qui contiennent les données du document. Ces documents comprennent :

* Fichiers de page de document (.fpage) - Contient le contenu du document et les paramètres de format du document. Chaque page d'un document XPS contient un fichier FPAGE.
* Fichier de paramètres de document (.fdoc) - Stocke les paramètres inclus dans l'archive XPS.
* Fichiers de fragment de document (.frag) - Définit les paramètres du fichier XPS réel et chaque page du document a son propre fichier .frag.

{{< figure src="../XPS-1.png" alt="Format de fichier XPS" >}}

Ces fichiers conservent le contenu du document de telle sorte que si, par exemple, quelqu'un n'a pas les mêmes polices installées sur sa machine, le visualiseur XPS affichera toujours ces polices d'origine. Cela implique l'inclusion d'un fichier de balisage XML pour chacun :

* Page
* Texte
* Polices intégrées
* Images matricielles
* Graphiques vectoriels 2D
* Gestion des droits numériques

Le format de document XPS comprend un ensemble bien défini de parties et de relations, chacune remplissant un objectif particulier dans le document. Le format étend également les fonctionnalités du package, y compris les signatures numériques, les vignettes et l'entrelacement.

Un document XPS typique se présente comme suit et peut être analysé à la lumière du format de fichier XPS spécifications.

{{< figure src="../XPS-2.png" alt="Format de fichier XPS" >}}


## Références ##

* [Spécifications du format de fichier XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - Par Wikipédia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)
