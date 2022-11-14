{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","fichier apkg", "format de fichier apkg", "type de fichier apkg", "fichier", "type", "Qu'est-ce qu'un fichier APKG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Format de fichier de pont Anki Flashcard",
  "description" :"Découvrez ce qu'est un fichier APKG et les API qui peuvent les créer et les ouvrir.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Qu'est-ce qu'un fichier APKG ?

Un fichier avec l'extension .apkg est un jeu de cartes mémoire généré pour être utilisé dans l'application logicielle [Anki](https://ankiweb.net/about) qui est un programme d'apprentissage basé sur des cartes mémoire. Il contient du texte [HTML](/fr/web/html/) à charger et à afficher dans l'application Anki et peut en outre avoir des images et des sons pour un apprentissage visuel et sonore. Anki permet aux utilisateurs de créer leurs propres jeux de cartes mémoire Anki ainsi que d'importer les jeux de cartes mémoire d'autres utilisateurs.

## Format de fichier APKG

Les jeux de cartes Anki sont créés à partir de modèles écrits en HTML, un langage célèbre et courant pour la création de pages Web. Le style des cartes de jeu se fait à l'aide de CSS, qui est le langage utilisé pour styliser les pages Web. Le style comprend des modifications à :

* font-family - Le nom de la police à utiliser sur la carte.
* font-size - La taille de la police en pixels.
* text-align - Définit si le texte doit être aligné au centre, à gauche ou à droite.
* couleur - Définit la couleur du texte qui peut être de simples noms de couleur tels que "bleu", "rouge", etc. ou des codes de couleur HTML.
* background-color - Définit la couleur de fond de la carte

Les informations de style sont partagées entre toutes les cartes, affectant toutes les cartes lorsqu'un changement est effectué. L'exemple suivant utilisera un fond jaune sur toutes les cartes sauf la première :

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Le redimensionnement des images dans une carte Anki peut être contrôlé comme suit.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Intégrer Javascript dans les cartes Anki

Il est possible d'intégrer [Javascript](/fr/web/js/) dans une carte Anki en utilisant les modèles de carte. Cependant, en raison du niveau avancé de Javascript, son support n'est pas fourni. De plus, les appareils de rendu peuvent montrer différemment l'implémentation de Javascript dans la carte, ce qui nécessite de tester l'implémentation sur tous les appareils. Certaines fonctionnalités Javascript telles que window.alert, rendent difficile le débogage du code Javascript que vous avez écrit.

## Références ##

* [Documentation Anki](https://docs.ankiweb.net/intro.html)

