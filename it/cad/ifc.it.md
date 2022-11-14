{
  "date" : "2020-03-16",
  "keywords" :[ "File IFC", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file IFC e le API che possono creare e aprire file IFC.",
  "title" :"Formato file IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file IFC?

I file con estensione IFC si riferiscono al formato di file Industry Foundation Classes (IFC) che stabilisce gli standard internazionali per importare ed esportare oggetti edilizi e le loro proprietà. Questo formato di file fornisce l'interoperabilità tra diverse applicazioni software. Le specifiche per questo formato di file sono sviluppate e mantenute da buildingSMART International come Data Standard. L'obiettivo finale del formato di file IFC è migliorare la comunicazione, la produttività, i tempi di consegna e la qualità durante l'intero ciclo di vita di un edificio.

Grazie agli standard stabiliti per gli oggetti comuni nel settore edile, riduce la perdita di informazioni durante la trasmissione da un'applicazione all'altra. IFC può contenere dati per la geometria, il calcolo, le quantità, la gestione delle strutture, i prezzi ecc. per molte professioni diverse (architetto, elettrico, HVAC, strutturale, terreno ecc.).

## Breve storia ##

L'iniziativa IFC è stata presa nel 1994 da Autodesk per supportare lo sviluppo di applicazioni integrate e includeva aziende come Honeywell, Butler Manufacturing e AT&T. Nel 1995 l'adesione è stata aperta a chiunque e il nome è stato cambiato in International Alliance for Interoperability. L'intento dell'organizzazione no-profit era quello di pubblicare l'Industry Foundation Class (IFC) come modello di prodotto AEC. Nel 2005, il nome è stato nuovamente cambiato e buildSMART ora lo mantiene.

## Formato file IFC ##

Il formato file IFC ha subito diverse modifiche in passato per raggiungere le specifiche del formato file v4. Di tanto in tanto si sono verificate diverse modifiche minori e che sono state inserite nelle specifiche come Addendum. Di seguito è riportato un elenco di diverse versioni delle specifiche dei file che sono state rese pubbliche in passato.

* IFC4 Add2 (2016) IFC4 Add1 (2015)
* IFC4 (marzo 2013) ifcXML2x3 (giugno 2007)
* IFC2x3 (febbraio 2006) ifcXML2 per IFC2x2 add1 (RC2)
* IFC2x2 Addendum 1 (luglio 2004)ifcXML2 per IFC2x2 (RC1)
* IFC 2x2IFC 2x Addendum 1ifcXML1 per IFC2x e
* IFC2x Addendum 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Le ultime versioni delle specifiche del formato di file IFC sono sempre disponibili sul sito Web di buildingSMART e lo sviluppatore dovrebbe consultarle per qualsiasi tipo di applicazione che intendono sviluppare. Al momento della stesura di questo articolo, le specifiche della versione 4 sono le ultime disponibili online.

### Formati di file di dati IFC ###

Il formato file IFF supporta lo scambio di dati tra applicazioni utilizzando formati diversi, come elencato di seguito:

**IFC:** Questo è il formato di scambio IFC predefinito e utilizza la struttura fisica dei file STEP secondo ISO 10303-21. Questo formato di file ha estensione .ifc ed è il formato IFC più utilizzato.

**IFC-XML:** È una versione in formato file XML di IFC che può essere generata direttamente dall'applicazione di invio secondo la struttura ISO 10303-28, chiamata anche STEP-XML. Il formato di file IFC-XML è considerato adatto per l'interoperabilità tra gli strumenti XML. Rispetto al formato di file IFC, l'IFC-XML è di dimensioni maggiori del 300-400%.

**IFC-ZIP:** È una versione compressa [ZIP](/it/compression/zip/) di IFC o IFC-XML in cui uno di questi file si trova nella directory principale dell'archivio zip. Questo formato comprime un file .ifc del 60-80% e un file XML .ifc del 90-95%.

### Architettura IFC ###

La specifica IFC include termini, concetti e voci di specifica dei dati che derivano dall'uso all'interno di discipline, mestieri e professioni del settore dell'edilizia e della gestione delle strutture. Termini e concetti utilizza le semplici parole inglesi, gli elementi di dati all'interno della specifica dei dati seguono una convenzione di denominazione.

i nomi degli elementi di dati per tipi, entità, regole e funzioni iniziano con il prefisso "Ifc" e continuano con le parole inglesi nella convenzione di denominazione CamelCase (nessun carattere di sottolineatura, prima lettera in maiuscolo); i nomi degli attributi all'interno di un'entità seguono la convenzione di denominazione CamelCase senza prefisso; le definizioni degli insiemi di proprietà che fanno parte di questo standard iniziano con il prefisso "Pset_" e continuano con le parole inglesi nella convenzione di denominazione di CamelCase; le definizioni degli insiemi di quantità che fanno parte di questo standard iniziano con il prefisso "Qto_" e continuano con le parole inglesi nella convenzione di denominazione CamelCase.

L'architettura dello schema dei dati di IFC definisce quattro livelli concettuali, ogni singolo schema è assegnato esattamente a un livello concettuale.

**Livello di risorse**: il livello più basso include tutti i singoli schemi contenenti definizioni di risorse, tali definizioni non includono un identificatore univoco globale e non devono essere utilizzate indipendentemente da una definizione dichiarata a un livello superiore;

**Livello principale**: il livello successivo include lo schema del kernel e gli schemi di estensione del nucleo, contenenti le definizioni di entità più generali, tutte le entità definite al livello principale o superiore portano un ID univoco globale e, facoltativamente, informazioni sul proprietario e sulla cronologia;

**Livello di interoperabilità**: il livello successivo include schemi contenenti definizioni di entità specifiche per un prodotto generale, processo o specializzazione delle risorse utilizzate in diverse discipline, tali definizioni sono generalmente utilizzate per lo scambio tra domini e la condivisione di informazioni sulla costruzione;

**Livello di dominio**: il livello più alto include schemi contenenti definizioni di entità che sono specializzazioni di prodotti, processi o risorse specifiche per una determinata disciplina, tali definizioni sono in genere utilizzate per lo scambio e la condivisione di informazioni all'interno del dominio.

## Riferimenti ##

* [Classi della Fondazione dell'Industria - Di Wikipedia](https://en.wikipedia.org/wiki/Classi della Fondazione_Industria)

