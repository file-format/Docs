{
  "date" : "2019-10-11",
  "keywords" :[ "3DS", "file", "formato", "tipo di file", "estensione", "cos'è un file 3DS?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file 3DS e le API che possono aprire e creare file 3DS.",
  "title" :"Formato file 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Cos'è il file 3DS?

Un file con estensione .3ds rappresenta il formato di file mesh 3D Sudio (DOS) utilizzato da Autodesk 3D Studio. Autodesk 3D Studio è presente nel mercato dei formati di file 3D dagli anni '90 e ora si è evoluto in 3D Studio MAX per lavorare con la modellazione 3D, l'animazione e il rendering. Un file 3DS contiene dati per la rappresentazione 3D di scene e immagini ed è uno dei formati di file più diffusi per l'importazione e l'esportazione di dati 3D. Considera informazioni come le posizioni delle telecamere, i dati Mesh, le informazioni sull'illuminazione, le configurazioni del viewport, i dati di gruppo di smoothing, i riferimenti bitmap e gli attributi per creare vertici e poligoni per il rendering di una scena.

## Formato file 3DS - Ulteriori informazioni
Alla base, 3DS è un formato di file binario e segue una struttura predefinita per l'archiviazione e il recupero dei dati. Il formato di file binario consente al formato di file 3DS di essere più piccolo rispetto ai formati di file basati su testo. I dati all'interno di un file 3DS vengono archiviati sotto forma di blocchi.

### Pezzo 3DS

Ogni blocco in un file 3DS è un blocco di dati che contiene un ID, la lunghezza del blocco per la posizione del blocco successivo e i dati stessi. L'ID del blocco consente ai lettori di formati di file 3DS di saltare i blocchi che non riconoscono. Aiuta anche nell'estendibilità del formato. Ogni blocco memorizza informazioni relative a forme, illuminazione e informazioni di visualizzazione che insieme rendono la scena. I blocchi sono disposti in una struttura gerarchica in un file 3DS e nella rappresentazione assomigliano all'albero degli oggetti del documento XML.

**Chunk ID:** I primi due byte di un blocco rappresentano un identificatore di blocco che consente al lettore di file di decidere se considerarlo durante la lettura o saltarlo.

**Lunghezza del blocco:** L'ID del blocco è seguito da un numero intero di 4 byte (in little-endian) che rappresenta la lunghezza del blocco. Questa lunghezza include anche la lunghezza dei dati, la lunghezza dei suoi sottoblocchi e l'intestazione di 6 byte.

**Carico utile:** La lunghezza del blocco è seguita dai byte di dati effettivi per il blocco, seguiti dai suoi blocchi secondari nella stessa struttura gerarchica che può essere estesa a diversi livelli in profondità.

### Struttura di un pezzo

La struttura gerarchica di un blocco semplice è la seguente:

**Un pezzo**

|inizio|fine|dimensione|nome
--- | --- | --- | ---
|0|1|2|ID blocco
|2|5|4|Pezzo successivo

I blocchi hanno una gerarchia imposta loro che è identificata dal suo ID. Un file 3ds ha l'ID blocco primario 4D4Dh. Questo è sempre il primo pezzo del file. Con nel blocco principale ci sono i blocchi principali.

**Pezzi principali**

|id|Descrizione
--- | ---
|3D3D|Inizio dei dati della mesh dell'oggetto.
|B000|Inizio dei dati del fotogramma chiave.

Il puntatore Next Chunk dopo il blocco ID punta al successivo blocco Main.
Subito dopo un pezzo principale c'è un altro pezzo. Questo potrebbe essere qualsiasi altro tipo di blocco consentito all'interno del suo ambito di blocchi principali.
Per la descrizione della mesh (3D3D) potrebbero essere multipli di qualsiasi.

**Subchunk di 3D3D - Blocco mesh**


|id|Descrizione
--- | ---
|1100|sconosciuto
|1200|Colore sfondo.
|1201|sconosciuto
|1300|sconosciuto
|1400|sconosciuto
|1420|sconosciuto
|1450|sconosciuto
|1500|sconosciuto
|2100|Blocco colore ambiente
|2200|nebbia?
|2201|nebbia?
|2210|nebbia?
|2300|sconosciuto
|3000|sconosciuto
|4000|Blocco oggetti
|7001|sconosciuto
|AFFF|sconosciuto

**Subchunk di 4000 - Blocco descrizione oggetto**
Il primo elemento di Subchunk 4000 è una stringa ASCIIZ del nome degli oggetti.
Ricorda che un oggetto può essere una mesh, una luce o una fotocamera.

|id|Descrizione
--- | ---
|4010|sconosciuto
|4012|ombra?
|4100|Oggetto poligono triangolare
|4600|Luce
|4700|Fotocamera

## Riferimenti

* [Formati di file di geometria - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32-htm.html)
* [3DS - Di Wikipedia](https://en.wikipedia.org/wiki/.3ds)
