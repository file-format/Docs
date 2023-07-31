{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Présentation de la page de rapport",
  "keywords" :[ "rpl", "Mise en page du rapport", "XSD", "SQL Server", "rapports"],
  "description":"En savoir plus sur le format de flux RPL qui est un format binaire interne utilisé par Microsoft SQL Server Reporting Services lors du contact avec les contrôles de la visionneuse.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Qu'est-ce qu'un fichier RPL ? ##

Le format de flux RPL (Report Page Layout) est un format binaire interne utilisé par MS SQL Server Reporting Services lors du contact avec les contrôles de la visionneuse pour réduire une partie du travail de rendu du serveur au contrôle de la visionneuse client. Les développeurs peuvent créer des concepteurs de rapports personnalisés à l'aide de RPL, qui généreront des RPL ainsi que des moteurs de rendu de rapports personnalisés qui traitent et affichent le fichier RPL pour afficher les rapports.

## Structures RPL

Un flux RPL comprend une structure de flux, une structure de rapport, des propriétés de rapport et des énumérations. Chaque structure comprend les éléments suivants :

- Une définition de la structure.

- La grammaire de la forme Backus-Naur augmentée (ABNF) pour la structure.

- Un petit schéma de la structure.

- Définitions de tous les champs contenus dans la structure.

Voici les brèves notes sur certaines des structures RPL :

### Structure du flux
La structure du flux consiste en une série d'enregistrements. Un enregistrement contient zéro ou plusieurs champs structurés contenant la mise en page du rapport.

#### Flux RPL
Le flux RPL doit avoir un seul enregistrement de rapport et le flux doit être une série d'enregistrements binaires qui conservent la hiérarchie des rapports.

#### Enregistrement
L'enregistrement est un bloc de construction de base utilisé pour conserver les informations sur un rapport. Un enregistrement consiste en une séquence d'octets de longueur variable. Un enregistrement se compose de deux éléments :
- Un type d'enregistrement
- Les données d'enregistrement spécifiques à ce type d'enregistrement.
Le type d'enregistrement est un octet qui définit le type d'informations spécifié par l'enregistrement et la manière dont la structure des données d'enregistrement concernant l'enregistrement est ordonnée et structurée. La valeur de l'enregistrement dépend du type de données propre à cet enregistrement.

#### Structures de types de données simples

Le tableau suivant définit les types de données dans un flux RPL.

|Description| format|
---|---|
|Char|Représente une valeur numérique (ordinale) de 16 bits (2 octets).|
|Byte|Représente un entier non signé de 8 bits (1 octet).|
|Int16|Représente un entier signé de 16 bits (2 octets).|
|Single|Représente une valeur à virgule flottante simple précision de 32 bits (4 octets).|
|Decimal|Représente un type de données de 128 bits (16 octets).|
|DateTime|Représente un codage 64 bits (8 octets) d'une valeur de date et d'heure.|
|Int64|Représente un entier signé 64 bits (8 octets).|
|Int32|Représente un entier signé 32 bits (4 octets).|
|Float|Représente une valeur à virgule flottante simple précision de 32 bits (4 octets).|
|Booléen|Représente une valeur de type booléen logique 8 bits (1 octet). Les valeurs valides sont true (1) et false (0).|
|Long|Représente un entier signé 64 bits (8 octets).|
|String|Toutes les valeurs de chaîne dans le protocole DOIVENT être UNICODE UTF-16. Par défaut, toutes les valeurs de chaîne commencent par un entier qui définit la longueur de la chaîne. Les valeurs de chaîne sont représentées dans le protocole sous la forme d'un tableau d'octets ; le nombre d'octets DOIT être égal au nombre de caractères dans la chaîne multiplié par deux.|

### Structures de rapport
Les structures de rapport incluent les définitions et les tailles de leurs structures et éléments pertinents.

La liste suivante spécifie les structures de rapport :

- Signaler
- Version
- Propriétés du rapport
- Élément de tableau décalé
- Contenu de la page
- Page
- Propriétés de la page
- Mise en page
- Section
- Section simple
- Section Mixte
- Propriétés de la section
- Élément de zone corporelle
- Élément d'en-tête de page
- Élément de pied de page
- Élément de corps
- Propriétés des éléments
- Propriétés des éléments partagés
- Utiliser les propriétés d'éléments partagés
- InlineSharedElementProperties
- NonSharedElementProperties
- Style
- Propriétés de style partagé
- Propriétés de style non partagées
- ActionInfo
- ActionInfoContenu
- Action
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- Décalages de consolidation d'image
- ReportItem
- Ligne
- Image
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Graphique
- Panneau de jauge
- Carte
- Rectangle
- Sous-rapport
- RichTextBox
- Contenu du paragraphe
- TextRun
- Paragraphe
- RichTextBoxStructure
- Tableaux
- TablixContent
- Structure de tablix
- Mesures Tablix
- Largeurs des colonnes
- InfoColonne
- Hauteurs de ligne
- RowInfo
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Des mesures
- La mesure
- ReportElementEnd

### Propriétés
Voici la liste des propriétés pouvant être utilisées dans un flux RPL :

- IDENTIFIANT
- ColumnCount
- Espacement des colonnes
- Nom unique
- Nom
- Étiquette
- Signet
- Info-bulle
- Basculer l'élément
- La description
- Emplacement
- ConsumeContainerWhiteSpace (RPL 10.6)
- Langue
- Temps d'exécution
- Auteur
- Actualisation automatique
- Nom du rapport
- Hauteur de page
- Largeur de page
- Marge supérieure
- Marge gauche
- Marge droite
- Marge inférieure
- Colonnes
- Nom de page (RPL 10.6)
- Incliné
- Peut grandir
- PeutRéduire
- Évaluer
- Basculer l'état
- CanSort
- SortState
- Formule
- EstToggleParent
-TypeCode
- Valeur d'origine
- Est simple
- Décalage du contenu
- Nom du flux
- Dimensionnement
- Lien vers l'enfant
- Imprimer sur la première page
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- TraitéAvecErreur
- ImageMIMEType
- NomImage
- Largeur
- Hauteur
- Résolution horizontale
- Résolution verticale
- Format brut
- Lien hypertexte
- BookmarkLink
- ID d'extraction
- Url d'extraction
- Couleur de la bordure
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- Style de bordure
- BorderStyleLeft
- BorderStyleRight
- BordureStyleTop
- BorderStyleBottom
- Largeur de la bordure
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- Rembourrage gauche
- Rembourrage droit
- Rembourrage Haut
- Rembourrage en bas
- Le style de police
- Famille de polices
- Taille de police
- FontWeight
-Format
- Décoration de texte
- TextAlign
- Alignement vertical
- Couleur
- Hauteur de la ligne
- Direction
- Mode d'écriture
- UnicodeBiDi
- Image de fond
- Couleur de l'arrière plan
- Répétition du fond
- NumeralLanguage
- Variante numérique
- Calendrier
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Niveau
- MemberCellIndex
-CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- Index de colonne
- Index de ligne
- GroupLabel
- RecursiveToggleLevel
- Style de liste
- NiveauListe
- Numéro de paragraphe
- Retrait à droite
- Retrait à gauche
- Retrait suspendu
- EspaceAvant
- EspaceAprès
- Première ligne
- Balisage
- ContenuTop
- ContentLeft
- ContenuLargeur
- Hauteur du contenu
- État
- CellItemState
- MemberDefState

### Énumérations
La liste suivante montre les énumérations qui peuvent être utilisées dans le flux RPL :

- Options de tri
- Tailles
- Type de forme
- ImageRawFormat
- Styles de police
- FontWeights
- Décorations de texte
- Alignements de texte
- Alignements verticaux
- Les directions
- Modes d'écriture
- UnicodeBiDiTypes
- Calendriers
- Styles de bordure
- Types de répétition d'arrière-plan
- Styles de liste
- Styles de balisage
-TypeCode
- Valeurs d'état
- TablixMemberStateValues
- TablixMemberDefStateValues
- Taille RPL





## Références ##

- [Format de flux binaire de présentation de page de rapport (RPL)](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

