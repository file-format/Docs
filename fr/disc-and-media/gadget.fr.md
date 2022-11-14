{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"En savoir plus sur le format de fichier GADGET et les API qui peuvent créer et ouvrir des fichiers GADGET.",
  "title" :"GADGET - Fichier de CD virtuel",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## Qu'est-ce qu'un fichier GADGET ?

Un fichier GADGET consiste en un petit programme logiciel qui s'exécute dans la barre latérale de Windows Vista ou Windows 7. Il compresse plusieurs fichiers Web et les fichiers peuvent comprendre les fichiers [.html](/fr/web/html), [.css](/fr/web/css) ou [.js](/fr/web/js), ainsi que d'autres fichiers Web. Les fichiers GADGET sont utilisés pour les petits composants tels que les outils de recherche, les flux d'actualités, les utilitaires système et les petits jeux. Bien que les GADGET soient hébergés par la barre latérale, ils ne sont pas spécifiques à la zone de la barre latérale ; ceux-ci peuvent être détachés et déplacés sur le bureau comme vous le souhaitez.

## Format de fichier GADGET

Le fichier GADGET est une archive renommée [ZIP](/fr/compression/zip) contenant une collection de fichiers HTML, XML, JScript et CSS (Cascading Style Sheets). L'installation consiste à télécharger le fichier .gadget et à activer le processus de téléchargement pour installer le composant ou à enregistrer le fichier .gadget sur le système local et à double-cliquer pour démarrer le processus d'installation.

Fondamentalement, un GADGET contient deux fichiers :

1. **Gadget.xml** : Le manifeste, un fichier XML contenant des informations générales de présentation et de configuration pour le gadget.
2. **name.html** : Un fichier HTML, dans lequel le nom est spécifié dans le<name> balise du manifeste de gadget associé, qui fournit le wrapper pour l'interface utilisateur du gadget et comprend la fonctionnalité principale du gadget.

Plusieurs instances d'un fichier GADGET peuvent être exécutées simultanément. Par exemple, si quelqu'un veut connaître l'heure dans différents fuseaux horaires, il peut exécuter plusieurs instances du gadget horloge en réglant chaque horloge sur un fuseau horaire particulier.

### Arrêt de GADGET

Étant donné que la plate-forme Windows Sidebar de Windows 7 présente de graves vulnérabilités, les gadgets ne sont plus disponibles sur le site officiel de Microsoft. Plus tard, Microsoft a retiré cette fonctionnalité dans les nouvelles versions de Windows. GADGET pourrait être exploité pour accéder aux fichiers d'un ordinateur, endommager un ordinateur, révéler un contenu répréhensible ou modifier son comportement à tout moment.

## Références

* [Barre latérale Windows - par Microsoft](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Développement d'un gadget pour la barre latérale Windows Partie 1](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

