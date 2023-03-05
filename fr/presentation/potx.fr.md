{
  "date" : "2019-10-11",
  "keywords" :[ "fichier potx", "format de fichier potx", "qu'est-ce qu'un fichier potx", "fichier", "exemple de potx", "extension de fichier potx","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :" POTX - Modèle de présentation Microsoft PowerPoint ",
  "description":"En savoir plus sur le format de fichier POTX et les API qui peuvent créer et ouvrir des fichiers POTX.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier POTX ?

Les fichiers avec l'extension .POTX représentent des présentations de modèles Microsoft PowerPoint créées avec Microsoft PowerPoint 2007 et versions ultérieures. Ce format a été créé pour remplacer le format de fichier [POT](/fr/presentation/pot/) basé sur le format de fichier binaire et pris en charge par PowerPoint 97-2003. Les fichiers générés peuvent être utilisés pour créer des présentations qui ont la même mise en page et d'autres paramètres requis pour être appliqués aux nouveaux fichiers. Ces paramètres peuvent inclure des styles, des arrière-plans, une palette de couleurs, des polices et des valeurs par défaut. Ces fichiers sont générés afin de créer des fichiers modèles prêts à l'emploi pour une utilisation officielle.

## Bref historique ##

C'est au début des années 2000 que Microsoft a décidé de changer pour s'adapter à la norme **Office Open XML**. Les documents, de différents types, sous cette nouvelle norme ont été identifiés en ajoutant "X" dans leurs extensions, "X" étant pour XML. En 2007, ce nouveau format de fichier a été intégré à Office 2007 et est également repris dans les nouvelles versions de Microsoft Office. Le nouveau type de fichier a ajouté des avantages de petites tailles de fichiers, moins de changements de corruption et une représentation d'images bien formatées.

## Spécifications du format de fichier ##

Les fichiers générés avec le format de fichier Office Open XML sont une collection de fichiers XML ainsi que d'autres fichiers qui fournissent des liens entre tous les fichiers constitutifs. Cette collection est en fait une archive compressée qui peut être extraite pour afficher son contenu. Pour ce faire, renommez simplement l'extension de fichier POTX avec zip et extrayez-la pour observer son contenu.

Les sections suivantes jettent un peu de lumière sur chacun d'eux.

### [Content_Types].xml ###

C'est le seul fichier qui se trouve au niveau de base lorsque le zip est extrait. Il répertorie les types de contenu pour les parties du package. Toutes les références aux fichiers XML inclus dans le package sont référencées dans ce fichier XML. Voici un type de contenu pour une partie de diapositive :
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Si de nouvelles pièces doivent être ajoutées au package, cela peut être fait en ajoutant la nouvelle pièce et en mettant à jour toutes les relations dans les fichiers .rels. Il faut garder à l'esprit que pour un tel changement, le Content_Types.xml doit également être mis à jour.

### \_rels (Dossier) ###

Les relations entre les autres parties et les ressources en dehors du package sont gérées par la partie relations. Le dossier Relations contient un seul fichier XML qui stocke les relations au niveau du package. Les liens vers les éléments clés des fichiers PPTX sont contenus dans ce fichier sous forme d'URI. Ces URI identifient le type de relation de chaque partie clé avec le package. Cela inclut la relation avec le document Office principal situé en tant que ppt/presentation.xml et d'autres parties dans docProps en tant que propriétés principales et étendues.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Chaque partie du document qui est la source d'une ou plusieurs relations aura sa propre partie de relations où chaque partie de relation se trouve dans un sous-dossier \_rels de la partie et est nommée en ajoutant ".rels" au nom de la partie. La partie principale du contenu (presentation.xml) a sa propre partie relations (presentation.xml.rels). Il contient des relations avec d'autres parties du contenu telles que slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, ainsi que les URI des liens externes.

#### Relation explicite ####

Pour une relation explicite, une ressource est référencée à l'aide de l'attribut Id d'un<Relationship> élément. C'est-à-dire que l'ID dans la source correspond directement à l'ID d'un élément de relation, avec une référence explicite à la cible.

Par exemple, une diapositive peut contenir un lien hypertexte tel que :
```
<a:hlinkClick r:id#"rId2">
```
Le r:id#"rId2" fait référence à la relation suivante dans la partie relations de la diapositive (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Relation implicite ####

Pour une relation implicite, il n'y a pas de référence directe à un `<Relationship> Id`. Au lieu de cela, la référence est comprise.

### Dossier ppt ###

C'est le dossier principal qui contient tous les détails sur le contenu de la présentation. Par défaut, il contient les dossiers suivants :

* \_rels
* thème
* diapositives
* slideLayouts
* slidemasters

et les fichiers xml suivants :

* présentation.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Références ##

* [[MS-PPTX] - Format de fichier PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

