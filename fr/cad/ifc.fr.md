{
  "date" : "2020-03-16",
  "keywords" :[ "Fichier IFC", "Format", "CAO" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier IFC et les API qui peuvent créer et ouvrir des fichiers IFC.",
  "title" :"Format de fichier IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier IFC ?

Les fichiers avec l'extension IFC font référence au format de fichier IFC (Industry Foundation Classes) qui établit des normes internationales pour importer et exporter des objets de construction et leurs propriétés. Ce format de fichier permet l'interopérabilité entre différentes applications logicielles. Les spécifications de ce format de fichier sont développées et maintenues par buildingSMART International en tant que norme de données. L'objectif ultime du format de fichier IFC est d'améliorer la communication, la productivité, le délai de livraison et la qualité tout au long du cycle de vie d'un bâtiment.

En raison des normes établies pour les objets communs dans l'industrie du bâtiment, il réduit la perte d'informations lors de la transmission d'une application à une autre. IFC peut contenir des données pour la géométrie, le calcul, les quantités, la gestion des installations, la tarification, etc. pour de nombreuses professions différentes (architecte, électricité, CVC, structure, terrain, etc.).

## Bref historique ##

L'initiative IFC a été prise en 1994 par Autodesk pour soutenir le développement d'applications intégrées et comprenait des sociétés comme Honeywell, Butler Manufacturing et AT&T. En 1995, l'adhésion a été ouverte à tous et le nom a été changé en Alliance internationale pour l'interopérabilité. L'intention de l'organisation à but non lucratif était de publier l'Industry Foundation Class (IFC) en tant que modèle de produit AEC. En 2005, le nom a de nouveau été changé et buildSMART le maintient désormais.

## Format de fichier IFC ##

Le format de fichier IFC a subi plusieurs modifications par le passé pour atteindre les spécifications de format de fichier v4. Plusieurs changements mineurs sont survenus de temps à autre et ont été intégrés aux spécifications sous forme d'addendums. Vous trouverez ci-dessous une liste des différentes versions des spécifications de fichiers qui ont été rendues publiques par le passé.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (mars 2013) ifcXML2x3 (juin 2007)
* IFC2x3 (février 2006) ifcXML2 pour IFC2x2 add1 (RC2)
* IFC2x2 Addendum 1 (juillet 2004)ifcXML2 pour IFC2x2 (RC1)
* IFC 2x2IFC 2x Addendum 1ifcXML1 pour IFC2x et
* IFC2x Addendum 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Les dernières versions des spécifications de format de fichier IFC sont toujours disponibles sur le site Web de buildingSMART et les développeurs doivent les consulter pour tout type d'applications qu'ils envisagent de développer. Au moment de la rédaction de cet article, les spécifications de la version 4 sont les dernières disponibles en ligne.

### Formats de fichiers de données IFC ###

Le format de fichier IFF prend en charge l'échange de données entre les applications en utilisant différents formats comme indiqué ci-dessous :

**IFC :** Il s'agit du format d'échange IFC par défaut et utilise la structure de fichier physique STEP conformément à la norme ISO 10303-21. Ce format de fichier a l'extension de fichier .ifc et est le format IFC le plus utilisé.

**IFC-XML :** Il s'agit d'une version au format de fichier XML d'IFC qui peut être générée directement par l'application émettrice selon la structure ISO 10303-28, également appelée STEP-XML. Le format de fichier IFC-XML est considéré comme adapté à l'interopérabilité entre les outils XML. Par rapport au format de fichier IFC, le format IFC-XML est 300 à 400 % plus grand.

**IFC-ZIP :** Il s'agit d'une version compressée [ZIP](/fr/compression/zip/) d'IFC ou d'IFC-XML où l'un de ces fichiers se trouve dans le répertoire principal de l'archive zip. Ce format compresse un fichier .ifc de 60 à 80 % et un fichier XML .ifc de 90 à 95 %.

### Architecture IFC ###

La spécification IFC comprend des termes, des concepts et des éléments de spécification de données qui proviennent de l'utilisation dans les disciplines, les métiers et les professions du secteur de la construction et de la gestion des installations. Les termes et concepts utilisent des mots anglais clairs, les éléments de données dans la spécification de données suivent une convention de dénomination.

les noms des éléments de données pour les types, les entités, les règles et les fonctions commencent par le préfixe "Ifc" et continuent avec les mots anglais dans la convention de dénomination CamelCase (pas de trait de soulignement, première lettre du mot en majuscule) ; les noms d'attributs au sein d'une entité suivent la convention de dénomination CamelCase sans préfixe ; les définitions de jeux de propriétés qui font partie de cette norme commencent par le préfixe "Pset_" et continuent avec les mots anglais dans la convention de dénomination CamelCase ; les définitions d'ensembles de quantités qui font partie de cette norme commencent par le préfixe "Qto_" et continuent avec les mots anglais dans la convention de dénomination CamelCase.

L'architecture de schéma de données d'IFC définit quatre couches conceptuelles, chaque schéma individuel est affecté à exactement une couche conceptuelle.

**Couche de ressources** : la couche la plus basse comprend tous les schémas individuels contenant des définitions de ressources. Ces définitions n'incluent pas d'identifiant unique au monde et ne doivent pas être utilisées indépendamment d'une définition déclarée à une couche supérieure ;

**Couche principale** : la couche suivante comprend le schéma du noyau et les schémas d'extension principaux, contenant les définitions d'entité les plus générales, toutes les entités définies au niveau de la couche principale ou au-dessus portent un identifiant unique au monde et éventuellement des informations sur le propriétaire et l'historique ;

**Couche d'interopérabilité** : la couche suivante comprend des schémas contenant des définitions d'entité spécifiques à une spécialisation générale de produits, de processus ou de ressources utilisées dans plusieurs disciplines. Ces définitions sont généralement utilisées pour l'échange inter-domaines et le partage d'informations de construction ;

**Couche de domaine** : la couche la plus élevée comprend des schémas contenant des définitions d'entités qui sont des spécialisations de produits, de processus ou de ressources spécifiques à une certaine discipline. Ces définitions sont généralement utilisées pour l'échange intra-domaine et le partage d'informations.

## Références ##

* [Classes de base de l'industrie - Par Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

