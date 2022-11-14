{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "partiel", "extension", "fichier", "format", "web", "Really Simple Syndication","Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Syndication vraiment simple",
  "description":"En savoir plus sur le format de fichier RSS et les API qui peuvent créer et ouvrir des fichiers RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Qu'est-ce qu'un fichier RSS ? ##

Un fichier avec l'extension .rss est appelé Really Simple Syndication. RSS est un type de fichier facilement ou facilement lu par l'ordinateur, le fichier XML. Ces fichiers XML sont automatiquement mis à jour avec toute modification des données ou mise à jour d'un site Web ou d'une page Web. Les informations mises à jour ainsi que les métadonnées (nom de l'auteur, nom de l'éditeur, date de publication, etc.) et les autres contenus Web du site Web sont extraits par les fichiers RSS de l'utilisateur et présentés dans un format facile à lire. La meilleure caractéristique de ces fichiers RSS est qu'ils fonctionnent en temps réel et que les mises à jour, les actualités, les publications, c'est-à-dire les dernières, sont affichées en haut du fichier. À l'aide d'un fichier RSS, vous pouvez facilement créer un fichier contenant les dernières mises à jour de n'importe quel sujet qui vous intéresse, en extrayant le contenu connexe du Web et en le lisant à l'aide d'un fichier RSS.

## Bref historique ##

Dans sa chair, le fichier RSS a d'abord été créé par Netscape, ils ont inventé la première version du fichier RSS mais ont ensuite abandonné l'idée et n'ont pas continué avec les versions plus récentes. C'est alors **Userland Software** qui a travaillé sur le format de fichier RSS et a continué à l'innover avec une version plus récente, c'est ainsi que RSS v2 est arrivé sur le marché. Cependant, l'invention de RSS peut être liée à Resource Description Framework, par Ramanathan V en 1997. Le fonctionnement des deux fichiers est assez similaire et il est prudent de supposer que le concept de RSS a été formé sur la base du fonctionnement de RDF, un lecteur de fichiers qui a été utilisé pour collecter les métadonnées.

## Spécification technique ##

Le fichier RSS est un type de fichier XML et tous les fichiers RSS doivent respecter les normes XML 1.0. Il existe différentes versions de différents fichiers RSS, tels que 0.91, 0.92, 2.0, entre autres. Le fichier de chaque version est conforme aux spécifications et aux normes de cette version spécifique.

## Exemple RSS ##

Voici un exemple simplifié du RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Référence ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
