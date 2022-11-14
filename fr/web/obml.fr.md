{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier OBML - Fichier de page Web enregistré Opera Mini",
  "description" :"Découvrez ce qu'est un fichier OBML et les API qui peuvent créer et ouvrir un fichier OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Qu'est-ce qu'un fichier OBML ?

Un fichier OBML (Opera Binary Markup Language) est une version hors ligne d'une page Web enregistrée par le navigateur Web mobile Opera Mini. Il s'agit d'une version compacte et autonome des fichiers [HTML](/fr/web/html/) qui contient tous les éléments de la page à afficher sur des appareils spécifiques en mode hors connexion. Le format de fichier OBML a été mis à niveau vers plusieurs versions, OBML15 et OBML16 étant largement utilisés. Un point important à garder à l'esprit est que chaque version d'Opera Mini n'est compatible qu'avec un seul format OBML. Ainsi, la mise à niveau d'Opera Mini laissera lisibles les pages précédemment enregistrées. Les fichiers OBML peuvent être convertis en HTML et [PDF](/fr/pdf/).

## Format de fichier OBML

Le format de fichier OBML est enregistré dans le format de fichier propriétaire d'Opera et ses spécifications de format de fichier ne sont pas disponibles publiquement. Cependant, [le format OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) a été rétro-conçu pour décoder sa structure comme suit.

### Types de données OBML

Selon les résultats de la rétro-ingénierie, OBML utilise les types primitifs suivants :

* `byte` - entier non signé (1 octet)
* `short` - entier signé (2 octets, gros boutien)
* `medium` - entier signé (3 octets, gros boutien)
 * `blob` – { length: short, data: byte[length] }
* `char` - un octet contenant un caractère ASCII
* `string` - un blob contenant du texte encodé en UTF-8

### En-tête OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## Références

* [Format OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

