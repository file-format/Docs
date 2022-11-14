{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "File", "Estensione", "Formato file", "Estensione file", "html estensibile"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Formato file del linguaggio di markup ipertestuale estensibile",
  "description":"Scopri cos'è il formato di file XHTML e le API che possono creare e aprire file XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file XHTML?

L'XHTML è un formato di file basato su testo con markup nell'XML, che utilizza una riformulazione di HTML 4.0. Questi file sono adatti per essere aperti o visualizzati in un browser web. XHTML è stato progettato per essere più strutturato, meno scripting, generico; utilizzando tutte le strutture esistenti di XML e più indipendente dal dispositivo. XHTML fornisce un insieme generalmente utile di elementi e attributi, con opzioni di estensione in combinazione con fogli di stile. Gli attributi vengono utilizzati dalla raccolta di attributi dei metadati. XHTML fornisce flessibilità e accessibilità subordinando tutti gli elementi di presentazione **[HTML](/it/web/html/)** ai fogli di stile. I fogli di stile sono più versatili di questi elementi di presentazione. Le specifiche per HTML 4.01, HTML5 e XHTML vengono sviluppate dinamicamente dal World Wide Web Consortium (W3C).

## Breve storia del formato di file XHTML

La storia di XHTML inizia con una bozza di documento pubblicata nel dicembre 1998 dal World Wide Web Consortium. Questo documento fa riferimento alla "Riformulazione dell'HTML in XML", una specifica chiamata XHTML 1.0. Questa nuova specifica ha riformulato l'HTML in XML utilizzando gli elementi o gli attributi esistenti. Nel maggio 1999, W3 Consortium ha dichiarato che HTML 4.0 era stato riformato come applicazione XML. cioè XHTML. Il 26 gennaio 2000, la prima specifica che definisce XHTML 1.0 è stata rilasciata dal W3C. Inoltre, il 31 maggio 2001, il W3C ha annunciato XHTML come linguaggio indipendente e ha iniziato a lavorare allo sviluppo di HTML 5.0. Tuttavia, nel 2005, è stato formato un gruppo di lavoro (WHATWG) che mirava a migliorare l'HTML ordinario indipendentemente dall'XHTML. Il WHATWG alla fine iniziò a lavorare su HTML5 in parallelo a XHTML 2.

## Formato file XHTML

XHTML è un formato, che è una raccolta di diversi tipi di documenti e moduli che imitano, categorizzano ed estendono HTML 4. I file in XHTML sono basati su XML e mirano a lavorare con gli interpreti basati su XML. I file XHTML sono conformi a XML. Gli strumenti XML standard vengono utilizzati per visualizzare, modificare e convalidare file XHTML. Le applicazioni dipendenti da HTML Document Object Model o XML Document Object Model [DOM] possono funzionare tramite documenti XHTML. Optando XHTML oggi, gli sviluppatori di contenuti possono godere di tutti i vantaggi associati di XML senza preoccuparsi della compatibilità con le versioni precedenti o successive dei loro contenuti.

Un insieme di elementi correlati costruisce un modulo in XHTML. Un modulo di moduli o tabelle può contenere vari elementi di moduli o tabelle che possono essere visualizzati su una pagina Web. La modularizzazione mirava a isolare gli elementi HTML in insiemi di numerosi elementi collegati. In modo che gli sviluppatori di contenuti possano trarre vantaggio dalla selezione dei moduli per diversi tipi di dispositivi. Inoltre, i moduli consentono agli agenti utente di selezionare gli elementi senza perdere la coerenza con lo standard XHTML. I requisiti di analisi di XHTML sono gli stessi di XML mentre HTML pratica i propri.

### Conformità del documento

XHTML2 offre specifiche conformi ai documenti XHTML 1.0, che utilizza gli elementi e gli attributi degli spazi dei nomi da XML e XHTML 1.0. La conformità del documento è di due tipi.

Un Documento Strettamente Conforme è basato su XML che necessita solo dei servizi obbligatori definiti in questa specifica. I seguenti criteri devono essere soddisfatti per i file XHTML:

* Un file deve essere conforme ai vincoli definiti nelle DTD e nell'Appendice B.
* L'elemento base del file deve essere html.
* L'elemento base del file deve contenere una dichiarazione per lo spazio dei nomi XHTML e deve essere definito come:

```
http://www.w3.org/1999/xhtml.
```

* L'elemento base potrebbe essere scritto come:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Prima dell'elemento base, deve essere dichiarato un DOCTYPE, il cui identificatore pubblico deve fare riferimento a una delle tre definizioni del tipo di documento (DTD). L'identificatore di sistema può essere modificato per conformarsi alle attuali convenzioni di sistema.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

Nei documenti XML, non è necessario specificare le dichiarazioni XML in tutti i documenti; tuttavia gli sviluppatori di contenuti sono invogliati a utilizzare le dichiarazioni XML in tutti i loro documenti XHTML. Queste dichiarazioni sono obbligatorie quando la codifica dei caratteri del documento è diversa da UTF-8 /16 o non è stata specificata alcuna codifica da un protocollo di governo. Il seguente esempio di un documento XHTML definisce le dichiarazioni XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Un programma utente conforme deve soddisfare le seguenti regole:

* L'analisi e la valutazione del documento XHTML viene eseguita da un programma utente che ne assicura la coerenza con la Raccomandazione XML 1.0.
* In caso di convalida dell'agente utente, deve verificare la validità dei documenti per i DTD di riferimento secondo XML. Quando il file XHTML viene elaborato dall'agente utente come XML generico, le caratteristiche del tipo ID verranno riconosciute come identificatori di frammento.

Se un programma utente si imbatte in un elemento non riconosciuto, di seguito sono riportati i criteri obbligatori che deve soddisfare

* elaborare il contenuto di quell'elemento sconosciuto
* ignora l'attributo e il suo valore
* Utilizzare il valore dell'attributo fornito come predefinito.

Quando lo user agent incontra una dichiarazione di riferimento di entità non è stata elaborata in precedenza, dovrebbe essere elaborata come i caratteri (iniziando con il segno "&" e terminando con il punto e virgola). Durante l'elaborazione del contenuto, caratteri o riferimenti a entità carattere prevedibili dall'interprete ma non renderizzabili possono utilizzare qualsiasi rendering alternativo che fornisca un significato simile. In tal caso, il documento deve essere visualizzato in modo da rendere evidente all'utente che il processo di rendering non è stato normale. Per elaborare gli spazi bianchi, l'interprete deve guardare la definizione dai caratteri CSS [CSS2].

## Compatibilità con le versioni precedenti di XHTML

La compatibilità con le versioni precedenti dei documenti XHTML 1. è ben esperta con gli user agent HTML 4, se vengono seguite le regole appropriate. XHTML 1.1 è completamente compatibile ad eccezione delle annotazioni ruby, anche se generalmente vengono ignorate dai browser HTML 4. XHTML 2.0 è relativamente meno compatibile, tuttavia il problema è stato affrontato in una certa misura attraverso l'uso di script.

## Riferimenti

* [Una storia di XHTML: dagli anni '90 ad oggi](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

