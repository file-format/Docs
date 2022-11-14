{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File APPCACHE - Formato file manifest della cache HTML5",
  "description" :"Scopri cos'è un file APPCACHE e le API che possono creare e aprire file APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Che cos'è un file APPCACHE?

Un file APPCACHE è un file di testo che contiene l'elenco delle risorse che devono essere memorizzate nella cache dai browser per l'accesso offline alle applicazioni Web. Questo è utile quando non c'è connessione a Internet. In tale situazione, il browser utilizza le risorse della cache offline per fornire l'accesso ai contenuti web. Il file APPCACHE contiene risorse Web come immagini (ad esempio **[PNG](/it/image/png/)**, **[WEBP](/it/image/webp/)**, ecc.), fogli di stile **([ CSS])(/it/web/css/)** e file di script (come i file Javascript **[JS](/it/web/js/)**).

Le applicazioni che possono **aprire file APPCACHE** includono browser Web come Google Chrome, Safari e Firefox.

## Formato file APPCACHE - Ulteriori informazioni

I file APPCACHE sono semplici file di testo, che forniscono l'accesso offline alle pagine Web per l'esecuzione senza una connessione Internet. La presenza di APPCACHE designa una pagina come disponibile offline.

### Come fare riferimento a un file APPCACHE?

Nella tua pagina HTML, un file APPCACHE è referenziato come segue.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struttura di un file manifest APPCACHE

Un semplice file manifest APPCACHE ha il seguente aspetto.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Questo è un esempio più semplice e possono essere presenti anche strutture più complesse.

## Vantaggi di APPCACHE Manifest

L'uso dell'interfaccia cache offre alle applicazioni web i seguenti vantaggi.

1. Navigazione offline: l'interfaccia della cache consente agli utenti finali di esplorare l'intero sito quando sono offline
1. Velocità: la cache consente l'accesso ad alta velocità ai contenuti offline direttamente dal disco
1. Accessibilità in ogni momento - In caso di malfunzionamento del tuo sito, gli utenti avranno comunque accesso ai contenuti web e potranno vivere l'esperienza offline

## Riferimenti

* [Una guida per principianti al manifesto di AppCache](https://web.dev/appcache-beginner/)

