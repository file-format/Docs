{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file AHK e le API che possono creare e aprire file AHK.",
  "title" :"Formato file AHK - File script AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Che cos'è un file AHK?

Un file AHK è un file di script generato con l'applicazione software AutoHotkey che viene utilizzato per l'automazione delle attività in Microsoft Windows. Contiene istruzioni per l'automazione delle attività utilizzando i tasti di scelta rapida che possono essere utilizzati per eseguire azioni istantanee. Il file viene eseguito da AutoHotkey e tutte le azioni vengono eseguite in sequenza. I file AHK sono abbastanza potenti per eseguire attività complesse utilizzando i tasti di scelta rapida definiti utilizzando i tasti di scelta rapida. I file AHK possono essere aperti con editor di testo come Microsoft Notepad e Notepad++.

## Formato file AHK

I file AHK vengono salvati su disco come file di testo normale e contengono righe di codice che possono essere eseguite da AutoHotkey. AutoHotkey è un linguaggio di scripting open source gratuito e consente agli utenti di creare script da semplici a complessi per eseguire azioni come compilatori di moduli, clic automatici, esecuzione di macro, ecc. Un file AHK come minimo può eseguire una singola azione e quindi uscire .

Sono disponibili strumenti che possono essere utilizzati per convertire AHK in file [Exe](/it/executable/exe/).

### Esempio AHK

Nell'esempio seguente viene utilizzata la chiave Win+Z per eseguire Blocco note Microsoft o portarlo in primo piano se è già in esecuzione.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Come faccio a creare un file AHK?

I seguenti passaggi possono essere utilizzati per creare un file AHK. Questi presuppongono che AutoHotkey sia già installato sulla macchina.

* Fare clic con il pulsante destro del mouse sul desktop.
* Trova "Nuovo" nel menu.
* Fai clic su "Script AutoHotkey" all'interno del menu "Nuovo".
* Assegna un nuovo nome allo script.
* Trova il file appena creato sul desktop e fai clic con il pulsante destro del mouse.
* Fai clic su "Modifica script".
* Dovrebbe essere apparsa una finestra, probabilmente Blocco note.
* Salva il file.

## Riferimenti

* [AutoHotkey](https://www.autohotkey.com/)
* [File batch - di Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

