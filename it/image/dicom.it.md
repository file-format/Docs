{
  "date" : "2019-10-11",
  "keywords" :[ "file dicom", "formato file dicom", "cos'è un file dicom", "file", "esempio dicom", "estensione file dicom", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Formato file di imaging digitale e comunicazioni",
  "description":"Scopri il formato di file DICOM e le API che possono creare e aprire file DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DICOM?

DICOM è l'acronimo di Digital Imaging and Communications in Medicine e appartiene al campo dell'informatica medica. DICOM viene utilizzato per l'integrazione di dispositivi di imaging medico come stampanti, server, scanner, ecc. di vari fornitori e contiene anche i dati di identificazione di ciascun paziente per l'unicità. I file DICOM possono essere condivisi tra due parti se sono in grado di ricevere dati di immagine in formato DICOM. La parte di comunicazione di DICOM è il protocollo a livello di applicazione e utilizza TCP/IP per comunicare tra entità. Le versioni supportate dai servizi Web sono 1.0, 1.1, 2 o successive.

## Storia ##

DICOM è stato sviluppato congiuntamente dall'American College of Radiology (ACR) e dalla National Electrical Manufacturers Association (NEMA) per lo scambio e la visualizzazione di immagini mediche come risonanza magnetica, scansioni TC e immagini a ultrasuoni. Inizialmente, era difficile decodificare le immagini prodotte dalle macchine. Pertanto, ACR e NEMA insieme hanno formato una squadra nel 1983 che ha rilasciato il suo primo standard, ACR/NEMA 300 nel 1985. La seconda versione è stata rilasciata nel 1988 ed è stata più popolare tra i fornitori, ma presto si è capito che anche la seconda versione necessita di miglioramenti. La terza versione dello standard è stata rilasciata nel 1993 come "DICOM". 3.0 è ancora l'ultima versione ma è stata continuamente aggiornata dal 1993.

## Formato file DICOM ##

DICOM è la combinazione di definizione del formato file e protocollo di comunicazione di rete. DICOM utilizza l'estensione .DCM. .DCM esiste in due diversi formati, ovvero il formato 1.x e il formato 2.x. DCM Format 1.x è inoltre disponibile in due versioni normale ed estesa. I protocolli HTTP e HTTPS vengono utilizzati per i servizi Web di DICOM.

### Intestazione del file ###

L'intestazione del file contiene 128 byte di preambolo del file e 4 byte di prefisso DICOM.

**Preambolo n. 128 byte**|**Prefisso n. 4 byte “D, I, C, M**

**Preambolo** viene utilizzato per accedere alle immagini e ad altri dati nel file DICOM fornendo compatibilità con i formati di file immagine comunemente utilizzati.

**Prefisso** contiene la stringa "DICM" come caratteri maiuscoli.

### Set di dati ###

Ciascun file deve contenere un unico set di dati che rappresenta l'istanza SOP e la classe SOP con IOD correlato. Il set di dati è la rappresentazione delle informazioni del mondo reale. Il set di dati contiene elementi di dati e gli elementi di dati contengono i valori degli attributi di quell'oggetto. La struttura degli attributi è specificata negli IOD. Un oggetto dati DICOM è costituito da una serie di attributi, inclusi elementi come nome, ID, ecc., e anche da un attributo speciale contenente i dati dei pixel dell'immagine.

### Elementi di dati ###

L'elemento dati è costituito dall'elemento dati Tag, Lunghezza valore e valore per l'elemento dati. Esistono 5 tipi di elementi di dati, ovvero elementi di dati obbligatori di tipo 1, elementi di dati condizionali di tipo 1C, elementi di dati obbligatori di tipo 2, elementi di dati condizionali di tipo 2C e elementi di dati opzionali di tipo 3. Base Tre tipi di strutture di elementi di dati sono i seguenti.

**Elemento dati con una realtà virtuale esplicita**

|Numero gruppo|Numero elemento|Rappresentazione valore|Riservato|Lunghezza valore|Campo valore
---|---|---|---|---|---|
|2 byte|2 byte|2 byte|2 byte # 0x00, 0x00|4 byte|"Byte lunghezza valore"

**Elemento dati con una realtà virtuale esplicita**

|Numero gruppo|Numero elemento|Rappresentazione valore|Lunghezza valore|Campo valore
---|---|---|---|---|
|2 byte|2 byte|2 byte|2 byte|"Byte lunghezza valore"

**Elemento dati con una realtà virtuale implicita**


|Numero gruppo|Numero elemento|Lunghezza valore|Campo valore
---|---|---|---|
|2 byte|2 byte|4 byte|"Byte lunghezza valore"

1. **Tag elemento dati**: un numero intero ordinato che rappresenta il numero del gruppo e il numero dell'elemento
1. **Rappresentazione valore VR**: VR è una stringa di caratteri che rappresenta il VR dell'elemento dati.
1. **Lunghezza valore**: è un intero senza segno che rappresenta la lunghezza esplicita del campo del valore.
1. **Campo valore**: descrive i valori degli elementi di dati.

## Sintassi di trasferimento ##

La sintassi di trasferimento è un insieme di regole per la codifica per rappresentare in modo inequivocabile sintassi più astratte. Con l'aiuto della sintassi di trasferimento, le entità comunicanti negoziano sulle tecniche di codifica comuni che supportano.

## SOP ##

L'unione di IOD e DIMSE definisce una classe SOP. La definizione della classe SOP contiene le regole e la semantica che possono limitare l'uso dei servizi nel gruppo di servizi DIMSE o gli attributi dell'IOD. Esempi di elementi di servizio sono Archivia, Ottieni, Trova, Sposta, ecc. Esempi di oggetti sono immagini TC, immagini RM, ma includono anche elenchi di pianificazione, code di stampa, ecc.

## Servizi ##

DICOM fornisce vari servizi, per lo più legati alla comunicazione di dati. Ciascuno è brevemente descritto di seguito:


**Store:** Il servizio DICOM Store invia immagini o altri oggetti a un sistema di archiviazione e comunicazione di immagini (PACS) o server.


**Impegno di archiviazione:** Il servizio di impegno di archiviazione viene utilizzato per confermare che un'immagine è stata archiviata in modo permanente sul dispositivo su qualsiasi tipo di supporto.


**Query/recupero:** Questo servizio consente a una workstation di trovare gli elenchi di immagini o altri oggetti e quindi di recuperarli da PACS.


**Lista di lavoro modalità:** Il servizio elenco di lavoro modalità fornisce un elenco di procedure di imaging che sono state programmate per l'esecuzione da un dispositivo di acquisizione immagini.


**Stampa:** Questo servizio invia le immagini alla stampante.

## Numeri di porta su IP ##

DICOM utilizza le seguenti porte TCP e UDP:

1. 104
1. 2761
1. 2762
1. 11112

## Riferimenti ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

