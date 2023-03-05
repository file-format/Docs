{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier DISCO - Format de fichier de document de découverte DISCO",
  "description":"Découvrez ce qu'est un fichier DISCO et les API qui peuvent créer et ouvrir des fichiers DISCO.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## Qu'est-ce qu'un fichier DISCO ?

Un fichier DISCO est un format de fichier Microsoft Discovery utilisé pour publier et découvrir des services Web. Il est stocké au format de fichier XML et permet aux outils de découverte de services Web de localiser ou de découvrir un ou plusieurs documents connexes pour décrire les services [XML](/fr/web/xml/) disponibles. Le fichier DISCO stocke des informations telles que des documents de découverte, des schémas [XSD](https://docs.fileformat.com/programming/xsd/) et des descriptions de service. Les services Web XML utilisent ces informations pour accéder aux services Web XML disponibles à une URL donnée.

## Format de fichier DISCO - Plus d'informations

Les fichiers DISCO sont enregistrés au format de fichier XML. Microsoft Discovery Tool (DISCO.exe), fourni avec le logiciel de développement Microsoft ASP.NET tel que Microsoft Studio, utilise les fichiers DISCO pour découvrir les détails des services Web XML répertoriés dans un DiscoveryDocument à une URL spécifique. Microsoft a fourni la prise en charge de la lecture des fichiers de découverte dans le framework .NET.

## Références

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894?tab=Overview)
* [Découverte des services Web](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Exemple C# de classe DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

