{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PDF/X",
  "description":"En savoir plus sur le format de fichier PDF/X et les API qui peuvent créer et ouvrir des fichiers PDF/X.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Qu'est-ce qu'un fichier PDF/X ? #

PDF/X est une norme ISO 15930 publiée en 2001 avec un sous-ensemble de fonctionnalités PDF. La norme a été établie et publiée en fonction des exigences spécifiques des industries de l'impression et de l'édition. Les exigences de cette norme ont toutes été conçues en fonction des divers besoins des industries de l'impression et de l'édition. PDF/X exige que les fichiers conformes soient complets, c'est-à-dire autonomes. Cela nécessite que des éléments tels que les polices utilisées dans la page fassent partie du document. Les contenus tels que la 3D ou la vidéo ne peuvent pas faire partie d'un document PDF/X. Les informations contenues dans le document PDF/X doivent être exactes.

## Normes et révisions PDF/X ##

La famille de normes PDF/X comprend plusieurs versions, chacune conçue pour un résultat spécialisé. L'élaboration de ces normes visait à répondre aux nombreux besoins divers des industries de l'imprimerie et de l'édition.

* `PDF/X-1a` - Aussi connu comme le premier standard de la famille PDF/X, PDF/X-1a exige que tout le contenu fasse partie du document PDF afin de pouvoir être imprimé. Les éléments de document tels que les polices, les formulaires, la protection par mot de passe et les annotations visibles ne sont pas autorisés. PDF/X-1a a ses propres exigences spécifiques, telles que celles relatives à la transparence et aux calques qui sont autorisées. Celles-ci exigent également que les éléments d'impression n'utilisent que CMJN, niveaux de gris ou couleurs d'accompagnement, ce qui évite l'utilisation de RVB ou d'espaces colorimétriques indépendants de l'appareil. est destiné aux échanges dans lesquels tous les fichiers doivent être livrés en CMJN (et/ou couleurs d'accompagnement), sans données RVB ou de gestion des couleurs. PDF/X-1a est également appelé échange complet en raison de l'exhaustivité des informations requises par
* `PDF/X-3` - a été introduit en 2002 et a levé de nombreuses restrictions de PDF/X-1a. Cela a permis aux graphiques d'un PDF/X-3 d'utiliser les espaces colorimétriques CMJN, grescale, RVB, Lab et ICC. Il est en fait basé sur les normes PDF 1.3 avec [profil ICC](https://en.wikipedia.org/wiki/ICC_Profile). Il est également appelé gestion des couleurs en raison de la flexibilité et des règles qu'il introduit concernant les couleurs incluses dans un document PDF.
* `PDF/X-4` - prend en charge les transparences, donc PDF-X/4 contient toutes les données requises pour la sortie sans aplatissement.
* `PDF/X-5` - est basé sur PDF/X-4, ajoutant la prise en charge des graphiques externes via XObjects de référence, ainsi que des profils de n-colorant externes pour l'intention de rendu. Utilisez-le pour l'échange partiel de données d'impression à l'aide de la version PDF 1.6

## Références ##

* [PDF/X - Par Wikipédia](https://en.wikipedia.org/wiki/PDF/X)

