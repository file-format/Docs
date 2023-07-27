{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Format de fichier de script Haskell",
  "description":"Découvrez ce qu'est un format de fichier HS et les API qui peuvent créer et ouvrir des fichiers HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Format de fichier Java HelpSet

## Qu'est-ce qu'un fichier Java HS ?

Un fichier avec l'extension .hs dans le langage de programmation Java est un fichier de documentation d'aide utilisé par le système JavaHelp lorsqu'il est activé par une application. Il définit l'ensemble d'aide pour l'application particulière installée et comprend plusieurs sous-ensembles dans le cadre de l'aide système de l'application. Le programme Java doit pouvoir trouver le fichier d'aide dont le nom se termine par l'extension .hs.

## Informations sur l'ensemble d'aide Java

Un fichier .hs peut contenir les informations suivantes.

|Informations|Description|
---|---|
|Fichier de carte|Le fichier de carte est utilisé pour associer les ID de rubrique au localisateur de ressources uniforme ou au nom de chemin des fichiers de rubrique du langage de balisage hypertexte.|
|Afficher les informations|Informations décrivant les navigateurs utilisés dans l'ensemble d'aide. les navigateurs de qualité sont : table des matières, index et recherche plein texte. d'autres navigateurs incluent le gloss ainsi que les navigateurs favoris. les données concernant les navigateurs personnalisés sont jointes ici plus loin.|
<html>|Titre de l'aide|Le \<title> est décrit dans le fichier helpset (.hs). Ce titre apparaît au plus haut de la plupart des fenêtres et de toutes les fenêtres secondaires décrites dans votre fichier d'aide.| </html>
|ID d'accueil|Le titre de l'ID (par défaut) qui s'affiche lorsque l'observateur d'assistance est appelé sans indiquer d'ID.|
|Présentation|Les fenêtres dans lesquelles afficher les sujets d'assistance. Il s'agit d'une version moderne du programme informatique JavaHelp 2 décrit plus en détail ci-dessous \<presentation> .|
|Sous-helpsets|Cette zone discrétionnaire incorpore statiquement d'autres helpsets en utilisant la balise. Les ensembles d'aide affichés par cette balise sont combinés naturellement dans l'ensemble d'aide qui contient la balise. Plus de points d'intérêt autour de la fusion peuvent être trouvés dans Blending Helpsets.|
|Implementation|Ce segment discrétionnaire crée un registre qui donne le mappage des informations clés pour caractériser la classe HelpBroker à utiliser dans la méthode HelpSet.createHelpBroker. Le registre décide en outre du visualiseur de substance au client pour un type Emulate donné.|

## Format de fichier Java HS

Les fichiers Java HS sont au format XML et sont basés sur la recommandation proposée par le World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Cela signifie qu'un fichier Java HS est au format de fichier XML lisible par l'homme et peut être ouvert dans n'importe quelle application de lecture XML.

### Exemple de format de fichier Java HS

Voici un exemple de fichier d'aide à partir de [documentation Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## Références
* [Fichier Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Format de fichier de script Haskell

## Qu'est-ce qu'un fichier SH ?

Un fichier avec l'extension .hs est un fichier Haskell Script écrit en [Haskell](https://wiki.haskell.org/Haskell), un langage de programmation open source avancé purement fonctionnel. Le code écrit dans le fichier HS est purement basé sur des fonctions, contrairement à [C](/fr/programming/c/), [C++](/fr/programming/cpp/) et similaires, qui suivent les principes de développement rapide de logiciels robustes et concis. Haskell fournit une concurrence et un parallélisme intégrés ainsi que des API riches, des profileurs et des débogueurs pour produire des applications flexibles et de haute qualité.

## Format de fichier SH

Comme tout langage de programmation, les fichiers HS sont écrits au format texte brut lisible par l'homme. Ceux-ci peuvent être créés, modifiés et visualisés avec tous les outils de texte disponibles. Le fichier de code source .hs est compilé avec un compilateur Haskell, générant le fichier binaire exécutable.

### Exemple de format de fichier HS

Le code peut être écrit dans un fichier .hs et compilé à l'aide d'un compilateur Haskell tel que [GHC](https://haskell.org/ghc). La ligne de code suivante est enregistrée sous `HelloWorld.hs`, comme illustré dans l'exemple suivant.

```
main = putStrLn "Hello, World!"
```

Ceci est compilé à l'aide de la commande :

```
$ ghc -o hello hello.hs
```
et le fichier exécutable résultant peut être exécuté comme :

```
$ ./hello
```
Cela imprime le "Hello, World!" déclaration à la sortie.

## Références

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell en 5 étapes faciles](https://wiki.haskell.org/Haskell_in_5_steps)

