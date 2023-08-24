{
  "date" : "2019-12-03",
  "keywords" :[ "GLB", "file", "formato", "tipo di file", "estensione", "cos'è un file GLB?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Scopri il formato di file GLB e le API che possono aprire e creare file GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Che cos'è un file GLB?

GLB è la rappresentazione in formato file binario di modelli 3D salvati nel formato di trasmissione GL ([glTF](/it/3d/gltf/)). Informazioni su modelli 3D come gerarchia dei nodi, telecamere, materiali, animazioni e mesh in formato binario. Questo formato binario archivia l'asset glTF (JSON, .bin e immagini) in un BLOB binario. Evita anche il problema dell'aumento della dimensione del file che si verifica in caso di glTF. Il formato file GLB si traduce in dimensioni di file compatte, caricamento rapido, rappresentazione completa della scena 3D ed estensibilità per un ulteriore sviluppo. Il formato utilizza model/gltf-binary come tipo MIME.

## Formato file GLB - Ulteriori informazioni

I metodi di consegna dei contenuti utilizzati da glTF comportano un'elaborazione aggiuntiva per decodificare i dati binari codificati in base 64 e aumentano anche le dimensioni del file del 33%. Questi metodi di consegna, che hanno contribuito alla formazione del formato di file GLB, includono:

* glTF JSON punta a dati binari esterni (geometria, fotogrammi chiave, skin) e immagini.
* glTF JSON incorpora dati binari con codifica base64 e immagini inline utilizzando URI di dati.

GLB come formato contenitore è stato introdotto come formato di file binario per la rappresentazione della risorsa glTF in un BLOB binario per evitare i problemi causati da glTF. Il formato del file GLB [specifiche](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) dovrebbe essere indicato per qualsiasi implementazione del lettore/scrittore dello stesso per lo sviluppo di applicazioni .

## Struttura del file GLB

Il formato del file GLB si basa su little endian e la sua struttura mostra che contiene:

* Un preambolo di 12 byte, intitolato header.
* Uno o più blocchi che contengono contenuto JSON e dati binari.

#### Intestazione GLB

L'intestazione del formato file GLB è composta da tre voci da 4 byte:

* uint32 magic - magic è uguale a 0x46546C67. È una stringa ASCII glTF e può essere utilizzata per identificare i dati come glTF binari
* uint32 version - indica la versione del formato contenitore Binary glTF
* uin32 length - la lunghezza totale di Binary glTF, incluso Header e tutti i blocchi in byte

#### Pezzi

Ogni pezzo in un file GLB ha la seguente struttura:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - lunghezza di chunkData in byte
* `chunkType` - indica il tipo di blocco
* `chunkData` - carico utile binario del pezzo

dove sono i tipi di blocchi:

|# |Tipo di blocco|ASCII|Descrizione|Ricorrenze
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Contenuto JSON strutturato|1
|2.|0x004E4942|BIN|Buffer binario|0 o 1

L'inizio e la fine di ogni blocco devono essere allineati al limite di 4 byte e il riempimento deve essere utilizzato per questo scopo.

##### Contenuto JSON strutturato

Questo dovrebbe essere il primo pezzo di asset Binary glTF e consente all'implementazione di recuperare progressivamente le risorse dai blocchi successivi. Ciò fornisce anche la capacità di leggere solo un sottoinsieme selezionato di risorse da un asset glTF binario come il LOD più grossolano di una mesh. Per soddisfare i requisiti di allineamento, questo blocco deve essere riempito con caratteri spaziali finali (0x20).

##### Buffer binario #####

Questo pezzo contiene il carico utile binario per geometria, fotogrammi chiave di animazione, skin e immagini. Dovrebbe essere il secondo pezzo dell'asset Binary glTF e deve essere riempito con zeri finali (0x00) per soddisfare i requisiti di allineamento.

## Riferimenti ##

* [Specifiche del formato file GLB - Khronos](/it/3d/gltf/)

