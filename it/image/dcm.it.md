{
  "date" : "2019-10-11",
  "keywords" :[ "file dcm", "formato file dcm", "cos'è un file dcm", "file", "esempio dcm", "estensione file dcm", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file DCM - File di informazioni mediche digitali",
  "description":"Ulteriori informazioni sul formato di file DCM e sulle API che possono creare e aprire file DCM.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Che cos'è un file DCM?

I file con estensione .dcm rappresentano un'immagine digitale che memorizza informazioni mediche di pazienti come risonanza magnetica, scansioni TC e immagini ecografiche. I file DCM utilizzano il formato di file immagine [DICOM](/it/image/dicom) (Digital Imaging and Communications in Medicine) e possono includere le informazioni sul paziente come riferimento. È stato sviluppato dalla [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) e aveva lo scopo di standardizzare il formato del file di imaging per la distribuzione e la visualizzazione di immagini mediche.

## Formato file DCM

I file DCM memorizzano le informazioni nel formato immagine DICOM. Questi file memorizzano il set di dati, che è un'informazione del mondo reale, che rappresenta un'istanza SOP correlata a un DICOM IOD. Le meta informazioni del file DICOM vengono memorizzate nel file seguito dal flusso di byte del set di dati effettivo.

### Informazioni meta file DICOM ##

Ogni file DICOM include un'intestazione di informazioni di identificazione per il set di dati incapsulato che consiste in:
* Un preambolo del file a 128 byte
* Prefisso DICOM a 4 byte
* File Meta elementi

Questa intestazione è un must per ogni file DICOM.

### File Metaelementi ###
|Nome attributo|Tag|Tipo| Descrizione attributo
---|---|---|---|
|Preambolo del file|Nessun campo tag o lunghezza|1|Un campo fisso di 128 byte disponibile per il profilo dell'applicazione o l'uso specificato dall'implementazione. Se non utilizzati da un profilo dell'applicazione o da un'implementazione specifica, tutti i byte devono essere impostati su 00H. I lettori di set di file o gli aggiornamenti non faranno affidamento sul contenuto di questo preambolo per determinare che questo file sia o meno un file DICOM.
|Prefisso DICOM|Nessun campo tag o lunghezza|1|Quattro byte contenenti la stringa di caratteri "DICM". Questo prefisso deve essere utilizzato per riconoscere che questo file è o meno un file DICOM.
|Lunghezza del gruppo di informazioni meta file|(0002,0000)|1|Numero di byte dopo questo elemento meta file (fine del campo Valore) fino all'ultimo elemento meta file del gruppo 2 Meta informazioni file incluso
|Versione meta informazioni file|(0002,0001)|1|Questo è un campo di due byte in cui ogni bit identifica una versione di questa intestazione Meta informazioni file. Nella versione 1 il primo valore di byte è 00H e il secondo valore di byte è 01H. Le implementazioni che leggono file con metainformazioni in cui questo attributo ha il bit 0 (lsb) del secondo byte impostato su 1 possono interpretare le metainformazioni del file come specificato in questo versione di PS3.10. Tutti gli altri bit non devono essere controllati.
|UID classe SOP di archiviazione multimediale|(0002,0002)|1|Identifica in modo univoco la classe SOP associata al set di dati. Gli UID della classe SOP consentiti per l'archiviazione multimediale sono specificati in PS3.4 - Profili dell'applicazione di archiviazione multimediale.
|UID istanza SOP di archiviazione multimediale|(0002,0003)|1|Identifica in modo univoco l'istanza SOP associata al set di dati inserito nel file e che segue le metainformazioni del file.
|Sintassi di trasferimento UID|(0002,0010)|1|Identifica in modo univoco la sintassi di trasferimento utilizzata per codificare il seguente set di dati. Questa sintassi di trasferimento non si applica alle metainformazioni del file.
|UID classe di implementazione|(0002,0012)|1|Identifica in modo univoco l'implementazione che ha scritto questo file e il suo contenuto. Fornisce un'identificazione univoca del tipo di implementazione che ha scritto per ultimo il file in caso di problemi di interscambio.
|Nome versione implementazione|(0002,0013)|3|Identifica una versione per un UID classe di implementazione (0002,0012) utilizzando fino a 16 caratteri del repertorio.
|Titolo dell'entità dell'applicazione di origine|(0002,0016)|3|Il titolo dell'entità dell'applicazione DICOM (AE) dell'AE che ha scritto il contenuto di questo file (o lo ha aggiornato l'ultima volta). Se utilizzato, consente di risalire alla fonte degli errori in caso di problemi di interscambio dei media.
|UID del creatore di informazioni private|(0002,0100)|3|L'UID del creatore delle informazioni private (0002,0102).
|Informazioni private|(0002,0102)|1C|Contiene informazioni private inserite nelle metainformazioni del file. Il creatore deve essere identificato in (0002,0100). Richiesto se è presente l'UID del creatore di informazioni private (0002,0100).

### Incapsulamento del set di dati ###

Un file DICOM contiene un unico set di dati che rappresenta una singola istanza SOP correlata a una singola classe SOP. L'UID della sintassi di trasferimento delle metainformazioni del file DICOM deve definire la sintassi di trasferimento utilizzata per codificare il set di dati.

### Supporto per le informazioni sulla gestione dei file ###

Il livello del formato multimediale fornisce le seguenti informazioni sulla gestione dei file, se necessario per un determinato profilo dell'applicazione DICOM.

* Identificazione del proprietario del contenuto del file

* Statistiche di accesso ai file (ad es. data e ora di creazione)

* Controllo dell'accesso ai file dell'applicazione

* Controllo dell'accesso ai supporti fisici (ad es. protezione da scrittura)

## Riferimenti ##
* [Standard DICOM](https://www.dicomstandard.org/current/)
* [Formato file DICOM](http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

