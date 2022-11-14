{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File del linguaggio di markup del dispositivo portatile",
  "description":"Scopri il formato di file HDML e le API che possono creare e aprire file HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Che cos'è un file HDML?

Un file con estensione .hdml (Handheld Device Markup Language) è un linguaggio di markup per la creazione di pagine Web per dispositivi elettronici portatili come computer palmari, smartphone e dispositivi di visualizzazione delle informazioni. Si dice che HDML sia un'estensione del linguaggio [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML è simile all'HTML ma per dispositivi wireless e palmari dotati di display di piccole dimensioni come PDA, telefoni cellulari e così via. È stato sostituito con WML per il quale ha agito come un'influenza importante.

## Formato file HDML - Ulteriori informazioni

HDML è un linguaggio di markup per dispositivi palmari basato su tag di markup simili all'HTML. L'HDML è stato sottoposto al W3C per la standardizzazione, ma non è mai diventato uno standard. Le sue specifiche sul formato dei file sono, tuttavia, disponibili sul [sito Web W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) come riferimento. La [sintassi per il linguaggio HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) è disponibile come riferimento per gli sviluppatori e può essere utilizzata per lo sviluppo di applicazioni di esempio.

## Elementi HDML

Di seguito è riportato un elenco di elementi che forniscono un ambiente di runtime per HDML ed è indicato come agente utente.

|Elemento|Descrizione|
---|---|
|Carte|Questo è il blocco fondamentale dell'HDML e visualizza e consente all'utente di interagire con le schede di informazioni. |
|Mazzi|Le carte HDML sono raggruppate in mazzi. Un deck HDML è simile a una pagina HTML in quanto è identificato dall'URL [RFC1738] ed è l'unità di contenuto richiesta da un server e memorizzata nella cache dall'agente utente.|
|Azioni|Le azioni possono essere di tipo PREV, SOFT1-SOFT8 e HELP. Questi sono astratti e sono supportati nell'interfaccia utente in un modo specifico dell'agente utente.|
|Attività|Un'attività è come un gruppo di carte correlate che svolgono una funzione logica. Questi possono estendersi su uno o più mazzi. Il modello di navigazione e stato dell'HDML è strutturato attorno alle attività.|
|Navigazione basata sulla cronologia|Il programma utente mantiene una cronologia delle carte visualizzate all'utente. Ogni carta a cui si accede viene aggiunta allo storico delle carte. Il programma utente consente all'utente di tornare facilmente alla scheda precedente nella cronologia.|

## Riferimenti

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Specifiche HDML - Scuole W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

