{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","fichier", "format", "type de fichier", "extension","qu'est-ce qu'un fichier DOCX ?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"En savoir plus sur le format de fichier DOCX et les API qui peuvent créer et ouvrir des fichiers DOCX.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Qu'est-ce qu'un fichier DOCX ? ##

DOCX est un format bien connu pour les documents Microsoft Word. Introduit à partir de 2007 avec la sortie de Microsoft Office 2007, la structure de ce nouveau format de document est passée de binaire simple à une combinaison de fichiers XML et binaires. Les fichiers Docx peuvent être ouverts avec Word 2007 et les versions latérales, mais pas avec les versions antérieures de MS Word qui prennent en charge les extensions de fichier DOC.

## Bref historique ##

Après que Microsoft a ouvert les spécifications du format de fichier DOC, il était facile pour ses concurrents de rétroconcevoir le format et de fournir le même support dans leurs propres applications. De plus, la concurrence d'Open Office sous la forme de son Open Document Format, a contraint Microsoft à adopter des normes plus ouvertes et plus larges. C'est au début des années 2000 que Microsoft a décidé d'opter pour le changement afin de s'adapter à la norme **Office Open XML**. Les documents sous cette nouvelle norme ont reçu [extension .docx](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), le "X" étant pour XML. En 2007, ce nouveau format de fichier a été intégré à Office 2007 et est également repris dans les nouvelles versions de Microsoft Office. Le nouveau type de fichier a ajouté des avantages de petites tailles de fichiers, moins de changements de corruption et une représentation d'images bien formatées.

## Spécifications du format de fichier DOCX - Plus d'informations

Un fichier Docx comprend une collection de fichiers XML contenus dans une archive ZIP. Le contenu d'un nouveau document Word peut être visualisé en décompressant son contenu. La collection contient une liste de fichiers XML classés comme :

* Fichiers de métadonnées - contient des informations sur les autres fichiers disponibles dans l'archive
* Document - contient le contenu réel du document

### Fichiers de métadonnées ###

Microsoft Word utilise ces fichiers pour trouver la relation entre les fichiers et pour localiser le contenu du document. Lorsqu'une archive de document Word est extraite, elle contient un certain nombre de fichiers de ce type, comme indiqué ci-dessous.

#### Relations - \_rels/.rels ####

Ce fichier contient des informations indiquant à MS Word où rechercher le contenu du document et d'autres références. Chaque relation est identifiée par un identifiant de relation unique et spécifie le fichier XML référencé comme cible. Un exemple de fichier de relations est illustré ci-dessous :

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Types de contenu ####

Un document peut contenir plusieurs types de médias à l'intérieur, tels que des images, des thèmes, des illustrations textuelles, etc. Le [Content_Types].xml contient des informations sur ces types de médias présents dans le document. Le contenu d'un tel fichier XML est affiché comme suit :

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### Références aux ressources - \_rels/document.xml.rels ####

Les informations sur les ressources, telles que les images intégrées dans le document, sont référencées dans ce fichier XML.

#### Contenu principal du document ####

Il s'agit du fichier XML principal de l'archive qui contient le contenu textuel du document. Ce contenu est représenté par une variété de nœuds conformément aux spécifications OpenOffice XML. La plupart du temps, le contenu de ce fichier se compose de paragraphes et de tableaux, bien qu'il puisse également s'agir d'autres nœuds.

### Nœuds de format de fichier ###

Le fichier document.xml principal est une collection de nœuds pour la représentation du contenu global d'un fichier. Chaque nœud a un début et une fin qui encapsulent soit d'autres nœuds, soit le contenu. Un exemple simplifié d'un tel fichier xml est le suivant :

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Voici les informations sur certains des nœuds contenus dans un fichier DOCX pour la représentation du contenu.

`<w:document> ` - Représente l'élément racine du contenu principal du fichier.

`<w:body> ` - Représente le corps du document qui peut comprendre de nombreux autres nœuds d'éléments tels que des paragraphes, des tableaux et des sections.

#### Paragraphes ####

Un paragraphe est le principal support de contenu d'un document. Il est représenté par **<w:p> ** élément dans un document. Un paragraphe se compose en outre d'un ou plusieurs passages **<w:r> ** qui contient le texte réel du paragraphe. En plus des séquences, les paragraphes peuvent également contenir d'autres éléments de document tels que des liens hypertexte, des commentaires, etc. Un exemple de structure de paragraphe est illustré ci-dessous :

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## Références ##

* [MS - Format de fichier DOCX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML] (http://officeopenxml.com/)

