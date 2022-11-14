{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HDM - File del linguaggio di markup del dispositivo portatile",
  "description":"Scopri il formato di file HDM e le API che possono creare e aprire file HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Che cos'è un file HDM?

Un file HDM è un file di pagina Web del linguaggio di markup che viene creato in Handheld Device Markup Language (HDML). Contiene tag di markup simili al linguaggio [HTML](/it/web/html/), ma è progettato per dispositivi elettronici palmari come smartphone e PDA. Le [specifiche del formato file HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) sono state inviate al W3C per la standardizzazione ma non sono diventate uno standard. HDM si basa sulle specifiche del formato file [HDML](/it/web/hdml/) disponibili sul sito Web W3.

## Formato file HDM - Ulteriori informazioni

Il file HDM è costituito da tag di markup che vengono visualizzati su un sito Web progettato visivamente su dispositivi palmari. I file HDM vengono copiati sui dispositivi utilizzando il protocollo HDTP (Handheld Device Transport Protocol) anziché il protocollo HTTP utilizzato per le pagine HTML.

## Elementi del file HDML

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

