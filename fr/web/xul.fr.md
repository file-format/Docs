{
  "date" : "2021-05-24",
  "keywords" :["xul", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "Langage de l'interface utilisateur XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - Fichier de langage d'interface utilisateur XML",
  "description":"En savoir plus sur le format de fichier XUL et les API qui peuvent créer et ouvrir des fichiers XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Qu'est-ce qu'un fichier XUL ?

Un fichier avec une extension .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) signifie XML User Interface Language) est un fichier de langage de balisage basé sur [XML](/fr/web/xml/) pour création d'interfaces utilisateur. Il a été développé par Mozilla pour que les développeurs créent des éléments d'interface utilisateur graphique similaires à d'autres langages de balisage utilisés pour créer des pages Web. XUL a été largement utilisé par Mozilla dans son navigateur Firefox où il a utilisé la base de code Mozilla. Le rendu XUL est réalisé à l'aide de la
[Moteur Gecko](https://en.wikipedia.org/wiki/Gecko_(software)). Les fourches Firefox telles que Pale Moon, Basilisk et Waterfox conservent la prise en charge des modules complémentaires XUL. Les fichiers XUL sont identifiés par le type MIME : application/vnd.mozilla.xul+xml.

## Format de fichier XUL

Les fichiers XUL sont écrits en texte brut basé sur le format de fichier XML et sont rendus à l'aide du moteur Gecko. Les trois parties principales d'une structure XUL sont :

* `Content` - Cela inclut les déclarations de la fenêtre et les éléments de l'interface utilisateur qu'elles contiennent.
* `Skin` - Il comprend toutes les feuilles de style, images et autres fichiers liés au thème. L'apparence d'une fenêtre est décrite dans les feuilles de style.
* `Locale` - Le texte affiché dans une fenêtre est stocké séparément et plusieurs ensembles de fichiers de langue peuvent être utilisés par les utilisateurs.

### Exemple XUL

L'exemple suivant crée trois boutons empilés les uns sur les autres dans le sens vertical.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Références

* [XUL - Par Wikipédia](https://en.wikipedia.org/wiki/XUL)
* [Documentation archivée XUL - Par Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

