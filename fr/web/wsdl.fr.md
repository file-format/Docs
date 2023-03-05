{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier WSDL - Fichier de langage de description de services Web",
  "description":"Découvrez ce qu'est un fichier WSDL et les API qui peuvent créer et ouvrir des fichiers WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Qu'est-ce qu'un fichier WSDL ?

Un fichier WSDL est un fichier Web Services Description Language écrit en langage XML pour décrire les services Web. Il contient des informations sur les terminaux ou les interfaces de connectivité avec le monde extérieur dans un format universellement accepté. [Spécifications du format de fichier WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (maintenu par W3C.org) définissent les conditions de publication des flux de données pour l'échange de données afin d'avoir accès aux applications à distance sur les ports et les terminaux.

## Format de fichier WSDL - Plus d'informations

Les fichiers WSDL sont enregistrés sous forme de fichiers XML lisibles par l'homme et peuvent être ouverts dans n'importe quel éditeur de texte pour afficher le contenu.

## Description du service WSDL

Les spécifications du format de fichier WSDL 2.0 décrivent le service WSDL comme comprenant deux étapes :

- Stade abstrait
- Scène béton

La réutilisabilité de la description et des conceptions indépendantes est régie par un service Web. Ceci est réalisé en utilisant plusieurs types d'éléments différents, notamment des types (définitions de types de données), des messages (les données communiquées), des opérations (actions) et des protocoles utilisés par le service. Ceux-ci sont tous gérés au niveau abstrait. La liaison des détails de transport et de format de câble est spécifiée par la liaison, qui regroupe les points de terminaison pour implémenter une interface commune.

### Quelles technologies peuvent être utilisées pour s'interfacer avec les services WSDL ?

Plusieurs technologies différentes peuvent être utilisées pour l'interfaçage avec les services WSDL, notamment les applications ASP.NET, C/C++ et Java.

## Exemple WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

Dans cet exemple, le portType "glossaryTerms" définit une opération unidirectionnelle appelée "setTerm".

## Références

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Spécifications du format de fichier WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

