{
  "date" : "2021-09-02", 
  "keywords" :[ "TCL", "file", "estensione", "formato file", "tiсkle", "Guida alla programmazione", "esempio tcl", "linguaggio TCL", "inizializzazione", "Tооl Соmmаd Lаnguаge" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCL - File della lingua degli strumenti",
  "description":"Scopri il formato di file TCL e le API che possono creare e aprire file TCL.",
  "linktitle" : "TCL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-02"
}

## Che cos'è un file TCL?

TCL (pronunciato "tickle" o come un inizializzazione) è un linguaggio di programmazione di alto livello, generico, interpretato, dinamico. È stato progettato con l'obiettivo di essere molto semplice ma potente. TCL mette tutto nello stampo di un comando, anche la programmazione costruisce come l'assegnazione di variabili e la definizione di procedura. Il linguaggio TCL supporta più parametri di programmazione, inclusi stili di programmazione o procedurali orientati all'oggetto, imperativi e funzionali.

## Formato file TCL ##

TCL è comunemente usato incorporato nelle applicazioni, per la prototipazione rapida, le applicazioni scritte, le GUI e i test. Gli interpreti TCL sono disponibili per molti sistemi operativi, consentendo al codice TCL di funzionare su un'ampia varietà di sistemi. Dato che TCL è una lingua molto ampia, viene utilizzato su piattaforme di sistemi embedded, sia nella sua forma completa che in diverse altre piccole versioni.

La comune combinazione di TCL con l'estensione Tk è denominata TCL/TK e consente di creare un'interfaccia utente grafica (GUI) nativamente in TCL. TCL/TK è incluso nell'installazione standard di Рythоn sotto forma di Tkinter. TCL si interfaccia nativamente con la lingua. Questo perché è stato originariamente scritto per essere un quadro per fornire un front-end sintattico ai comandi scritti in С, e tutti i comandi nella lingua (comprese le cose che potrebbero altrimenti essere parole chiave, come ad esempio se questo è impietoso).

Il linguaggio TCL ha sempre consentito per i pacchetti di estensione, che forniscono funzionalità aggiuntive, come una GUI, un'applicazione basata sui terminali, l'accesso al database e così via. TCL è un linguaggio di programmazione interpretato in modo estremamente semplice che fornisce servizi comuni come variabili, procedure e strutture di controllo, nonché molte funzioni utili che non sono disponibili in molte altre lingue.


## Breve storia ##

La lingua di programmazione TCL è stata creata nella primavera del 1988. Originariamente "nata dalla frustrazione", secondo l'autore, con i programmatori che hanno ideato le proprie lingue destinate a essere incorporate nelle applicazioni, TCL è stata colta. Оusterhоut è stato premiato nel 1997 per TCL/TK. Il nome deriva originariamente da Tool Соmmаge Lаnguаge, ma è convenzionalmente scritto "TCL" piuttosto che "TСL". Una colla più semplice rende il lavoro più facile.


## Specifiche tecniche ##

Tutte le operazioni sono comandi, comprese le strutture linguistiche. Sono scritti in notazione di prefisso. Spesso è richiesto un numero variabile di argomenti. Tutto può essere ridefinito dinamicamente e superato. In realtà, non ci sono parole chiave, quindi anche le strutture di controllo possono essere aggiunte o modificate, anche se questo non è consigliabile. Tutti i tipi di dati possono essere manipolati come stringhe, incluso il codice sorgente.

Internamente, le variabili hanno tipi come intero e doppio, ma la conversione è puramente automatica. Le variabili non sono dichiarate, ma assegnate a. L'uso di una variabile non definita provoca un errore. Sistema di oggetti completamente dinamico, basato su classi, TсlОО, comprese funzionalità avanzate come meta classi, filtri e mixin. Interfaccia guidata da eventi a socket e file. Sono possibili anche eventi basati sul tempo e definiti dall'utente. Visibilità variabile limitata per impostazione predefinita a un ambito lessicale (statico), ma di livello superiore e superiore, consentendo ai passaggi di interagire con gli ambiti delle funzioni di inclusione.

Tutti i comandi definiti da TCL stesso generano messaggi di errore in caso di utilizzo errato. Estensibilità, via С, С++, Jаvа, Рythоn e TCL. Lingua interpretata usando il byte code. Il supporto Full Uniсоde (3.1 all'inizio, regolarmente aggiornato) è stato rilasciato per la prima volta nel 1999.

Safe-Tcl è un sottoinsieme di TCL che ha funzionalità limitate in modo che gli script TCL non possano danneggiare la loro macchina o applicazione host. Safe-Tсl può essere incluso nell'e-mail quando l'applicazione/safe-tcl e il multipart/enabled-mail sono supportati. La funzionalità di Safe-Tсl è stata da allora incorretta come parte delle versioni standard di TCL/TK.


## Esempio di formato file TCL ##

```
puts "Hello, World!"

oo::class create fruit {
    method eat {} {
        puts "yummy!"
}
}
oo::class create banana {
    superclass fruit
    constructor {} {
        my variable peeled
        set peeled 0
}
    method peel {} {
        my variable peeled
        set peeled 1
        puts "skin now off"
}
    method edible? {} {
        my variable peeled
        return $peeled
}
    method eat {} {
        if {![my edible?]} {
            my peel
    }
        next
}
}
set b [banana new]
$b eat               → prints "skin now off" and "yummy!"
fruit destroy
$b eat               → error "unknown command"
```

## Riferimento ##

* [TCL - di Wikipedia](https://en.wikipedia.org/wiki/Tcl)



