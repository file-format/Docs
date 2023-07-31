{
  "date" : "2020-01-11",
  "keywords" :[ "file x", "formato file x", "cos'è un file x", "file", "esempio x", "estensione file x", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Formato file DirectX 2.0",
  "description":"Scopri il formato di file DirectX X e le API che possono aprire e creare file DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Che cos'è un file X?

Un file con estensione .x fa riferimento a [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics formato file legacy introdotto con Microsoft DirectX 2.0. È stato utilizzato per il rendering di grafica 3D nei giochi e specifica le strutture per mesh, trame, animazioni e oggetti definiti dall'utente. È stato deprecato dal 2014 poiché il formato di file FBX di Autodesk funziona meglio come formato più moderno. X è basato su modelli ed è privo di qualsiasi conoscenza sull'utilizzo.

Puoi aprire i file DirectX X utilizzando Microsoft DirectX e comuni editor di testo.

## Formato file X

Il [riferimento al file X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) contiene informazioni di riferimento per gli elementi dell'API utilizzati per lavorare con i file DirectX .x. Il formato fornisce primitive di dati di basso livello che vengono utilizzate da altre applicazioni per definire primitive di livello superiore tramite modelli di dati. DirectX 6.0 ha introdotto interfacce e metodi che consentono di leggere e scrivere su file .x. DirectX 3.0 ha introdotto una versione binaria di questo formato di file.

Il [riferimento al formato file X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) definito da DirectX 9 contiene informazioni di riferimento per .x file in binari e codifiche di testo.

### Codifica binaria

Il [formato binario](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definisce il formato DirectX X come una rappresentazione tokenizzata del formato di testo. Questi token possono essere autonomi per fornire una struttura grammaticale o possono essere token di registrazione che forniscono i dati necessari.

#### Intestazione

L'intestazione binaria può essere letta e scritta utilizzando le seguenti definizioni.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Codifica del testo

I file DirectX .x non dipendono dal modo in cui viene utilizzato il file e non sono specifici di alcuna applicazione. Questo approccio basato su modelli consente di utilizzare il formato di file .x da qualsiasi applicazione client.


#### Intestazione

L'intestazione a lunghezza variabile è obbligatoria e deve trovarsi all'inizio del flusso di dati. L'intestazione contiene i seguenti dati.

|Tipo |Sottotipo |Dimensione |Contenuto |Significato contenuto|
---|---|---|---|---|
|Numero magico (richiesto)| | 4 byte |xdi |
|Numero versione (richiesto) |Numero principale |2 byte |03 |Versione principale 3|
| |Numero minore |2 byte |02 |Versione minore 2|
|Tipo formato (richiesto)| |4 byte |"txt " |File di testo|
| | | |"bin "| File binario|
| | | |"zip"| File di testo compresso MSZip|
| | | |"bzip"| File binario compresso MSZip|
|Dimensione del galleggiante (richiesto)| |4 byte| 0064| float a 64 bit|
| | | |0032 |virgola mobile a 32 bit|


## Riferimenti

* [X File Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Riferimento al formato file DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

