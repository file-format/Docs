{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PDF/UA",
  "description":"En savoir plus sur le format de fichier PDF/UA et les API qui peuvent créer et ouvrir des fichiers PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Qu'est-ce qu'un fichier PDF/UA ? #

PDF/UA a été publié en tant que [Norme ISO 14289-1](https://en.wikipedia.org/wiki/ISO_14289) en août 2012 et est de loin la première définition complète d'un ensemble d'exigences pour des documents PDF universellement accessibles. Le terme "universellement accessible" fait référence à la compréhension que les informations contenues dans un document [PDF](/fr/pdf/) doivent être accessibles de manière égale et indépendante à tous en général et aux personnes handicapées en particulier. L'introduction de la norme PDF/UA peut être considérée comme une étape majeure dans la création d'outils et d'applications permettant de créer et de lire du contenu PDF.

## Exigences de format de fichier ##

Le PDF/UA a des exigences définies à sa base qui constituent l'essence de cette norme. Essentiellement, ceux-ci sont basés sur le balisage des PDF, ce qui signifie que tous les documents PDF/UA doivent être correctement balisés. Cela nécessite également que les balises soient sémantiquement appropriées et dans un ordre logique. Cela garantit que le document final créé avec la spécification PDF/UA est plus fiable et accessible. Cela peut amener les auteurs de PDF à se demander s'ils ont besoin de tout savoir sur toutes ces exigences ? Heureusement, ce n'est pas comme ça car les outils de conformité PDF/UA prennent la responsabilité d'ajouter et de préserver l'accessibilité du PDF.

Les exigences de format de fichier pour PDF/UA sont les suivantes.

* Le contenu est catégorisé de deux manières : le contenu significatif et les artefacts tels que les éléments décoratifs de la page. Tout contenu significatif doit être balisé et intégré dans l'arborescence de toutes les balises d'un document. Les artefacts, en revanche, n'ont qu'à être marqués comme tels.
* Le contenu significatif doit être marqué avec des balises et, avec les autres balises du document, créer une arborescence complète.
* Le contenu significatif doit être marqué avec les balises sémantiques appropriées.
* L'arborescence créée par les balises du document doit refléter l'ordre logique de lecture du document.
* Seules les balises standard définies dans PDF 1.7 peuvent être utilisées ; si d'autres balises sont utilisées, une entrée d'attribution de rôle doit enregistrer quelle balise standard chacune représente.
* Les informations ne peuvent pas être transmises uniquement par des moyens visuels (par exemple, contraste, couleur ou position sur la page).
* Aucun contenu scintillant, clignotant ou clignotant n'est autorisé, que ce soit en tant qu'effets contrôlés par JavaScript ou dans le cadre de vidéos intégrées dans le PDF.
* Un titre de document doit être donné et le document doit être configuré de manière à ce que le titre (plutôt que le nom de fichier) apparaisse dans le titre de la fenêtre.
* La langue de tout le contenu doit être notée et les changements de langue doivent être explicitement marqués comme tels.

## Conformité PDF/UA ##

La norme PDF/UA définit les spécifications pour le contenu, les lecteurs et la technologie d'assistance. Ces trois aspects sont liés les uns aux autres en fonction du contenu du document. Les exigences de conformité pour chacun d'entre eux sont indiquées ci-dessous.

## Fichiers conformes ##

Les fichiers conformes à la norme PDF/UA doivent contenir des fonctionnalités valides conformément aux [spécifications PDF 1.7] (http://www.adobe.com/go/pdfreference). Cependant, les fonctionnalités spécifiquement interdites par PDF/UA doivent être exclues.

## Lecteurs conformes ##

Un lecteur conforme doit obéir aux règles énoncées dans les spécifications PDF 1.7. Plus précisément, il doit prendre en charge :

* toutes les balises, attributs et valeurs clés spécifiés pour l'accessibilité. Il devrait également avoir la capacité de traiter et de représenter des signatures numériques, des annotations et du contenu facultatif.
* traiter et représenter les signatures numériques, les annotations et le contenu facultatif
* naviguer dans le document par une variété de moyens

## Technologie d'assistance conforme ##

Une technologie d'assistance conforme est destinée à prendre en charge les fonctionnalités PDF/UA. Ceux-ci incluent, par exemple, les caractéristiques du contenu et du lecteur, et doivent permettre la navigation par étiquettes de page, structure du document ou plan. Il devrait également permettre à l'utilisateur de remplacer le zoom de navigation par défaut.

## Références ##

* [PDF/UA - Par Wikipédia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA en bref](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

