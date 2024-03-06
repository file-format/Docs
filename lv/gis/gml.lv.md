{
  "date": "2019-10-11",
  "keywords": [
"gml failu",
"kas ir gml fails",
"failu",
"gml piemērs",
"gml faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GML — ģeogrāfijas iezīmēšanas valodas faila formāts",
  "description": "Uzziniet par GML failu formātu un API, kas var izveidot un atvērt GML failus.",
  "linktitle": "GML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gm-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir GML fails?

GML apzīmē ģeogrāfijas iezīmēšanas valodu, kas ir balstīta uz XML specifikācijām, ko izstrādājis Open Geospatial Consortium (OGC). Formāts tiek izmantots, lai saglabātu ģeogrāfisko datu objektus, lai veiktu apmaiņu starp dažādiem failu formātiem. Tas kalpo kā ģeogrāfisko sistēmu modelēšanas valoda, kā arī atvērts apmaiņas formāts ģeogrāfiskiem darījumiem internetā.

## GML faila formāts ##

Tāpat kā lielākajā daļā uz XML balstītu gramatiku, gramatikai ir divas daļas – shēma, kas apraksta dokumentu, un instances dokuments, kurā ir faktiskie dati. GML dokuments ir aprakstīts, izmantojot GML shēmu. Tas ļauj lietotājiem un izstrādātājiem aprakstīt vispārīgas ģeogrāfisko datu kopas, kas satur punktus, līnijas un daudzstūrus. Izmantojot lietojumprogrammu shēmas, lietotāji var atsaukties uz ceļiem, lielceļiem un tiltiem, nevis uz punktiem, līnijām un daudzstūriem.

Ir vērts atzīmēt, ka GML nevajadzētu interpretēt telpisko datu attēlošanai kartēs. GML satura attēlojums atšķiras no mērķa, kuram GML tika izveidots. Īsāk sakot, GML ir līdzīgs XML, jo tas tiek izmantots tikai telpiskā satura glabāšanai, ko var izmantot kartēšanas lietojumprogrammām displeja nolūkos.

### Satura veidošana GML ###

GML represents spatial data using features which is a list of properties and geometries. A Property has a name, type and value description. Geometries are composed of basic geometry building blocks such as:

* punkti

* līnijas

* līknes

* virsmas un

* daudzstūri


Plānots, ka nākamās GML versijas atbalstīs 3D ģeometriju, kā arī topoloģiskās attiecības starp iezīmēm.

GML kodējums jau pieļauj diezgan sarežģītas funkcijas. Funkcija, piemēram, var sastāvēt no citiem līdzekļiem. Atsevišķs elements, piemēram, lidosta, varētu sastāvēt no citiem elementiem, piemēram, taksometru ceļiem, skrejceļiem, pakaramiem un gaisa termināļiem. Ģeogrāfiskā objekta ģeometriju var veidot arī daudzi ģeometrijas elementi. Tādējādi ģeometriski sarežģīts elements var sastāvēt no ģeometrijas veidu kombinācijas, tostarp punktiem, līniju virknēm un daudzstūriem.

### Piemēri ###

GML 1.0 un 2.0 kodē daudzstūra, punktu un līniju virknes objektus šādi:

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

## Atsauces Nr.

* [GML specifikācijas](https://www.ogc.org/standard/gml/)

* [GML — Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)


