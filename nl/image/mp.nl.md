{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP-bestand - LaTeX MetaPost-bestand",
  "description":"Meer informatie over MP-bestandsindelingen en API's die MP-bestanden kunnen maken en openen.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Wat is een MP-bestand?

Een MP-bestand is een vectorafbeeldingsbestand dat is gegenereerd door de programmeertaal MetaPost om afbeeldingen te maken. Vectorafbeeldingen die zijn gemaakt met het MP-bestandsformaat worden opgeslagen als [EPS](/nl/image/eps/) (Encapsulated PostScript)-bestanden. Bovendien wordt MetaPost geleverd met TeX- en Metafont-frameworks en kunnen MP-bestanden worden gegenereerd vanuit de TEX- en LTX-bestanden die door deze applicaties worden gebruikt. MP-bestanden bevatten tekeninstructies en wiskundige algoritmische tekeningen voor het renderen van het EPS-uitvoerbestand. De PDFTex-engine kan de gemaakte EPS gebruiken om [PDF](/nl/pdf/)-bestanden rechtstreeks te genereren.

## MP-bestandsindeling

MP-bestanden worden op schijf opgeslagen als binaire bestanden en genereren EPS-uitvoer wanneer ze worden geëxporteerd naar het uitvoerbestandsformaat voor vectorafbeeldingen. Tekeningen die met MetaPost zijn gemaakt, worden in opgemaakte vorm opgenomen in technische documenten en tijdschriftpublicaties die met LaTex zijn gemaakt.

### MetaPost MP-bestandsvoorbeeld

Hieronder volgt een voorbeeld, waarnaar wordt verwezen vanuit [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), dat een pijl en de letter "A" net boven het midden van de pijl.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Referenties ##

* [MetaPost door Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Latex-voorbeeld Metapost door Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

