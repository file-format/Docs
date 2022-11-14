{
  "date" : "2019-10-11",
  "keywords" :[ "file potm", "formato file potm", "cos'è un file potm", "file", "esempio potm", "estensione file potm", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTM - File modello Microsoft PowerPoint con macro",
  "description":"Scopri il formato di file POTM e le API che possono creare e aprire file POTM.",
  "linktitle" : "POTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file POTM?

I file con estensione POTM sono file modello di Microsoft PowerPoint con supporto per le macro. I file POTM vengono creati con PowerPoint 2007 o versioni successive e contengono impostazioni predefinite che possono essere utilizzate per creare ulteriori file di presentazione. Queste impostazioni possono includere stili, sfondi, tavolozza dei colori, caratteri e impostazioni predefinite insieme a macro che consistono in funzioni personalizzate per svolgere attività particolari. Possono anche essere aperti da una versione precedente di PowerPoint con il supporto per documenti Open XML installato. I file POTM possono essere aperti in Microsoft PowerPoint per la modifica come qualsiasi altro file PowerPoint.

## Specifiche del formato file ##

Il formato del file POTM si basa sulle specifiche di Office OpenXML e ricorda la struttura del file [PPTX](/it/presentation/pptx/) che è un archivio [ZIP](/it/compression/zip/) compresso.

Le diapositive all'interno di un file POTM possono contenere testo, immagini, video, grafica e altri oggetti che possono essere disposti liberamente all'interno della pagina. I modelli POTM vengono quindi utilizzati per creare più file che ereditano tutte le opzioni di formattazione del file. Le macro contenute nel file POTM sono, quindi, ereditate anche da altre presentazioni. L'incorporamento nella struttura del documento avviene tramite il Registratore di macro incluso in MS Office che può salvare sequenze di comandi e creare macro per replicarle automaticamente.

File generati con il formato di file Office Open XML è una raccolta di file XML insieme ad altri file che forniscono collegamenti tra tutti i file costituenti. Questa raccolta è in realtà un archivio compresso che può essere estratto per visualizzarne il contenuto. Per farlo, basta rinominare l'estensione del file POTM con zip ed estrarlo per osservarne il contenuto.

Le sezioni seguenti fanno luce su ciascuno di questi.

### [Tipi_di_contenuto].xml ###

Questo è l'unico file che si trova a livello di base quando viene estratto lo zip. Elenca i tipi di contenuto per le parti all'interno del pacchetto. Tutti i riferimenti ai file XML inclusi nel pacchetto sono referenziati in questo file XML. Di seguito è riportato un tipo di contenuto per una parte diapositiva:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Se è necessario aggiungere nuove parti al pacchetto, è possibile farlo aggiungendo la nuova parte e aggiornando eventuali relazioni all'interno dei file .rels. Va tenuto presente che per tale modifica, è necessario aggiornare anche Content_Types.xml.

### \_rels (Cartella) ###

Le relazioni tra le altre parti e le risorse al di fuori del pacchetto sono mantenute dalla parte delle relazioni. La cartella Relazioni contiene un singolo file XML che memorizza le relazioni a livello di pacchetto. I collegamenti alle parti chiave dei file di presentazione sono contenuti in questo file come URI. Questi URI identificano il tipo di relazione di ciascuna parte chiave con il pacchetto. Ciò include la relazione con il documento dell'ufficio principale situato come ppt/presentation.xml e altre parti all'interno di docProps come proprietà principali ed estese.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Ciascuna parte del documento che è l'origine di una o più relazioni avrà la propria parte delle relazioni in cui ciascuna di tali parti della relazione si trova all'interno di una sottocartella \_rels della parte ed è denominata aggiungendo '.rels' al nome della parte parte. La parte del contenuto principale (presentation.xml) ha la propria parte relativa alle relazioni (presentation.xml.rels). Contiene relazioni con altre parti del contenuto come slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, nonché gli URI per i collegamenti esterni.

#### Relazione esplicita ####

Per una relazione esplicita, viene fatto riferimento a una risorsa utilizzando l'attributo Id di a<Relationship> elemento. Ovvero, l'Id nell'origine viene mappato direttamente a un ID di un elemento di relazione, con un riferimento esplicito alla destinazione.

Ad esempio, una diapositiva potrebbe contenere un collegamento ipertestuale come questo:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" fa riferimento alla relazione seguente all'interno della parte relativa alle relazioni per la diapositiva (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Relazione implicita ####

Per una relazione implicita, non esiste un riferimento così diretto a un `<Relationship> Id`. Invece, il riferimento è inteso.

### Cartella ppt ###

Questa è la cartella principale che contiene tutti i dettagli sui contenuti della Presentazione. Per impostazione predefinita, ha le seguenti cartelle:

* \_rels
* tema
* diapositive
* layout diapositiva
* SlideMaster

e seguenti file xml:

* presentazione.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Riferimenti ##

* [[MS-PPTX] - Formato file PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

