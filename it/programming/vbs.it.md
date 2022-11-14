{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "file", "estensione", "formato file", "Visual Basic Script", "Guida alla programmazione", "esempio vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - File di script di Visual Basic",
  "description":"Scopri il formato di file VBS e le API che possono creare e aprire file VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Che cos'è un file VBS?

VBS o VBScript è connesso con l'edizione di script di Microsoft Visual Basic. Nell'ambiente informatico, l'utente può accedere e controllarne molti aspetti. VBScript può utilizzare un modello denominato **Component Object Model** per usufruire degli elementi e degli strumenti dell'ambiente. Questo ambiente è specificato per lavorare ed eseguire VBScript.

Funziona in modo simile a Javascript quando vi accede il client nel campo dello sviluppo Web. Viene inoltre utilizzato dai server per l'elaborazione delle pagine web. Può essere considerato in alcuni altri tipi di file di scripting come applicazioni di [HTML](/it/web/html/).


## Breve storia ##

È stato lanciato per la prima volta nel 1996, come parte delle tecnologie utilizzate da Microsoft specificate per Windows Scripts. Inizialmente è stato sviluppato appositamente per l'aiuto degli sviluppatori Web. Nello stesso anno, l'esploratore di Microsoft Windows chiamato Internet Explorer è stato rilasciato insieme alle funzionalità di Visual Basic Script.

Con il progresso della tecnologia e dello sviluppo web, sono state lanciate molte versioni di VBScript insieme a molte funzionalità avanzate. Inoltre, nel prossimo anno, questo linguaggio di scripting entrerà a far parte di Microsoft Windows con nuove funzionalità.

## Specifiche tecniche ##

Per le pagine Web sul lato server, vengono utilizzati strumenti come **Active Server Pages** insieme a VBScript. Questo linguaggio di scripting può essere utilizzato anche nel componente script di Windows. I file di questa lingua sono archiviati con estensione .vbs in Windows.

Ci sono molte strutture di controllo come i loop che vengono utilizzate nel codice di questo linguaggio. Include anche argomenti che sono riga di comando e possono essere denominati o senza nome. I file di questa lingua possono essere archiviati semplicemente nelle cartelle o sul desktop di un sistema operativo Windows. Sebbene non esista un ambiente di sviluppo integrato specifico per i programmi VBScript come Microsoft Script Editor, fornisce la struttura per lo sviluppo di questo linguaggio.

Quando VBScript è ospitato dall'host Script di Windows, fornisce varie funzionalità che sono abbastanza comuni ai linguaggi di scripting ma non sono disponibili in Visual Basic 6.0. Le funzionalità che implicano l'accesso facile o diretto riguardano stampanti di rete, argomenti della riga di comando senza nome e con nome, stdout e stdin, condivisioni di rete, Strumentazione gestione Windows, informazioni sull'utente di reti come l'appartenenza a gruppi e molto altro.

## Esempio di formato file VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Riferimento ##

* [VBS - di Wikipedia](https://en.wikipedia.org/wiki/VBScript)



