{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File GDOC - Collegamento a Google Documenti",
  "description":"Scopri cos'è un file GDOC e le API che possono creare e aprire file GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Che cos'è un file GDOC?

Un file GDOC è un file di collegamento che punta a un file che si trova su Google Drive, un servizio di archiviazione di documenti basato su cloud. Quando il client Google Drive è installato su un computer e al suo interno viene creato un documento, l'unità crea un documento nell'archivio cloud online e scrive l'[URL](/it/web/url/) di questo documento nel file GDOC in Google locale Cartella dell'unità. Quando si fa doppio clic su questo file di collegamento, il browser Web predefinito apre il documento dalla posizione [URL](/it/web/url/). Se questo file di collegamento viene spostato fuori da questa cartella, il collegamento al documento in linea viene interrotto.

## Formato file GDOC - Ulteriori informazioni

Il file GDOC contiene il collegamento al documento online scritto nel formato di file [JSON](/it/web/json/). Il browser che apre i file GDOC legge le informazioni sull'URL e apre il documento collegato per la visualizzazione, a condizione che l'utente abbia effettuato l'accesso a questo account Google in cui è archiviato il documento. I file GDOC non contengono il contenuto del documento.

### Esempio di file GDOC

Il file GDOC può essere aperto in un editor di testo e il suo contenuto è simile al seguente.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Come si può vedere, i contenuti sono formattati in JSON con l'URL di un documento e l'ID documento associato.

## Riferimenti

* [Google Docs non apre né file gdoc né docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

