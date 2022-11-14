{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PDF/VT",
  "description":"En savoir plus sur le format de fichier PDF/VT et les API qui peuvent créer et ouvrir des fichiers PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Qu'est-ce que PDF/VT ? #

PDF/VT, publié sous [ISO 16612-2](https://www.iso.org/standard/46428.html) en août 2010 en tant que norme, est conçu pour permettre l'impression de documents variables (VDP) dans une variété de environnements. La norme fait des informations variables et de l'impression transactionnelle la base de la norme. L'impression de données variables est utilisée lorsqu'une partie de l'information est différente pour chaque destinataire du contenu. L'impression transactionnelle comprend des factures, des relevés et d'autres documents qui combinent des informations de facturation avec des informations marketing. Cela se traduit par un mélange de traitement amélioré des images, du texte et d'autres types de contenu. PDF/VT permet une gestion fiable et dynamique des pages pour les données d'impression HVTO (High Volume Transactional Output) en utilisant le concept de métadonnées de partie de document (DPM). Les fichiers PDF/VT peuvent être ouverts dans Adobe Acrobat Viewer sans qu'il soit nécessaire d'ajouter un autre composant.

## Hiérarchie des parties de document ##

La hiérarchie des parties de document (DPart) ressemble à une structure arborescente de nœuds de partie de document basée sur toutes les pages du document. Les éléments de cet arbre sont appelés nœuds DPart. Chaque nœud interne contient d'autres nœuds DPart et chaque nœud feuille spécifie une ou plusieurs pages pour un destinataire. Essentiellement, la hiérarchie DPart spécifie la séquence et la relation des documents ou parties de documents dans un fichier PDF/VT. L'arborescence des nœuds DPart représente facilement le contenu interne d'un document PDF/VT car il peut contenir des sous-documents pour de nombreux destinataires et chaque partie de document correspond aux pages d'un seul destinataire. La hiérarchie DPart est requise dans les fichiers PDF/VT.

## Métadonnées de partie de document (DPM) ##

Les métadonnées de partie de document (DPM) sont associées à chaque nœud de la hiérarchie des parties de document et peuvent être utilisées pour communiquer des informations sur le sous-document d'un destinataire particulier et ses parties. En particulier, le DPM peut contenir des informations sur les propriétés ou des informations sur les destinataires sous une forme codée.

## Niveaux de conformité ##

PDF/VT est conféré aux trois niveaux de conformité suivants. Ils sont tous basés sur [PDF](/fr/pdf/) 1.6.

* `PDF/VT-1` - Il est basé sur PDF/X-4 et contient toutes les ressources nécessaires au rendu d'un document PDF.
* `PDF/VT-2` - Conçus pour l'échange de plusieurs fichiers, les documents PDF/VT-2 peuvent faire référence à des intentions de sortie externes, à des contenus externes ou aux deux. Un document PDF/VT et tous ses fichiers PDF référencés et les intentions de sortie externes sont collectivement appelés un ensemble de fichiers PDF/VT-2. Acrobat 9 et prennent en charge cette fonctionnalité.
* `PDF/VT-2s` - Prend en charge la diffusion en direct PDF/VT-2. Cela permet de traiter des sections segmentées de données.

## Références ##

* [PDF/VT - Par Wikipédia](https://en.wikipedia.org/wiki/PDF/VT)
* [Technologie graphique ISO 16612-2] (https://www.iso.org/standard/46428.html)

