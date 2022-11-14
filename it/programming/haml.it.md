{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file HAML - File codice sorgente Haml",
  "description":"Scopri il formato di file HAML e le API che possono creare e aprire file HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Che cos'è un file HAML?

Un file HAML è un file del linguaggio di markup di astrazione HTML che contiene il codice sorgente scritto nel linguaggio [Haml](https://haml.info/). Può essere utilizzato come sostituto dell'ERB (script modello Ruby). Il file HAML contiene il codice sorgente del modello che consente di generare l'HTML di un documento web. I file ERB possono essere sostituiti semplicemente sostituendo questi file nella cartella app/viste in Haml modificando l'estensione del file. I file HAML possono essere aperti con qualsiasi editor di testo come Microsoft Notepad, Notepad++, Apple TextEdit,

## Formato file HAML

I file HAML sono file sorgente salvati su disco come file di testo normale. Contiene codice scritto nella sintassi HAML. HAML sostituisce i tag **<>** con il segno **%** per rendere il codice più semplice e facile. I file ERB sono sostituibili direttamente da HAML, come mostrato nel seguente semplice esempio.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Esempio HAML

Quello che segue è un esempio Hello World di HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
che esegue il rendering nel seguente output HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Riferimenti

* [HAML - Github](https://github.com/haml/haml)

