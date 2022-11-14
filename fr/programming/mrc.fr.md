{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "fichier", "extension", "format de fichier", "implémentation mrc", "Guide de programmation", "exemple mrc", "mIRC", "langage de script mIRC", "fichiers INI", " langage de script mSL", "langage mIRC", "scripts mIRC", "langage de script" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - Fichier de langage de script mIRC",
  "description":"En savoir plus sur le format de fichier MRC et les API qui peuvent créer et ouvrir des fichiers MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Qu'est-ce qu'un fichier MRC ?

mIRC est un langage de script intégré en tant que client IRC (Internet Relay Chat) dans le système d'exploitation Windows. Il fournit une fonction de protection contre le spam pour une utilisation personnelle et de canal. Pour offrir une meilleure expérience de compatibilité utilisateur, ce langage de script mIRC permet la création de fenêtres de dialogue. Les fichiers contenant des scripts, principalement au format texte brut, sont stockés avec l'extension MRC ou en tant que fichiers [INI](/fr/system/ini/). Les fonctions de ce langage sont appelées commandes et identificateurs (lorsqu'elles renvoient une valeur).

Le langage mIRC permet le chargement de plusieurs fichiers de script à la fois. D'autre part, un fichier peut empêcher l'autre d'être utilisé lorsqu'il est chargé simultanément. Les commandes sont enregistrées et elles peuvent exister automatiquement dans IRC. Les commandes et alias utilisés dans ce langage ne comportent la préséance d'aucun des caractères.

mIRC est largement utilisé pour permettre aux robots de gérer automatiquement un canal, mais il peut également être modifié par le langage de script mSL. Il peut introduire de nombreuses nouvelles fonctionnalités telles que des macros, la capacité de lecture de musique, de petites macros et fonctions, des jeux de base ou l'exploitation de petites applications.


## Bref historique ##

Ce langage de script a été développé pour la première fois en 1995 par Khaled Adam Bey. La conception du langage de script a également été créée par Khalid. La cible de ce langage était la programmation événementielle. Initialement, l'extension de fichier utilisée pour les fichiers de ce langage de programmation était .mrc et .ini. De plus, il a été développé sous la licence d'un logiciel propriétaire.

## Spécification technique ##

Certaines fonctions sont personnalisées via ce langage mIRC et sont connues sous le nom d'alias. Lorsque ces alias renvoient des valeurs, ils sont appelés identificateurs personnalisés. Toutes les variables contenues dans ce langage mIRC sont typées dynamiquement. Les sigils sont utilisés par les scripts mIRC. Une autre caractéristique de ce langage de script est les pop-ups. Les utilisateurs peuvent appeler des pop-ups en les sélectionnant simplement. Des télécommandes sont spécifiées pour certains événements. Les télécommandes sont appelées lorsque l'événement relatif se produit.

Des jetons délimités par des espaces sont utilisés pour casser chaque ligne de code de ce langage. Il existe d'autres extensions populaires utilisées pour les fichiers mIRC telles que MDX (mIRC Dialog Extension) et DCX (Dialog Control Extension). Ces deux extensions sont des extensions de dialogue et sont comparativement plus populaires. Les constructions de langage sont désignées par la nomenclature de ce langage de script. Le langage mIRC implique différents aspects d'un langage de script tels que les variables locales et globales, les variables binaires, les tables de hachage et la gestion des fichiers.


## Exemple de format de fichier MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/fr/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Référence ##

* [MIRC - par Wikipédia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



