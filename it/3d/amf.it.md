{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "file amf", "formato file amf", "formato file", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file AMF e le API che possono aprire e creare file AMF.",
  "title" :"AMF - File di produzione additiva",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file AMF?
Un file AMF è costituito da linee guida per la descrizione degli oggetti da utilizzare nei processi di produzione additiva. Contiene un'apertura<amf> tag XML e termina con a</amf> elemento. Questo è preceduto da una riga di dichiarazione XML che specifica la versione XML e la codifica del file. Le dichiarazioni possono includere informazioni sulle unità di misura e, in assenza di tali informazioni, vengono utilizzati i millimetri come unità di default.


## Formato file AMF

Il formato file di produzione additiva (**AMF**) definisce standard aperti per la descrizione degli oggetti da utilizzare nei processi di produzione additiva come la stampa 3D. I programmi CAD utilizzano il formato di file AMF utilizzando informazioni come geometria, colore e materiale degli oggetti. AMF è diverso dal formato STL in quanto il lato non supporta colore, materiali, reticoli e costellazioni.

### Elementi di un file AMF

I cinque elementi di primo livello definiti con il<AMF> i tag sono come dettagliato di seguito. La presenza di un singolo elemento oggetto è necessaria per un file AMF completamente funzionante.

`<object> ` - L'elemento oggetto definisce uno o più volumi di materiale, ciascuno dei quali è associato a un ID materiale per la stampa. Almeno un elemento oggetto deve essere presente nel file. Gli oggetti aggiuntivi sono facoltativi.

`<material> ` - L'elemento materiale facoltativo definisce uno o più materiali per la stampa con un ID materiale associato. Se non viene incluso alcun elemento materiale, si presume un unico materiale di default.

`<texture> ` - L'elemento texture opzionale definisce una o più immagini o texture per la mappatura dei colori o delle texture, ciascuna con un ID texture associato.

`<constellation> ` - L'elemento facoltativo della costellazione combina gerarchicamente oggetti e altre costellazioni in un modello relativo per la stampa.

`<metadata> ` - L'elemento metadata opzionale specifica informazioni aggiuntive sugli oggetti e sugli elementi contenuti nel file.

## Esempio AMF

Di seguito è riportato un esempio di file AMF che può essere copiato in un file [testo](/it/elaborazione testi/txt/) e salvato come file compresso [zip](/it/compressione/zip/) per l'apertura.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Riferimenti

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Specifiche AMF su ISO](https://www.iso.org/standard/67472.html)

