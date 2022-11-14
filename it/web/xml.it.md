{
  "date" : "2019-10-11",
  "keywords" :["xml", "File", "Estensione", "Formato file", "Estensione file", "linguaggio di markup estensibile"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file XML",
  "description":"Scopri il formato di file XML e le API che possono creare e aprire file XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file XML?

XML sta per Extensible Markup Language che è simile a **[HTML](/it/web/html/)** ma diverso nell'uso dei tag per definire gli oggetti. L'idea alla base della creazione del formato file XML era quella di archiviare e trasportare i dati senza dipendere da strumenti software o hardware. La sua popolarità è dovuta al fatto che è leggibile sia dall'uomo che dalla macchina. Ciò consente di creare protocolli di dati comuni sotto forma di oggetti da archiviare e condividere su una rete come il World Wide Web (WWW). La "X" in XML è estensibile, il che implica che il linguaggio può essere esteso a qualsiasi numero di simboli secondo le esigenze dell'utente. È per queste funzionalità che molti formati di file standard ne fanno uso come Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/it/web/xhtml/)** e **[SVG](/it/page-description-language /svg/)**.

## Formato file XML

Il formato del file XML si basa sull'XML Document Object Model (DOM) che è un'API di programmazione per documenti HTML e XML. Il DOM XML definisce un metodo standard per accedere e manipolare gli elementi del documento XML. Crea una vista ad albero di un documento XML che può essere utilizzato per accedere a tutti gli elementi attraverso l'albero DOM. Gli elementi esistenti possono essere modificati/eliminati così come nuovi elementi possono essere creati nell'albero XML. Ogni elemento di un documento XML è chiamato nodo. Il DOM XML è come mostrato nell'immagine seguente.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Approccio universale di XML

La potenza dell'XML lo rende un linguaggio universale per la comunicazione di dati sulla rete semplificando il trasporto dei dati e le modifiche alla piattaforma. Ciò assicura anche lo scambio di dati tra sistemi incompatibili possibile memorizzando i dati in formato testo normale. HTML serve per la rappresentazione dei dati sul web, mentre XML serve per lo scambio di dati. Le coppie di tag di markup utilizzate all'interno di XML definiscono gli elementi chiave della struttura che devono essere utilizzati dalle applicazioni di lettura.

## Esempio XML

Quello che segue è un esempio semplificato di un catalogo di CD in cui ogni record contiene informazioni sui CD come artista, paese, azienda, prezzo e anno di produzione.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Riferimenti

* [XML - Di Wikipedia](https://en.wikipedia.org/wiki/XML)

