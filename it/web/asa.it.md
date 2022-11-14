{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "formato file", "tipo di file", "cos'è un file .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - File di configurazione ASP",
  "description" :"Scopri cos'è un file ASA e le API che possono creare e aprire file ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Che cos'è un file ASA?

Un file ASA è un file di configurazione, creato per i progetti [ASP](/it/web/asp/)/ASP.NET. Contiene dichiarazioni di variabili, contiene e funzioni che devono essere accessibili a livello globale nell'applicazione. Tutte le pagine del progetto possono accedere a queste variabili e funzioni, evitando così la necessità di riscriverle. Uno di questi esempi è la pagina Global.asa che è memorizzata nella directory principale per essere accessibile da altre pagine del sito Web ASP. I file Global.asa sono facoltativi, ma se utilizzati, ogni applicazione può avere un solo file Global.asa.

## Formato file ASA - Ulteriori informazioni

I file ASA sono file di testo normale con le seguenti informazioni.

* Eventi applicativi
* Eventi di sessione
* \<object> dichiarazioni
* Dichiarazioni TypeLibrary
* la direttiva #include

## Esempio di file ASA

Un file Global.asa potrebbe assomigliare a questo.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Riferimenti

* [File ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

