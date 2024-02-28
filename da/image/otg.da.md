{
  "date": "2020-01-10",
  "keywords": [
"otg fil",
"otg filformat",
"hvad er en otg-fil",
"fil",
"otg eksempel",
"otg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTG - OpenDocument Drawing Template File Format",
  "description": "Lær om OTG filformat og API'er, der kan oprette og åbne OTG filer.",
  "linktitle": "OTG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ot-dag"
}
},
  "lastmod": "2020-01-10"
}

## Hvad er en OTG fil?

En OTG-fil er en tegneskabelon, der er oprettet ved hjælp af OpenDocument-standarden, der følger OASIS Office-applikationerne 1.0 specification. Det repræsenterer standardorganiseringen af tegningselementer til et vektorbillede, der kan bruges til yderligere at forbedre indholdet af filen. OTF-filer er ligesom alle andre OpenDocument-formatbaserede filer, der er baseret på XML-format for at repræsentere indholdet af dokumentet. OTF-filer kan ses ved at åbne dem i enhver tekst- eller standard XML-editor.

## OTG filformatspecifikationer ##

OTG-filformatet er baseret på OpenDocument XML-formatet, der har et veletableret skema. Strukturen af hver komponent i et OpenDocument-format er repræsenteret af et element, der har tilknyttede attributter og er fælles for alle dokumenttyper såsom tekstdokument, regneark eller en tegnefil. OTG, som er en tegneskabelon, bruger i vid udstrækning grafikindholdsspecifikationerne, der inkluderer:

  * Forbedrede sidefunktioner til grafiske applikationer
  * Tegne former
  * Rammer
  * 3D former
  * Brugerdefineret form
  * Præsentationsformer
  * Præsentationsanimationer
  * SMIL præsentationsanimationer
  * Præsentationsbegivenheder
  * Nuværende tekstfelter
  * Præsentationsdokumentets indhold

### Forbedrede sidefunktioner til grafiske applikationer ###
#### Handout Master ####

Handout Master-element er en skabelon til automatisk at generere uddelingssiderne til programmer, der understøtter udskrivning af sådanne sider.
De attributter, der kan være forbundet med `<style:handout-master> ` element er:

|Layout|Attribut|Beskrivelse
---|---|---|
|Præsentationssidelayout|præsentation:præsentationsside-layout-navn|Links til `<style:presentation-page-layout> ` attribut
|Sidelayout|`stil:side-layout-navn` | Angiver et sidelayout, der indeholder størrelserne, rammen og orienteringen af uddelings-mastersiden.
|Sidestil|`draw:style-name`|Tildeler yderligere formateringsattributter til en uddelingsmasterside ved at tildele en tegningssidestil.|
|Overskriftserklæring| `præsentation:brug-header-name`| Angiver navnet på den overskriftsfelterklæring, der bruges til alle overskriftsfelter, der vises på uddelingsmastersiden.
|Sidefoderklæring| presentation:use-footer-name|Specificerer navnet på sidefodsfelterklæringen, der bruges til alle sidefodsfelter, der vises på uddelingshovedsiden.
|Dato- og klokkeslætserklæring|use-date-time-name|Specificerer navnet på den dato- og klokkeslætsdeklaration, der bruges til alle dato- og klokkeslætsfelter, der vises på uddelingsmastersiden.

### Tegne figurer ###
OpenDocument-formatet understøtter flere tegningsformer, der kan bruges af enhver type dokument.

|Form|Associerede attributter| elementer
---|---|---|
Rektangel - `<draw:rect> `|Position, Størrelse, Stil, Lag, Z-indeks, ID, billedtekst-id, tekstanker, bordbaggrund, tegningsendeposition, runde hjørner|Titel, lang beskrivelse, begivenhedslyttere, limpunkter, tekst
Linje `<draw:line> `|Stil, lag, Z-indeks, ID, billedtekst-id og transformation, tekstanker, tabelbaggrund, tegningsslutposition, startpunkt, slutpunkt|titel, lang beskrivelse, hændelseslyttere, limpunkter, tekst
Polyline `<draw:polyline> `| Position, Størrelse, View box, Style, Layer, Z-Index, ID, Caption ID og Transformation, Tekstanker, tabelbaggrund, tegneslutposition, Points| Titel, lang beskrivelse, begivenhedslyttere, limpunkter, tekst
Polygon `<draw:polygon> `|Position, Størrelse, View box, Style, Layer, Z-Index, ID, Caption ID og Transformation, Tekstanker, tabelbaggrund, tegneslutposition, Points|Titel, Lang beskrivelse, Hændelseslyttere, Limpunkter, Tekst
|Almindelig polygon `<draw:regular-polygon> `|Position, størrelse, stil, lag, Z-indeks, id, billedtekst-id og transformation, tekstanker, bordbaggrund, tegningsendeposition, konkav, hjørner, skarphed|titel, lang beskrivelse, begivenhedslyttere, limpunkter, tekst
|Paht `<draw:path> `|Position, Størrelse, View box, Style, Layer, Z-Index, ID, Caption ID og Transformation,Tekstanker, tabelbaggrund, tegneslutposition, Stidata| Titel, lang beskrivelse, begivenhedslyttere, limpunkter, tekst

### Rammer ###
En ramme i et tegnedokument er en rektangulær beholder, der indeholder tekstbokse, billeder eller objekter. Rammer understøtter yderligere funktioner såsom konturer, billedkort og hyperlinks. En ramme kan indeholde et objekt såvel som et billede, hvilket gør det muligt at have flere gengivelser af et objekt. Applikationerne gengiver respektive element baseret på den bedste support.

Rammer kan indeholde:
  * Tekstbokse
  * Objekter repræsenteret enten i OpenDocument-formatet eller i et objektspecifikt binært format
  * Billeder
  * Applets
  * Plug-ins
  * Flydende rammer

En ramme er indeholdt i et dokument som vist nedenfor.

```
<define name=draw-frame>
<element name=draw:frame>
<ref name=common-draw-shape-with-text-and-styles-attlist/>
<ref name=common-draw-position-attlist/>
<ref name=common-draw-rel-size-attlist/>
<ref name=common-draw-caption-id-attlist/>
<ref name=presentation-shape-attlist/>
<ref name=draw-frame-attlist/>
<zeroOrMore>
<choice>
<ref name=draw-text-box/>
<ref name=draw-image/>
<ref name=draw-object/>
<ref name=draw-object-ole/>
<ref name=draw-applet/>
<ref name=draw-floating-frame/><ref name=draw-plugin/>
</choice>
</zeroOrMore>
<optional>
<ref name=office-event-listeners/>
</optional>
<zeroOrMore>
<ref name=draw-glue-point/>
</zeroOrMore>
<optional>
<ref name=draw-image-map/>
</optional>
<optional>
<ref name=svg-title/>
</optional>
<optional>
<ref name=svg-desc/>
</optional>
<optional>
<choice>
<ref name=draw-contour-polygon/><ref name=draw-contour-path/>
</choice>
</optional>
</element>
</define>
```

## Referencer ##
* [OASIS Open Document Format for Office-applikationer](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
