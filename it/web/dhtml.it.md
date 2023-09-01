{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","file dhtml", "formato file dhtml", "tipo di file dhtml", "file", "tipo", "che cos'è un file dhtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Formato file HTML dinamico",
  "description":"Scopri il formato di file DHTML e le API che possono creare e aprire file DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DHTML?

Un file con estensione .dhtml è un file dinamico [HTML](/it/web/html/) utilizzato per creare contenuti dinamici di una pagina web. Un elemento web creato in DHTML è guidato dagli eventi e non richiede il ricaricamento della pagina. Nella maggior parte dei casi, un file DHTML viene utilizzato per creare i contenuti dinamici di una pagina Web come menu a discesa, livelli mobili, pulsanti di rollover e altri contenuti dinamici. Ti imbatti in elementi html dinamici quasi ogni giorno nella tua vita quando passi il mouse su una voce di menu e si aprono ulteriori opzioni di sottomenu. DHTML fa uso di tecnologie web come [HTML](/it/web/html/), [Javascript](/it/web/js/), HTML DOM, HTML Events e [CSS](/it/web/css/) per ottenere la dinamica comportamento degli elementi.

## Formato file DHTML

I file DHTML sono file di testo normale che contengono codice DHTML per implementare il comportamento dinamico degli elementi web.


### DOM DHTML

Il DHTML Document Object Model (DOM) si basa sul DOM HTML che è una struttura ad albero con elementi, attributi e testo come mostrato nell'immagine seguente.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Il nodo `Documento` può essere utilizzato per chiamare diverse funzioni per implementare diverse funzionalità. L'esempio seguente utilizza semplicemente il metodo document.write() di JavaScript nel DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Questo codice scrive il testo "Hello World" per l'output nel browser.

### Eventi DHTML

|S.N.|Evento|Ricorrenza|
---|---|---|
|1|onabort|Si verifica quando l'utente interrompe il caricamento della pagina o del file multimediale.|
|2|onblur|Si verifica quando l'utente lascia un oggetto HTML.|
|3|onchange|Si verifica quando l'utente modifica o aggiorna il valore di un oggetto.|
|4|onclick|Si verifica o si attiva quando un utente fa clic su un elemento HTML.|
|5|ondblclick|Si verifica quando l'utente fa clic su un elemento HTML due volte insieme.|
|6|onfocus|Si verifica quando l'utente si concentra su un elemento HTML. Questo gestore di eventi funziona in modo opposto a onblur.|
|7|onkeydown|Si attiva quando un utente preme un tasto su un dispositivo tastiera. Questo gestore di eventi funziona per tutte le chiavi.|
|8|onkeypress|Si attiva quando gli utenti premono un tasto su una tastiera. Questo gestore di eventi non viene attivato per tutte le chiavi.|
|9|onkeyup|Si verifica quando un utente rilascia un tasto da una tastiera dopo aver premuto un oggetto o un elemento.|
|10|onload|Si verifica quando un oggetto è completamente caricato.|
|11|onmousedown|Si verifica quando un utente preme il pulsante del mouse su un elemento HTML.|
|12|onmousemove|Si verifica quando un utente sposta il cursore su un oggetto HTML.|
|13|onmouseover|Si verifica quando un utente sposta il cursore su un oggetto HTML.|
|14|onmouseout|Si verifica o si attiva quando il puntatore del mouse viene spostato fuori da un elemento HTML.|
|15|onmouseup|Si verifica o si attiva quando il pulsante del mouse viene rilasciato su un elemento HTML.|
|16|onreset|Viene utilizzato dall'utente per ripristinare il modulo.|
|17|onselect|Si verifica dopo aver selezionato il contenuto o il testo su una pagina web.|
|18|onsubmit|Viene attivato quando l'utente fa clic su un pulsante dopo l'invio di un modulo.|
|19|onunload|Viene attivato quando l'utente chiude una pagina web.|

## Riferimenti

* [HTML dinamico - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

