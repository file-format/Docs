{
  "date" : "2021-05-24",
  "keywords" :["xul", "File", "Estensione", "Formato file", "Estensione file", "Lingua interfaccia utente XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - File di lingua dell'interfaccia utente XML",
  "description":"Scopri il formato di file XUL e le API che possono creare e aprire file XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Che cos'è un file XUL?

Un file con estensione .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) sta per XML User Interface Language) è un file di linguaggio di markup basato su [XML](/it/web/xml/) per creazione di interfacce utente. È stato sviluppato da Mozilla per consentire agli sviluppatori di creare elementi dell'interfaccia utente grafica simili ad altri linguaggi di markup utilizzati per la creazione di pagine Web. XUL è stato ampiamente utilizzato da Mozilla nel suo browser Firefox dove utilizzava la base di codice Mozilla. Il rendering XUL viene eseguito utilizzando il
[Motore Gecko](https://en.wikipedia.org/wiki/Gecko_(software)). I fork di Firefox come Pale Moon, Basilisk e Waterfox mantengono il supporto per i componenti aggiuntivi XUL. I file XUL sono identificati con il tipo MIME: application/vnd.mozilla.xul+xml.

## Formato file XUL

I file XUL sono scritti in testo normale basato sul formato di file XML e vengono visualizzati utilizzando il motore Gecko. Le tre parti principali di una struttura XUL sono:

* `Contenuto` - Include le dichiarazioni della finestra e gli elementi dell'interfaccia utente contenuti al loro interno.
* `Skin` - Include tutti i fogli di stile, le immagini e altri file relativi ai temi. L'aspetto di una finestra è descritto nei fogli di stile.
* `Locale` - Il testo visualizzato all'interno di una finestra viene memorizzato separatamente e gli utenti possono utilizzare più set di file di lingua.

### Esempio XUL

L'esempio seguente crea tre pulsanti impilati uno sopra l'altro in direzione verticale.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Riferimenti

* [XUL - Di Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [Documentazione archiviata XUL - Di Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

