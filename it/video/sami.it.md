{
"data": "16-05-2023",
  "keywords": [
"file sami",
"cos'è un file sami",
"esempio di file sami",
"file",
"estensione file sami",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file SAMI - File di scambio di sottotitoli e metadati",
  "description":"Informazioni sul formato SAMI e sulle API in grado di creare e aprire file SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent" : "video"
}
},
"lastmod": "2023-05-16"
}

## Cos'è un file SAMI?

Un file con estensione ".sami" si riferisce in genere a un file SAMI (Sottotitoli e metadati). SAMI è un formato di sottotitoli utilizzato per visualizzare sottotitoli o sottotitoli nei video. È stato originariamente sviluppato da Microsoft per Windows Media Player.

I file SAMI contengono informazioni sui tempi e contenuto di testo per sottotitoli o didascalie, consentendo loro di essere sincronizzati con una riproduzione video. Il formato supporta opzioni di formattazione di base come stile del carattere, colore e posizionamento dei sottotitoli sullo schermo.

I file SAMI sono generalmente file di testo semplice e possono essere aperti e modificati utilizzando un editor di testo. Il contenuto di un file SAMI include in genere una sezione di intestazione che fornisce informazioni sul file, seguita da singole voci di sottotitoli con i rispettivi tempi e testo.

Ecco un esempio di come potrebbe apparire un file SAMI:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

I file SAMI sono comunemente usati insieme a lettori video o lettori multimediali che supportano la visualizzazione dei sottotitoli, come Windows Media Player o VLC Media Player. Il lettore legge il file SAMI e sincronizza i sottotitoli con il contenuto video, consentendo agli spettatori di leggere i sottotitoli mentre guardano il video.

## Tag HTML supportati

I file SAMI (Subtitles And Metadata Interchange) supportano un set limitato di tag simili a HTML per la formattazione e lo stile dei sottotitoli. Ecco alcuni dei tag comunemente utilizzati supportati da SAMI:

- "<SAMI> :`` L'elemento root che incapsula l'intero file SAMI.
- "<HEAD> :`` Contiene le informazioni sull'intestazione del file SAMI.
<html>- "<TITLE> :`` Specifica il titolo del file SAMI. </html>
- "<BODY> :`` Racchiude le voci dei sottotitoli e le relative informazioni sulla temporizzazione.
- "<SYNC> :`` Rappresenta un punto di sincronizzazione per una voce di sottotitoli. Specifica il momento in cui deve essere visualizzato il sottotitolo.
- "<P> :`` Racchiude il contenuto testuale effettivo di un sottotitolo. Viene tipicamente utilizzato all'interno di a<SYNC> bloccare.
<html>- `` <FONT>:`` Definisce le proprietà del carattere per il testo racchiuso. Attributi come Colore, Volto, Dimensione e Stile possono essere utilizzati per modificare l'aspetto del carattere.</font>
- "<BR> :`` Inserisce un'interruzione di riga all'interno di un sottotitolo.
<html>- `` <B>:`` Rende il testo racchiuso in grassetto.</b>
<html>- `` <I>:`` Rende il testo racchiuso in corsivo.</i>
<html>- `` <U>:`` Rende sottolineato il testo racchiuso.</u>
- "<C> :`` Specifica la posizione o l'allineamento del testo dei sottotitoli sullo schermo. Supporta attributi come Centro, Centro, Sinistra, Destra, Alto, Basso e le loro combinazioni.
- "<LANG> :`` Specifica il codice della lingua per il testo dei sottotitoli. Aiuta a identificare la lingua dei sottotitoli.

Questi sono alcuni dei tag di base supportati dai file SAMI. È importante notare che SAMI non supporta l'intera gamma di tag e attributi HTML. I tag supportati si concentrano principalmente sullo stile e sul posizionamento dei sottotitoli piuttosto che fornire un'ampia strutturazione o interattività del documento.

## Riferimenti
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

