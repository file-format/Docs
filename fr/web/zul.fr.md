{
  "date" : "2021-05-24",
  "keywords" :["zul", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "ouvrir"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - Fichier d'interface utilisateur ZK",
  "description":"En savoir plus sur le format de fichier ZUL et les API qui peuvent créer et ouvrir des fichiers ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Qu'est-ce qu'un fichier ZUL ?

Un fichier avec l'extension .zul est un fichier Web créé avec le langage ZUML (User Interface Markup Language) et contient des définitions pour les éléments de l'interface utilisateur. Les classes Ajax et Java prennent en charge l'utilisation de ZUML basé sur [XML](/fr/web/xml/) pour développer des fichiers côté serveur. Le format de fichier ZUL a été développé par ZK, un framework d'interface utilisateur qui vous permet de créer des applications Web et mobiles sans connaître JavaScript ou AJAX.

## Format de fichier ZUL

Les fichiers ZUL sont basés sur XML et se composent de différents éléments pour construire une interface utilisateur. Le chargeur ZK utilise chaque élément XML pour créer un composant. Le traitement global des éléments de la page tels que le titre de la page, la description, etc. est décrit par chaque instruction de traitement XML de ZUML.

### Exemple ZUL

Dans l'exemple suivant de code ZUML, la première ligne spécifie le titre de la page, la deuxième ligne crée un composant racine avec un titre et une bordure, et la troisième ligne crée un bouton avec une étiquette et un écouteur d'événement.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Le schéma ZUL peut être téléchargé depuis http://www.zkoss.org/2005/zul/zul.xsd.
## Références

* [ZUL - Par ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Schéma ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

