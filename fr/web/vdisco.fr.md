{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier VDISCO - Format de fichier de document de découverte dynamique DISCO",
  "description":"En savoir plus sur ce qu'est un fichier VDISCO ?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Qu'est-ce qu'un fichier VDISCO ?

Un fichier VDISCO est un fichier de découverte utilisé par Microsoft Visual Studio dans ses services Web. Il fournit des informations sur les services Web disponibles, telles que leurs URL, espaces de noms et méthodes. Le fichier VDISCO est similaire au format de fichier [DISCO](/fr/web/disco/) mais est généré au moment de l'exécution. Il est stocké dans l'application de service Web et est utilisé par Visual Studio pour découvrir et utiliser dynamiquement les services Web dans un projet. Les fichiers VDISCO sont utilisés en combinaison avec le fichier [.asmx](/fr/web/asmx/) qui contient le code réel du service Web.

Vous pouvez ouvrir le fichier VDISCO dans n'importe quel éditeur de texte tel que Microsoft Notepad, Github Atom et Apple TextEdit. Il peut également être ouvert avec Microsoft Visual Studio 2012 et versions ultérieures pour travailler avec.

## Format de fichier VDISCO

Un fichier VDISCO est enregistré et hébergé au format de fichier [XML](/fr/web/xml/), qui est un format universel pour la composition et la publication de données. Il contient l'URL du service, les espaces de noms et les méthodes dans des balises XML standard où chaque balise contient la valeur respective de ses informations.

## Les références

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Découverte des services Web](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Exemple C# de classe DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

