{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "file", "estensione", "formato", "Formato file 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato dei file per sapere cos'è un file FBX e le API che possono crearli e aprirli.",
  "title" :"FBX - Formato file FilmBox 3D",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file FBX?

FBX, FilmBox, è un popolare formato di file 3D originariamente sviluppato da Kaydara per MotionBuilder. È stato acquisito da Autodesk Inc nel 2006 ed è ora uno dei principali formati di scambio 3D utilizzato da molti strumenti 3D. FBX è disponibile sia in formato binario che ASCII. Il formato è stato creato per fornire l'interoperabilità tra le applicazioni di creazione di contenuti digitali. Sono disponibili molti strumenti per la conversione da/in formato file FBX.

## Formato file FBX - Ulteriori informazioni

FBX è un formato proprietario e le specifiche sul suo formato di file binario non sono disponibili ufficialmente. Autodesk fornisce un C++ FBX SDK per la lettura, la scrittura e la conversione in/da file FBX. Uno script di importazione ed esportazione Python per FBX è disponibile anche nel software Blender che non utilizza l'SDK FBX.

### Struttura del file basata su testo

La struttura del file basata su testo è una struttura ad albero documentata con identificatori chiaramente denominati. Consiste in un elenco annidato di nodi disposti in una gerarchia in cui ogni nodo ha:

* Un identificatore NodeType (nome classe)
* Una tupla di proprietà ad essa associate, gli elementi della tupla sono i soliti tipi di dati primitivi: ##float, integer, string## ecc.
* Un elenco che contiene nodi nello stesso formato (ricorsivamente).

Questi possono essere rappresentati logicamente come segue:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Alcuni dei nodi standard sono definiti come elenchi impliciti in cui ogni elemento è costituito da un elenco nidificato. Qualsiasi applicazione, che intenda accedere alla geometria FBX, deve analizzare questi contenuti e trarne un significato utile. Un esempio di file FBX basato su testo è il seguente:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Struttura dei file binari dei file FBX

Come affermato in precedenza, le specifiche del formato di file FBX non sono disponibili pubblicamente per FBX. Poiché Blender Foundation implementa il formato di file FBX senza utilizzare l'SDK fornito dall'azienda, alcuni dettagli sul formato di file binario sono [disponibili](https://code.blender.org/2013/08/fbx-binary-file-format -specifica/) come parte della sua implementazione.

La struttura dei file binari segue il seguente ordine:

* Intestazione
* Record oggetto
* Piè di pagina

### Intestazione FBX

Le informazioni sull'intestazione del file sono composte da 27 byte.

* Byte 0 - 20: Kaydara FBX Binary \x00 (file-magic, con 2 spazi alla fine, quindi un terminatore NULL).
* Byte 21 - 22: [0x1A, 0x00]## (sconosciuto ma tutti i file osservati mostrano questi byte).
* Byte 23 - 26: unsigned int, il numero di versione. 7300 per la versione 7.3 per esempio.

### Record oggetto ###

L'intestazione è seguita da un record oggetto che è un record di nodo completo con nome vuoto e elenco di proprietà vuoto. Contiene ricorsivamente l'intera formazione del file.

### Piè di pagina ###

La sezione FBX Footer si trova alla fine del file il cui contenuto è sconosciuto.

## Formati di registrazione ##

I record in un file FBX sono classificati come:

* Record di nodi
* Registri di proprietà

### Formato record del nodo ###

Ciascun Node Record Format è denominato e ha il seguente layout di memoria.


|Dimensione (byte)|Tipo di data|Nome
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProprietà
|4|UInt32|Elenco proprietàLen
|1|UInt8|NomeLen
|NomeLunghezza|carattere|Nome
|?|?|Proprietà[n], dove n = 0:PropertyListLen
|Facoltativo| |
|?|?|Elenco nidificato
|13|uint8[]|Null-Record

dove:

* `EndOffset` è la distanza dall'inizio del file alla fine del record del nodo (cioè il primo byte di quello che viene dopo). Questo può essere utilizzato per saltare facilmente record sconosciuti o non richiesti.
* `NumProperties` è il numero di proprietà nella tupla di valori associata al nodo. Un elenco annidato come ultimo elemento non viene conteggiato come proprietà.
* `PropertyListLen` è la lunghezza dell'elenco delle proprietà. Questa è la dimensione richiesta per la memorizzazione delle proprietà ##NumProperties##, che dipende dal tipo di dati delle proprietà.
* `NameLen` è la lunghezza del nome dell'oggetto, in caratteri. L'unico caso in cui questo è 0 sembra essere l'elenco di livello superiore.
* `Nome` è il nome dell'oggetto. Non esiste una terminazione zero.
* `Proprietà[n]` è l'ennesima proprietà. Per il formato, vedere la sezione Proprietà Record Format. Le proprietà vengono scritte in sequenza e senza riempimento.
* `NestedList` è l'elenco annidato, la cui presenza è indicata da un record NULL proprio alla fine.

L'esistenza di una voce di elenco nidificata può essere determinata controllando se sono rimasti byte fino al raggiungimento di EndOffset. In tal caso, il record dell'oggetto successivo dovrebbe essere letto direttamente dopo l'ultima proprietà. Il record dell'oggetto segue quindi 13 zero byte, che quindi si combinano con EndOffset. Lo scopo o il requisito della voce NULL non è noto e potrebbe puntare a qualche caratteristica del formato.

### Formato record proprietà ###

Un record di proprietà contiene dettagli sulle proprietà che fanno parte di Node. Un record di proprietà ha il seguente layout di memoria:


|Dimensione (byte)|Tipo di dati|Nome
--- | --- | ---
|1|char|TipoCodice
|?|?|Dati

TypeCode rappresentano codici carattere che vengono ordinati in gruppi che richiedono una gestione simile. I TypeCodes possono essere classificati nei seguenti tipi e TypeCode può essere uno dei codici carattere tra questi tipi.

#### Tipi primitivi ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

I dati nel record di tipo scalare primitivo sono esattamente la rappresentazione binaria del valore, in ordine di byte little-endian.

#### Tipi di array ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Il Data for Array Type è più complesso e si trova nella struttura seguente.


|Dimensione (byte)|Tipo di dati|Nome
--- | --- | ---
|4|Uint32|Lunghezza array
|4|Uint32|Codifica
|4|Uint32|Lunghezza compressa
|?|?|Contenuto

### Tipi speciali ###

Di seguito sono riportati i tipi speciali TypeCodes.

```
S: String
R: raw binary data
```

Entrambi questi TypeCodes sono rappresentati come segue:


|Dimensione (byte)|Tipo di dati|Nome
--- | --- | ---
|4|Uin32|Lunghezza
|Lunghezza| |

La stringa non ha terminazione zero e potrebbe contenere \0 caratteri (questo è effettivamente utilizzato in alcune proprietà FBX).

## Riferimenti ##

* [FBX - The Autodesk SDK](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [Specifiche del formato file binario FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

