{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "format de fichier", "type de fichier", "qu'est-ce qu'un fichier .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - Fichier de configuration ASP",
  "description" :"Découvrez ce qu'est un fichier ASA et les API qui peuvent créer et ouvrir des fichiers ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Qu'est-ce qu'un fichier ASA ?

Un fichier ASA est un fichier de configuration créé pour les projets [ASP](/fr/web/asp/)/ASP.NET. Il contient des déclarations de variables, des contenus et des fonctions destinés à être accessibles au niveau global dans l'application. Toutes les pages du projet peuvent accéder à ces variables et fonctions, évitant ainsi la nécessité de les réécrire. Un tel exemple est la page Global.asa qui est stockée dans le répertoire racine pour être accessible par d'autres pages de site Web ASP. Les fichiers Global.asa sont facultatifs, mais s'ils sont utilisés, chaque application ne peut avoir qu'un seul fichier Global.asa.

## Format de fichier ASA - Plus d'informations

Les fichiers ASA sont des fichiers texte brut contenant les informations suivantes.

* Événements d'application
* Événements de session
* \<object> déclarations
* Déclarations TypeLibrary
* la directive #include

## Exemple de fichier ASA

Un fichier Global.asa pourrait ressembler à ceci.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Références

* [Fichier ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

