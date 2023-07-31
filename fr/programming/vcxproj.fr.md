{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "fichier", "extension", "format de fichier", "Projet Visual C++", "Guide de programmation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"En savoir plus sur le format de fichier VCXPROJ et les API qui peuvent créer et ouvrir des fichiers VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier VCXPROJ ?

Un fichier avec l'extension .vcxproj est un fichier de projet Microsoft Visual C++ qui stocke les informations de projet [C++](/fr/programming/cpp/). Il contient des informations utilisées par le système de projet MSBuild pour compiler et générer la sortie finale. VCXPROJ des projets Visual C++ est le même que celui de [CSPROJ](/fr/programming/csproj/) pour les projets .NET. Les fichiers VCXPROJ ne contiennent aucun code mais font référence à toutes les classes, cibles et propriétés définies pour le projet afin de construire le projet. Ceux-ci peuvent être ouverts dans des éditeurs de texte brut ou de préférence dans Microsoft Visual Studio IDE.


## Format de fichier VCXPROJ - Plus d'informations

Les fichiers VCXPROJ sont des fichiers texte créés au format de fichier [XML](/fr/web/xml/). Ceux-ci peuvent être ouverts dans n'importe quel éditeur de texte, mais il est fortement recommandé d'utiliser Microsoft Visual Studio IDE pour ouvrir et modifier ces fichiers. Ceux-ci n'ont pas été conçus pour l'édition manuelle. Des erreurs peuvent provoquer le blocage de l'IDE ou son comportement inattendu.

Le contenu d'un exemple de fichier VCXPROJ est le suivant.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Éléments de fichier VCXPROJ

Un fichier VCXPROJ typique contient un certain nombre d'éléments comme on peut le voir dans l'exemple XML ci-dessus. La [structure VCXPROJ](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) de Microsoft explique chaque élément de fichier en détail et peut être consultée du point de vue du développeur.

#### Élément de projet

Il s'agit du nœud racine du fichier VCXPROJ. MSBuild utilise cet élément pour lire la version de build et la cible par défaut pour la compilation.

#### Élément de groupe d'éléments ProjectConfigurations

Il contient les informations de configuration du projet qui peuvent inclure la méthode de génération (Debug ou Release), la compilation 32 ou 64 bits, les options d'optimisation, etc. Les informations de ce groupe sont utilisées par l'IDE pour charger le projet.

#### Éléments de configuration du projet

Les éléments ProjectConfiguration d'un fichier VCXPROJ contiennent des informations sur la version et la plate-forme pour lesquelles le projet est chargé. Son nom doit suivre le format `$(Configuration)|$(Platform)`.

#### Élément Globals PropertyGroup

Cette section contient des paramètres qui fournissent des informations au niveau du projet, telles que :

* Guide de projet
* RootNamespace
* ApplicationType ou ApplicationTypeRevision


## Références

* [Structure VCXPROJ - MSDN](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Fichiers de projet C++](https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

