{
  "date" : "2020-01-10",
  "keywords" :[ "fichier otg", "format de fichier otg", "qu'est-ce qu'un fichier otg", "fichier", "exemple otg", "extension de fichier otg","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - Format de fichier de modèle de dessin OpenDocument",
  "description":"En savoir plus sur le format de fichier OTG et les API qui peuvent créer et ouvrir des fichiers OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Qu'est-ce qu'un fichier OTG ?

Un fichier OTG est un modèle de dessin créé à l'aide de la norme OpenDocument qui suit la spécification OASIS Office Applications [1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Il représente l'organisation par défaut des éléments de dessin pour une image vectorielle qui peut être utilisée pour améliorer davantage le contenu du fichier. Les fichiers OTF sont comme tous les autres fichiers basés sur le format OpenDocument qui sont basés sur le format XML pour représenter le contenu du document. Les fichiers OTF peuvent être visualisés en les ouvrant dans n'importe quel éditeur de texte ou XML standard.

## Spécifications du format de fichier OTG ##

Le format de fichier OTG est basé sur le format OpenDocument XML qui a un schéma bien établi. La structure de chaque composant d'un format OpenDocument est représentée par un élément qui a des attributs associés et est commun à tous les types de documents tels qu'un document texte, une feuille de calcul ou un fichier de dessin. OTG, étant un modèle de dessin, utilise largement les spécifications de contenu graphique qui incluent :

* Fonctionnalités de page améliorées pour les applications graphiques
* Dessiner des formes
* Cadres
* Formes 3D
* Forme personnalisée
* Formes de présentation
* Animations de présentation
* Animations de présentation SMIL
* Événements de présentation
* Présenter les champs de texte
* Contenu du document de présentation

### Fonctionnalités de page améliorées pour les applications graphiques ###
#### Document principal ####

L'élément Handout Master est un modèle permettant de générer automatiquement les pages du document pour les applications qui prennent en charge l'impression de telles pages.
Les attributs pouvant être associés au `<style:handout-master>` élément sont :

|Mise en page|Attribut|Description
---|---|---|
|Mise en page de la page de présentation|presentation:presentation-page-layout-name|Liens vers `<style:presentation-page-layout>`  attribut
|Mise en page|`style:page-layout-name` | Spécifie une mise en page qui contient les tailles, la bordure et l'orientation de la page maître du document.
|Style de page|`draw:style-name`|Attribue un attribut de mise en forme supplémentaire à une page maîtresse de document en attribuant un style de page de dessin.|
|Déclaration d'en-tête| `presentation:use-header-name`| Spécifie le nom de la déclaration de champ d'en-tête utilisée pour tous les champs d'en-tête affichés sur la page maître du document.
|Déclaration de pied de page| presentation:use-footer-name|Spécifie le nom de la déclaration de champ de pied de page utilisée pour tous les champs de pied de page affichés sur la page maître du document.
|Déclaration de date et d'heure|use-date-time-name|Spécifie le nom de la déclaration de champ date-heure utilisée pour tous les champs date-heure affichés sur la page maître du document.

### Dessiner des formes ###
Le format OpenDocument prend en charge plusieurs formes de dessin pouvant être utilisées par tout type de document.

|Forme|Attributs associés| éléments
---|---|---|
Rectangulaire - `<draw:rect>` |Position, Taille, Style, Calque, Z-Index, ID, ID de légende, Ancre de texte, arrière-plan du tableau, position de fin de dessin, Coins arrondis|Titre, Description détaillée, Écouteurs d'événements, Points de collage, Texte
Ligne `<draw:line> `|Style, Calque, Z-Index, ID, ID de légende et transformation, Ancre de texte, arrière-plan du tableau, position de fin de dessin, Point de départ, Point de fin|Titre, Description longue, Écouteurs d'événements, Points de collage, Texte
Polyligne `<draw:polyline> `| Position, taille, zone d'affichage, style, calque, index Z, ID, ID de légende et transformation, ancre de texte, arrière-plan du tableau, position de fin de dessin, points | Titre, description longue, écouteurs d'événement, points de liaison, texte
Polygone `<draw:polygon> `|Position, Taille, Zone d'affichage, Style, Calque, Z-Index, ID, ID de légende et transformation, Ancre de texte, arrière-plan du tableau, position de fin de dessin, Points|Titre, Description détaillée, Écouteurs d'événements, Points de collage, Texte
|Polygone régulier `<draw:regular-polygon> `|Position, Taille, Style, Calque, Z-Index, ID, ID de légende et transformation, Ancre de texte, arrière-plan du tableau, position de fin de dessin, Concave, Coins, Netteté|Titre, Description détaillée, Écouteurs d'événement, Points de collage, Texte
|Chemin `<draw:path> `|Position, Taille, Zone d'affichage, Style, Calque, Z-Index, ID, ID de légende et transformation, Ancre de texte, arrière-plan du tableau, position de fin de dessin, Données de chemin| Titre, description longue, écouteurs d'événement, points de liaison, texte

### Cadres ###
Un cadre, dans un document de dessin, est un conteneur rectangulaire qui contient des zones de texte, des images ou des objets. Les cadres prennent en charge des fonctionnalités supplémentaires telles que les contours, les images cliquables et les hyperliens. Un cadre peut contenir un objet ainsi qu'une image, permettant ainsi d'avoir plusieurs rendus d'un objet. Les applications rendent l'élément respectif basé sur le meilleur support.

Les cadres peuvent contenir :
* Zones de texte
* Objets représentés soit au format OpenDocument, soit dans un format binaire spécifique à l'objet
* Images
* Applets
* Plugins
* Cadres flottants

Un cadre est contenu dans un document comme illustré ci-dessous.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Références ##
* [Format de document ouvert OASIS pour les applications Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)

