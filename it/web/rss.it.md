{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "parziale", "estensione", "file", "formato", "web", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Syndication davvero semplice",
  "description":"Scopri il formato di file RSS e le API che possono creare e aprire file RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Che cos'è un file RSS? ##

Un file con estensione .rss è noto come Really Simple Syndication. RSS è un tipo di file facilmente o facilmente leggibile dal computer, il file XML. Questi file XML vengono aggiornati automaticamente con eventuali modifiche ai dati o aggiornamenti di un sito Web o di una pagina Web. Le informazioni aggiornate insieme ai metadati (nome dell'autore, nome dell'editore, data di pubblicazione, ecc.) e altri contenuti Web del sito Web vengono estratti dai file RSS dell'utente e presentati in un formato di facile lettura. La caratteristica migliore di questi file RSS è che funzionano in tempo reale e gli aggiornamenti, le notizie, le pubblicazioni, ovvero le ultime, vengono visualizzati nella parte superiore del file. Utilizzando un file RSS, puoi facilmente creare un file contenente gli ultimi aggiornamenti di qualsiasi argomento che ti interessa, estraendo il contenuto correlato dal Web e leggendolo utilizzando un file RSS.

## Breve storia ##

Nella sua carne, il file RSS è stato creato per la prima volta da Netscape, hanno inventato la prima versione del file RSS ma poi hanno abbandonato l'idea e non hanno continuato con le versioni più recenti. È stato allora **Userland Software** che ha lavorato sul formato di file RSS e ha continuato a innovarlo con una versione più recente, ecco come RSS v2 è entrato nel mercato. Tuttavia, l'invenzione di RSS può essere ricollegata a Resource Description Framework, di Ramanathan V nel 1997. Il funzionamento dei due file è abbastanza simile ed è lecito ritenere che il concetto di RSS sia stato formato sulla base del funzionamento di RDF, un lettore di file utilizzato per raccogliere i metadati.

## Specifiche tecniche ##

Il file RSS è un tipo di file XML e tutti i file RSS devono seguire gli standard di XML 1.0. Esistono diverse versioni di diversi file RSS, come 0.91, 0.92, 2.0, tra gli altri. Il file di ciascuna versione è conforme alle specifiche e agli standard di quella specifica versione.

## Esempio RSS ##

Quello che segue è un esempio semplificato di RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Riferimento ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
