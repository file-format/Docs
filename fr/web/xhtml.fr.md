{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "html extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Format de fichier de langage de balisage hypertexte extensible",
  "description":"Découvrez ce qu'est le format de fichier XHTML et les API qui peuvent créer et ouvrir des fichiers XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier XHTML ?

Le XHTML est un format de fichier basé sur du texte avec un balisage dans le XML, utilisant une reformulation de HTML 4.0. Ces fichiers sont bien adaptés pour être ouverts ou visualisés dans un navigateur Web. XHTML a été conçu pour être plus structuré, moins scripté, générique ; en utilisant toutes les facilités existantes de XML et plus indépendant de l'appareil. XHTML fournit un ensemble généralement intéressant d'éléments et d'attributs, avec des options d'extension en combinaison avec des feuilles de style. Les attributs sont utilisés à partir de la collection d'attributs de métadonnées. XHTML offre flexibilité et accessibilité en subordonnant tous les éléments de présentation **[HTML](/fr/web/html/)** aux feuilles de style. Les feuilles de style sont plus polyvalentes que ces éléments de présentation. Les spécifications pour HTML 4.01, HTML5 et XHTML sont développées de manière dynamique par le World Wide Web Consortium (W3C).

## Bref historique du format de fichier XHTML

L'histoire de XHTML commence avec un projet de document publié en décembre 1998 par le World Wide Web Consortium. Ce document fait référence à la "Reformulation du HTML en XML", une spécification appelée XHTML 1.0. Cette nouvelle spécification reformule le HTML en XML en utilisant les éléments ou attributs existants. En mai 1999, W3 Consortium a déclaré que HTML 4.0 avait été reformé en tant qu'application XML. c'est-à-dire XHTML. Le 26 janvier 2000, la première spécification définissant XHTML 1.0 a été publiée par le W3C. De plus, le 31 mai 2001, le W3C a annoncé XHTML comme langage indépendant et a commencé à travailler sur le développement de HTML 5.0. Cependant, en 2005, un groupe de travail (WHATWG) a été formé qui visait à améliorer le HTML ordinaire indépendamment du XHTML. Le WHATWG a finalement commencé à travailler sur HTML5 en parallèle avec XHTML 2.

## Format de fichier XHTML

XHTML est un format, qui est une collection de différents types de documents et de modules qui imitent, catégorisent et étendent HTML 4. Les fichiers en XHTML sont basés sur XML et destinés à fonctionner avec les agents utilisateurs basés sur XML. Les fichiers XHTML sont conformes à XML. Les outils XML standard sont utilisés pour visualiser, éditer et valider les fichiers XHTML. Les applications dépendantes du modèle d'objet de document HTML ou du modèle d'objet de document XML [DOM] peuvent fonctionner via des documents XHTML. En choisissant XHTML aujourd'hui, les développeurs de contenu peuvent profiter de tous les avantages associés à XML sans se soucier de la compatibilité ascendante ou descendante de leur contenu.

Un ensemble d'éléments connexes construit un module en XHTML. Un formulaire ou un module de tableau peut contenir divers éléments de formulaire ou de tableau pouvant être affichés sur une page Web. La modularisation visait à isoler les éléments HTML en ensembles de nombreux éléments liés. Ainsi, les développeurs de contenu peuvent profiter de la sélection de modules pour différents types d'appareils. De plus, les modules permettent aux agents utilisateurs de sélectionner des éléments sans perdre la cohérence avec le standard XHTML. Les exigences d'analyse de XHTML sont les mêmes que celles de XML, tandis que HTML pratique les siennes.

### Conformité des documents

XHTML2 offre des spécifications conformes aux documents XHTML 1.0, qui utilisent les éléments d'espaces de noms et les attributs du XML et du XHTML 1.0. La conformité des documents est de deux types.

Un document strictement conforme est basé sur XML et n'a besoin que des services obligatoires définis dans cette spécification. Les critères suivants doivent être remplis pour les fichiers XHTML :

* Un fichier doit respecter les contraintes définies dans les DTD et en Annexe B.
* L'élément de base du fichier doit être html.
* L'élément de base du fichier doit contenir une déclaration pour l'espace de noms XHTML et doit être défini comme :

```
http://www.w3.org/1999/xhtml.
```

* L'élément de base peut s'écrire :

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Avant l'élément de base, un DOCTYPE doit être déclaré, dont l'identifiant public doit référencer l'une des trois définitions de type de document (DTD). L'identifiant du système peut être modifié pour se conformer aux conventions actuelles du système.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

Dans les documents XML, il n'est pas nécessaire de spécifier des déclarations XML dans tous les documents ; cependant, les développeurs de contenu sont incités à utiliser des déclarations XML dans tous leurs documents XHTML. Ces déclarations sont obligatoires soit lorsque l'encodage des caractères du document est différent de l'UTF-8/16, soit qu'aucun encodage n'a été spécifié par un protocole régissant. L'exemple suivant d'un document XHTML définit les déclarations XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Un agent utilisateur conforme doit respecter les règles suivantes :

* L'analyse et l'évaluation du document XHTML sont effectuées par un agent utilisateur qui assure sa cohérence avec la recommandation XML 1.0.
* En cas de validation de l'agent utilisateur, il doit vérifier la validité des documents pour leurs DTD référencées selon XML. Lorsque le fichier XHTML est traité par l'agent utilisateur en tant que XML générique, les fonctionnalités de type ID seront reconnues comme des identifiants de fragment.

Si un agent utilisateur se heurte à un élément non reconnu, voici les critères obligatoires qu'il doit remplir

* traiter le contenu de cet élément inconnu
* ignorer l'attribut et sa valeur
* Utilisez la valeur de l'attribut fourni par défaut.

Lorsque l'agent utilisateur rencontre une déclaration de référence d'entité qui n'a pas été traitée plus tôt, elle doit être traitée comme les caractères (en commençant par le signe "&" et en terminant par le point-virgule). Pendant le traitement du contenu, les caractères ou les références d'entités de caractère qui sont prévisibles par l'agent utilisateur mais non restituables peuvent utiliser n'importe quel rendu alternatif qui produit la même signification. Dans ce cas, le document doit être affiché de manière à rendre évident à l'utilisateur le fait que le processus de rendu n'a pas été normal. Pour traiter les espaces blancs, l'agent utilisateur doit rechercher la définition à partir des caractères CSS [CSS2].

## Rétrocompatibilité XHTML

La rétrocompatibilité des documents XHTML 1. est bien familiarisée avec les agents utilisateurs HTML 4, si les règles appropriées sont suivies. XHTML 1.1 est entièrement compatible à l'exception des annotations ruby, même si elles sont généralement ignorées par les navigateurs HTML 4. XHTML 2.0 est comparativement moins compatible, néanmoins le problème a été résolu dans une certaine mesure grâce à l'utilisation de scripts.

## Références

* [Une histoire de XHTML : des années 1990 à aujourd'hui](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

