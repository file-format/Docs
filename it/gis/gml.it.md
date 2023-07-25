{
  "date" : "2019-10-11",
  "keywords" :[ "file gml", "che cos'è un file gml", "file", "esempio gml", "estensione file gml", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Formato file del linguaggio di markup geografico",
  "description":"Scopri il formato di file GML e le API che possono creare e aprire file GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file GML?

GML sta per Geography Markup Language, basato su specifiche XML sviluppate dall'Open Geospatial Consortium (OGC). Il formato viene utilizzato per memorizzare le caratteristiche dei dati geografici per l'interscambio tra diversi formati di file. Serve come linguaggio di modellazione per i sistemi geografici e come formato di interscambio aperto per le transazioni geografiche su Internet.

## Formato file GML ##

Come con la maggior parte delle grammatiche basate su XML, ci sono due parti della grammatica: lo schema che descrive il documento e il documento di istanza che contiene i dati effettivi. Un documento GML viene descritto utilizzando uno schema GML. Ciò consente a utenti e sviluppatori di descrivere set di dati geografici generici che contengono punti, linee e poligoni. Utilizzando gli schemi dell'applicazione, gli utenti possono fare riferimento a strade, autostrade e ponti invece di punti, linee e poligoni.

Vale la pena notare che GML non dovrebbe essere interpretato per la rappresentazione di dati spaziali su mappe. La rappresentazione del contenuto GML è diversa dallo scopo per cui GML è stato creato. In breve, GML è simile a XML in quanto viene utilizzato solo per contenere i contenuti spaziali che possono essere utilizzati dalle applicazioni di mappatura a scopo di visualizzazione.

### Formazione di contenuti in GML ###

GML rappresenta i dati spaziali utilizzando caratteristiche che sono un elenco di proprietà e geometrie. Una proprietà ha un nome, un tipo e una descrizione del valore. Le geometrie sono composte da elementi costitutivi della geometria di base come:

* punti
* linee
* curve
* sufraces e
* poligoni

Le future versioni di GML sono progettate per supportare la geometria 3D e le relazioni topologiche tra le caratteristiche.

La codifica GML consente già funzionalità piuttosto complesse. Una caratteristica può ad esempio essere composta da altre caratteristiche. Una singola caratteristica come un aeroporto potrebbe quindi essere composta da altre caratteristiche come le vie dei taxi, le piste, gli hangar e gli aerostazioni. La geometria di una caratteristica geografica può anche essere composta da molti elementi geometrici. Una caratteristica geometricamente complessa può quindi consistere in un mix di tipi di geometria inclusi punti, stringhe di linee e poligoni.

### Esempi ###

GML 1.0 e 2.0 codificano oggetti Polygons, Points e LineString come segue:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Riferimenti ##

* [Specifiche GML](https://www.ogc.org/standard/gml/)
* [GML - Di Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

