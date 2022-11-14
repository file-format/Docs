{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier APPCACHE - Format de fichier manifeste du cache HTML5",
  "description" :"Découvrez ce qu'est un fichier APPCACHE et les API qui peuvent créer et ouvrir des fichiers APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Qu'est-ce qu'un fichier APPCACHE ?

Un fichier APPCACHE est un fichier texte qui contient la liste des ressources à mettre en cache par les navigateurs pour un accès hors ligne aux applications Web. Ceci est utile lorsqu'il n'y a pas de connexion Internet. Dans une telle situation, le navigateur utilise les ressources de cache hors ligne pour fournir un accès au contenu Web. Le fichier APPCACHE contient des ressources Web telles que des images (par exemple **[PNG](/fr/image/png/)**, **[WEBP](/fr/image/webp/)**, etc.), des feuilles de style **([ CSS])(/fr/web/css/)** et les fichiers de script (tels que les fichiers Javascript **[JS](/fr/web/js/)**).

Les applications qui peuvent **ouvrir les fichiers APPCACHE** incluent les navigateurs Web tels que Google Chrome, Safari et Firefox.

## Format de fichier APPCACHE - Plus d'informations

Les fichiers APPCACHE sont de simples fichiers texte, fournissant un accès hors ligne aux pages Web pour une exécution sans connexion Internet. La présence d'APPCACHE désigne une page comme disponible hors ligne.

### Comment référencer un fichier APPCACHE ?

Dans votre page HTML, un fichier APPCACHE est référencé comme suit.

```
<html manifest="example.appcache">
  ...
</html>
```

## Structure d'un fichier manifeste APPCACHE

Un fichier manifeste APPCACHE simple se présente comme suit.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Ceci est un exemple le plus simple et il peut également y avoir des structures plus complexes.

## Avantages du manifeste APPCACHE

L'utilisation de l'interface de cache donne aux applications Web les avantages suivants.

1. Navigation hors ligne - L'interface de cache permet aux utilisateurs finaux de parcourir l'intégralité de votre site lorsqu'ils sont hors ligne.
1. Vitesse - le cache permet un accès rapide au contenu hors ligne directement à partir du disque
1. Accessibilité à tout moment - En cas de panne de votre site, les utilisateurs auront toujours accès au contenu Web et pourront profiter de l'expérience hors ligne

## Références

* [Guide du débutant sur le manifeste AppCache](https://web.dev/appcache-beginner/)

