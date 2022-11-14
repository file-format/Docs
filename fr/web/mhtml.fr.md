{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","fichier mhtml", "format de fichier mhtml", "type de fichier mhtml", "fichier", "type", "qu'est-ce qu'un fichier mhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - Fichier HTML MIME",
  "description":"En savoir plus sur le format de fichier MHTML et les API qui peuvent créer et ouvrir des fichiers MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier MHTML ?

Les fichiers avec l'extension MHTML représentent un format d'archive de page Web qui peut être créé par un certain nombre d'applications différentes. Ce format est appelé format d'archive, car il enregistre le code Web **[HTML](/fr/web/html/)** et les ressources associées dans un seul fichier. Ces ressources incluent tout ce qui est lié à la page Web, comme les images, les applets, les animations, les fichiers audio, etc. Les fichiers MHTML peuvent être ouverts dans une variété d'applications telles qu'Internet Explorer et Microsoft Word. Microsoft Windows utilise le format de fichier MHTML pour enregistrer les scénarios de problèmes observés lors de l'utilisation de toute application sous Windows qui pose des problèmes. Le format de fichier MHTML encode le contenu de la page de manière similaire aux spécifications définies dans message/rfc822, qui sont des spécifications relatives aux e-mails en texte brut. Les spécifications réelles du format sont détaillées dans la [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Format de fichier MHTML

MHTML est également connu sous le nom d'encapsulation MIME de documents HTML agrégés pour sa capacité à encoder des pages Web HTML avec ses ressources dans une seule archive Web. Selon les spécifications RFC 2557, un document agrégé est un message encodé MIME qui contient une ressource racine (objet) ainsi que d'autres ressources qui lui sont liées via des URI. Ces autres ressources peuvent être la représentation d'images en ligne, de feuilles de style, d'applets, etc. De plus, celles-ci peuvent être la racine d'autres documents multimédias. Les spécifications complètes du document pour le format de fichier MHTML sont détaillées dans la [RFC 2557](https://tools.ietf.org/html/rfc2557) et doivent être consultées pour tout type de développement d'application pour la lecture/l'écriture de ce format de fichier. La norme spécifie que les parties de corps à référencer peuvent être identifiées soit par un Content-ID, soit par un Content-Location.

### En-têtes de contenu MIME

Un en-tête de contenu MIME, Content-Location, est défini pour résoudre les références URI aux ressources dans d'autres parties du corps. Cet en-tête peut apparaître dans n'importe quel en-tête de message ou de contenu.

### En-tête de l'emplacement du contenu

Un Content-Location est une représentation d'un URI qui étiquette le contenu d'une partie de corps où il est placé. Sa valeur peut être un URI absolu ou relatif. Il peut être utilisé pour étiqueter une ressource qui n'est pas récupérable par certains ou tous les destinataires d'un message. Un seul message ne peut avoir qu'un seul en-tête Content-Location. Exemple d'une structure multipartie/connexe contenant des parties de corps avec à la fois des étiquettes Content-Location et Content-ID :

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI des agrégats MHTML

L'URI de l'agrégat MHTML est différent de celui de son URI racine. Le champ d'en-tête Content-Location doit s'appliquer à l'ensemble de l'agrégat s'il est utilisé dans l'en-tête d'un en-tête multipart/lié. De même, l'ensemble de ressources récupérées peut être différent de l'ensemble de ressources récupérées à l'aide des Content-Locations de ses parties lorsque l'URI faisant référence à l'agrégat MHTML est utilisé pour récupérer cet agrégat. Par exemple, la récupération d'un agrégat MHTML peut renvoyer une ancienne version, tandis que la récupération de l'URI racine et de ses objets liés en ligne peut renvoyer une version plus récente.

## Références

* [Encapsulation MIME de documents agrégés - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Format de fichier MHTML - Par Wikipédia](https://en.wikipedia.org/wiki/MHTML)

