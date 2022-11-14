{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "file ma", "formato file ma", "formato file", "3d", "download file ma", "file .ma", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file MA e le API che possono aprire e creare file MA.",
  "title" :"Formato file MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Che cos'è un file MA?

Un file con estensione .ma è un file di progetto 3D creato con l'applicazione Autodesk Maya. Contiene un ampio elenco di comandi testuali per specificare le informazioni sul file. Un **file .ma** può essere aperto e modificato in qualsiasi editor di testo per risolvere eventuali problemi con i comandi nel caso in cui un file venga danneggiato. Questi file contengono informazioni per definire le informazioni sulla scena 3D come geometria, illuminazione, animazione e rendering.

## Formato file MA

I file MA vengono salvati su disco in formato testo ASCII a differenza dei file MB che vengono salvati in formato file binario su disco. Un riferimento dettagliato per il formato di file MA è disponibile in [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) e può essere fatto riferimento a per riferimento dello sviluppatore.

### Intestazione del file MA

L'intestazione del file MA inizia con una sezione di commenti che fornisce le informazioni sulla creazione del file e la data di modifica. I lettori di file Maya ignorano questo blocco poiché viene utilizzato solo a scopo informativo. Tuttavia, un'intestazione deve iniziare con i primi sei caratteri come "//Maya".

L'intestazione del file ASCII ha il seguente aspetto.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Riferimenti ai file

La sezione dei riferimenti ai file di un file .ma contiene informazioni su tutti gli altri file Maya a cui si fa riferimento in questo file. Ciascun file di riferimento può essere letto utilizzando un comando di file singolo contenuto nello stesso file. La sintassi del comando file quando viene utilizzato per fare riferimento è:

```
file -r -rpr prefixString fileName;
```
o

```
file -r -ns nameSpace fileName
```
Ecco una stringa di esempio.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Questo esempio mostra che l'oggetto sole contenuto nel file `solar` sarebbe accessibile in questo file usando il nome "solar_sun".

### Requisiti

La sezione dei requisiti di un file .ma è costituita da una serie di comandi richiesti e fornisce informazioni a May come le informazioni sulla versione e sul plug-in necessarie per leggere i file. Un esempio di sezione dei requisiti è il seguente.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


La sezione successiva specifica i requisiti. Consiste in una serie di comandi require. Questa sezione del file indica a Maya quale software è necessario per caricare correttamente il file. In particolare, quale versione di Maya e quali plug-in.

## Download del file M.A
È un po' difficile trovare e scaricare il file MA di un modello 3d. Pertanto, puoi scaricare un file MA di esempio da qui:

- [Sample.ma](../sample.ma)


## Riferimenti

* [Organizzazione dei file Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

