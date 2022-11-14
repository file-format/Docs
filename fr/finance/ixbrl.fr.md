{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","fichier ixbrl", "format de fichier ixbrl", "type de fichier ixbrl", "fichier", "type", "qu'est-ce qu'un fichier ixbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - Format de fichier de rapports commerciaux et financiers",
  "description":"En savoir plus sur le format de fichier IXBRL et les API qui peuvent créer et ouvrir des fichiers IXBRL.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Qu'est-ce qu'un fichier iXBRL ?

Le format de fichier iXBRL (ilnine XBRL) permet d'intégrer des données [XBRL](/fr/web/xbrl/) dans un fichier HTML pour le rendre lisible par machine et par l'homme. Il s'agit en fait d'un fichier [xHTML](/fr/web/xhtml/) qui utilise les balises XBRL et a été développé par XBRL International pour répondre aux exigences du HMRC du Royaume-Uni. À l'aide d'iXBRL, les états financiers peuvent être créés en conservant intacte la mise en page du document d'origine. Les fichiers iXBRL peuvent être ouverts dans n'importe quel éditeur de texte tel que le Bloc-notes sur le système d'exploitation Windows et TextEdit sur MacOS.

## Format de fichier iXBRL

À l'intérieur de l'iXBRL, le contenu de XBRL est encapsulé dans un format de fichier xHTML qui utilise des balises XML. Comme XBRL,<xbrl> est l'élément racine des fichiers iXBRL. Le format XHTML représente son contenu comme une collection de différents types de documents et modules. Tous les fichiers en XHTML sont basés sur le format de fichier XML et sont conformes aux normes de document XML. XHTML est le format d'utilisation essentielle pour l'utilisation opérationnelle du modèle d'objet de document (DOM) [HTML](/fr/web/html/) dépendant ou du modèle d'objet de document [XML](/fr/web/xml/). Pour le monde extérieur, iXBRL respecte les spécifications du format de fichier [xHTML](/fr/web/xhtml/).

### iXBRL contre XBRL

XBRL peut être comparé à iXBRL sur la base des facteurs suivants :

* Complexité
* Options de formatage
* Types de fichiers/Extensions
* Option de rendu
* Processus de dépôt

Le tableau suivant illustre ces différences.

|Paramètre|XBRL|iXBRL|
---|---|---|
|Complexité|Plus complexe qu'iXBRL|Moins complexe en raison du schéma d'organisation existant de XHTML|
|Options de formatage|Flexibilité limitée|Grande flexibilité pour le formatage du contenu|
|Types de fichiers/Extension|Formellement enregistré avec l'extension .xml|Généralement enregistré sous l'extension .html ou .xhtml|
|Options de rendu|Visionneuses XBRL requises pour les visualiser|Contenu lisible par l'homme pouvant être visualisé dans les navigateurs|
|Processus de dépôt| Les documents d'instance XBRL (lisibles par machine) et HTML (lisibles par l'homme) doivent être déposés séparément.|Les formats lisibles par l'homme et lisibles par machine sont disponibles dans un seul document d'instance|

## Références

* [XBRL - Par Wikipédia](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

