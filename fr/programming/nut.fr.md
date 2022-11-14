{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "fichier", "extension", "format de fichier", "langage de programmation NUT", "Guide de programmation", "exemple NUT", "format de fichier NUT", "langage écureuil", "fichier d'extension .nut ", "Fichiers NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Fichier de langue d'écureuil",
  "description":"En savoir plus sur le format de fichier NUT et les API qui peuvent créer et ouvrir des fichiers NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Qu'est-ce qu'un fichier NUT ?

Le NUT fait référence au fichier NUT Open Container Format. Ce format de fichier NUT appartient au langage de programmation connu sous le nom d'écureuil. C'est un langage de programmation orienté objet, de haut niveau et impératif qui est principalement utilisé dans les systèmes embarqués et les jeux vidéo.

Le langage écureuil est considéré comme un langage de script léger qui peut être facilement ajusté en fonction de la taille et de la bande passante. Cela implique l'avantage du comptage automatique des références et la gestion des ordures en mémoire.

La syntaxe du langage écureuil attire les développeurs car elle ressemble à C et implique la fonctionnalité du langage de script. Mais encore, il a bien moins d'avantages par rapport à d'autres langages de programmation plus populaires à cette fin.



## Bref historique ##

Il a été conçu par Alberto Demichelis en 2003. Cependant, une version stable de ce langage est sortie en 2016. Il a été conçu sous la licence zlib/libpng. En 2010, la licence a été modifiée et transférée au MIT. Ce langage est considéré comme une version inspirée de [LUA](/fr/programming/lua/) (langage de programmation). Il y a une liste de suggestions pour l'ancienne langue sur le site Web conçu par Alberto pour la rendre plus avantageuse.


## Spécifications techniques ##

La caractéristique et les spécifications du langage de l'écureuil sont multiples. Il fournit la facilité de typage dynamique, la propriété de délégation, plusieurs utilisations de classes et d'interfaces. La syntaxe de ce langage a une similitude avec la syntaxe du langage C. Des applications telles que Enduro/X (un serveur d'applications en cluster) utilisent ce langage. Comme Squirrel est également utilisé pour les jeux vidéo, certains d'entre eux sont OpenTTD, GTA IV, etc.

La version stable du langage est 3.0.7. Une boîte à outils connue sous le nom de MirthKit utilise le langage de programmation Squirrel pour fournir une source ouverte et multiplateforme pour les jeux en deux dimensions. La nature de ce langage est dynamique et la plupart des fonctionnalités sont similaires à [Python](/fr/programming/py/), LUA, etc. Il implique également la mise en œuvre d'une VM basée sur des registres. Les performances de Squirrel sont plus lentes que celles de LUA.

Il existe également un autre type de fichier d'extension ".nut", c'est pourquoi vous devriez regarder la taille du fichier pour savoir quel fichier NUT vous avez. Les fichiers NUT de script Squirrel sont généralement inférieurs à 1 Mo, tandis que les fichiers NUT vidéo ont généralement une taille supérieure à 1 Mo.


## Exemple de format de fichier NUT ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Référence ##

* [NUT - par Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



