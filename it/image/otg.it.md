{
  "date" : "2020-01-10",
  "keywords" :[ "file otg", "formato file otg", "cos'è un file otg", "file", "esempio otg", "estensione file otg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - Formato file modello di disegno OpenDocument",
  "description":"Scopri il formato di file OTG e le API che possono creare e aprire file OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Che cos'è un file OTG?

Un file OTG è un modello di disegno creato utilizzando lo standard OpenDocument che segue la specifica OASIS Office Applications [specifica 1.0](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). Rappresenta l'organizzazione predefinita degli elementi di disegno per un'immagine vettoriale che può essere utilizzata per migliorare ulteriormente il contenuto del file. I file OTF sono come qualsiasi altro file basato sul formato OpenDocument che si basa sul formato XML per rappresentare il contenuto del documento. I file OTF possono essere visualizzati aprendoli in qualsiasi editor di testo o XML standard.

## Specifiche del formato file OTG ##

Il formato di file OTG si basa sul formato XML OpenDocument che ha uno schema consolidato. La struttura di ogni componente di un formato OpenDocument è rappresentata da un elemento che ha attributi associati ed è comune a tutti i tipi di documento come documento di testo, foglio elettronico o file di disegno. OTG, essendo un modello di disegno, utilizza ampiamente le specifiche del contenuto grafico che includono:

* Funzioni avanzate della pagina per le applicazioni grafiche
* Forme di disegno
* Cornici
* Forme 3D
* Forma personalizzata
* Forme di presentazione
* Animazioni di presentazione
* Animazioni di presentazione SMIL
* Eventi di presentazione
* Campi di testo presenti
* Contenuto del documento di presentazione

### Funzionalità avanzate della pagina per applicazioni grafiche ###
#### Maestro delle dispense ####

L'elemento Handout Master è un modello per generare automaticamente le pagine dell'handout per le applicazioni che supportano la stampa di tali pagine.
Gli attributi che possono essere associati a `<style:handout-master> ` elementi sono:

|Layout|Attributo|Descrizione
---|---|---|
|Layout pagina di presentazione|presentazione:nome-layout-pagina-presentazione|Collegamenti a `<style:presentation-page-layout>`  attributo
|Layout di pagina|`stile:nome-layout-pagina` | Specifica un layout di pagina che contiene le dimensioni, il bordo e l'orientamento della pagina master dello stampato.
|Stile pagina|`draw:style-name`|Assegna attributi di formattazione aggiuntivi a una pagina master di uno stampato assegnando uno stile di pagina di disegno.|
|Dichiarazione di intestazione| `presentazione:usa-nome-intestazione`| Specifica il nome della dichiarazione del campo di intestazione utilizzata per tutti i campi di intestazione visualizzati nella pagina principale dell'handout.
|Dichiarazione a piè di pagina| presentazione:use-footer-name|Specifica il nome della dichiarazione del campo del piè di pagina che viene utilizzata per tutti i campi del piè di pagina visualizzati nella pagina principale dell'handout.
|Dichiarazione di data e ora|use-date-time-name|Specifica il nome della dichiarazione del campo data-ora utilizzata per tutti i campi data-ora visualizzati nella pagina principale dell'handout.

### Forme di disegno ###
Il formato OpenDocument supporta diverse forme di disegno che possono essere utilizzate da qualsiasi tipo di documento.

|Forma|Attributi associati| elementi
---|---|---|
Rettangolo - `<draw:rect> `|Posizione, dimensione, stile, livello, indice Z, ID, ID didascalia, ancoraggio del testo, sfondo della tabella, posizione finale del disegno, angoli arrotondati|Titolo, descrizione lunga, listener di eventi, punti di incollaggio, testo
Riga `<draw:line> `|Stile, livello, indice Z, ID, ID didascalia e trasformazione, ancoraggio del testo, sfondo della tabella, posizione finale del disegno, punto iniziale, punto finale|Titolo, descrizione lunga, listener di eventi, punti di incollaggio, testo
Polilinea `<draw:polyline> `| Posizione, Dimensione, Casella di visualizzazione, Stile, Livello, Z-Indice, ID, ID didascalia e Trasformazione, Ancoraggio del testo, Sfondo della tabella, Posizione finale del disegno, Punti| Titolo, descrizione lunga, ascoltatori di eventi, punti di colla, testo
Poligono `<draw:polygon> `|Posizione, Dimensione, Casella di visualizzazione, Stile, Livello, Indice Z, ID, ID didascalia e Trasformazione, Ancoraggio del testo, Sfondo della tabella, Posizione finale del disegno, Punti|Titolo, Descrizione lunga, Listener di eventi, Punti di incollaggio, Testo
|Poligono regolare `<draw:regular-polygon> `|Posizione, dimensione, stile, livello, indice Z, ID, ID didascalia e trasformazione, ancoraggio del testo, sfondo della tabella, posizione finale del disegno, concavo, angoli, nitidezza|titolo, descrizione lunga, ascoltatori di eventi, punti di incollaggio, testo
|Percorso `<draw:path> `|Posizione, Dimensione, Casella di visualizzazione, Stile, Livello, Indice Z, ID, ID didascalia e Trasformazione, Ancoraggio del testo, sfondo della tabella, posizione finale del disegno, dati del percorso| Titolo, descrizione lunga, ascoltatori di eventi, punti di colla, testo

### Cornici ###
Una cornice, in un documento di disegno è un contenitore rettangolare che contiene caselle di testo, immagini o oggetti. I frame supportano funzionalità aggiuntive come contorni, mappe immagine e collegamenti ipertestuali. Una cornice può contenere un oggetto oltre che un'immagine, consentendo così di avere più rappresentazioni di un oggetto. Le applicazioni rendono il rispettivo elemento basato sul miglior supporto.

Le cornici possono contenere:
* Caselle di testo
* Oggetti rappresentati nel formato OpenDocument o in un formato binario specifico dell'oggetto
* Immagini
* Applet
* Plug-in
* Cornici mobili

Una cornice è contenuta in un documento come mostrato di seguito.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Riferimenti ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formato OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

