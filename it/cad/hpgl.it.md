{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Formato file", "Apri", "Leggi", "Crea", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file HPGL e le API che possono creare e aprire file HPGL.",
  "title" :"Formato file HPGL: impara dagli esperti di formati file!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Che cos'è un file HPGL?

Un file HPGFL (Hewlett-Packard Graphics Language) contiene un set di istruzioni per il controllo del plotter sviluppato da HP. I plotter HP utilizzano questo file per disegnare e stampare contenuti vettoriali e raster sulla carta.

### Comando HPGL

Un comando HPGL è costituito da quanto segue.
* Una sezione di comando dell'alfabeto di due caratteri
* Una sezione di parametro
* Sezione terminatore

Ogni parametro nel file deve essere separato con un separatore in caso di parametri multipli.

### Esempio di comando HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Sistema di coordinate

I sistemi di coordinate comprendono indicatori di misurazione bidimensionali per individuare qualsiasi posizione specifica. L'HPGL utilizza sia le coordinate del plotter che il sistema di coordinate dell'utente per questo scopo.

#### Sistema di coordinate del plotter

Questo sistema di coordinate viene utilizzato per tracciare i disegni in base al movimento del plotter. Una tipica unità XY di movimento minimo del plotter è 0,025 mm. La possibile gamma di disegni cambia con i tipi di plotter.

#### Sistema di coordinate utente

Il sistema di coordinate specificato dall'utente può essere impostato utilizzando la scala e l'origine. Questi vengono convertiti in coordinate del plotter utilizzando il comando IP e il comando SC. Le coordinate del sistema del plotter vengono utilizzate per impostazione predefinita se questa conversione non viene eseguita.

## Formato file HPGL
I file HPGL sono in formato ASCII (file di testo) e iniziano con pochi comandi di installazione. Questo imposta alcuni parametri per il plotter per la stampa. Un tipico file HPGL ha il seguente aspetto.

|Comando|Significato
---|---|
|IN;|inizializza, avvia un lavoro di stampa|
|IP;|imposta i punti di scala (P1 e P2) sulle posizioni predefinite|
|SP1;|seleziona penna 1|
|PU0,0;|solleva la penna e passa al punto di partenza per l'azione successiva|
|PD100,0,100,100,0,100,0,0;|metti la penna giù e spostati nelle seguenti posizioni (disegna un riquadro intorno alla pagina)|
|PU50,50;|Penna su e passa alle coordinate X,Y 50,50|
|CI25;|disegna una circonferenza di raggio 25|
|SS;|selezionare il set di caratteri standard|
|DT*,1;|imposta il delimitatore di testo sull'asterisco e non stamparlo (l'1, che significa "vero")|
|PU20,80;|solleva la penna e passa a 20,80|
|LBHello World*;|disegna un'etichetta|

## Riferimenti
* [HPGL di Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [Guida di riferimento HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

