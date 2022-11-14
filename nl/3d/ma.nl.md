{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma-bestand", "ma-bestandsindeling", "bestandsindeling", "3d", "ma-bestand downloaden", ".ma-bestand", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over MA-bestandsindeling en API's die MA-bestanden kunnen openen en maken.",
  "title" :"MA-bestandsindeling",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Wat is een MA-bestand?

Een bestand met de extensie .ma is een 3D-projectbestand dat is gemaakt met de Autodesk Maya-toepassing. Het bevat een grote lijst met tekstuele opdrachten om informatie over het bestand te specificeren. Een **.ma-bestand** kan in elke teksteditor worden geopend en bewerkt om eventuele problemen met de opdrachten op te lossen voor het geval een bestand beschadigd raakt. Deze bestanden bevatten informatie voor het definiëren van de 3D-scène-informatie, zoals geometrie, belichting, animatie en weergave.

## MA-bestandsindeling

MA-bestanden worden op schijf opgeslagen in ASCII-tekstindeling, in tegenstelling tot de MB-bestanden die in binaire bestandsindeling op schijf worden opgeslagen. Een gedetailleerde referentie voor het MA-bestandsformaat is beschikbaar in [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) en kan worden doorverwezen om ter referentie van de ontwikkelaar.

### MA Bestandskop

De header van het MA-bestand begint met een gedeelte met opmerkingen dat de aanmaakinformatie van het bestand en de wijzigingsdatum geeft. Maya-bestandslezers negeren dit blok omdat het alleen voor informatieve doeleinden wordt gebruikt. Een koptekst moet echter beginnen met de eerste zes tekens als "//Maya".

De kop van het ASCII-bestand ziet er als volgt uit.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Bestandsverwijzingen

De sectie met bestandsverwijzingen van een .ma-bestand bevat informatie over alle andere Maya-bestanden waarnaar in dit bestand wordt verwezen. Elk bestand waarnaar wordt verwezen, kan worden gelezen met behulp van een enkele bestandsopdracht die zich in hetzelfde bestand bevindt. De syntaxis van de bestandsopdracht wanneer deze wordt gebruikt voor verwijzingen is:

```
file -r -rpr prefixString fileName;
```
of

```
file -r -ns nameSpace fileName
```
Hier is een voorbeeldreeks.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Dit voorbeeld laat zien dat het sun-object in het bestand `solar` in dit bestand toegankelijk zou zijn met de naam "solar_sun".

### Vereisten

Het gedeelte Vereisten van een .ma-bestand bestaat uit een reeks vereiste opdrachten en vertelt May-informatie zoals versie- en plug-in-informatie die nodig is om de bestanden te lezen. Een voorbeeld van een sectie met vereisten is als volgt.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


In de volgende sectie worden de vereisten gespecificeerd. Dit bestaat uit een reeks vereiste opdrachten. Dit gedeelte van het bestand vertelt Maya welke software nodig is om het bestand correct te laden. Specifiek, welke versie van Maya en welke plug-ins.

## MA-bestand downloaden
Het is een beetje moeilijk om het MA-bestand van een 3D-model te vinden en te downloaden. Daarom kunt u hier een voorbeeld MA-bestand downloaden:

- [Voorbeeld.ma](../voorbeeld.ma)


## Referenties

* [Organisatie van Maya ASCII-bestanden - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

