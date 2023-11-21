{
"data": "31-05-2023",
  "keywords": [
"file sul desktop",
"cos'è un file desktop",
"cosa contiene il file desktop",
"file desktop di esempio",
"come aprire il file desktop",
"qual è il formato del file desktop",
"file",
"estensione del file sul desktop",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file DESKTOP - File di voci desktop",
  "description":"Informazioni sul formato DESKTOP e sulle API in grado di creare e aprire file DESKTOP.",
"linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent": "impostazioni"
}
},
"lastmod": "2023-05-31"
}

## Cos'è un file DESKTOP?

Un file .desktop è un file di configurazione utilizzato dagli ambienti desktop Linux per definire i collegamenti e i lanciatori delle applicazioni. Fornisce metadati su un'applicazione come nome, icona, comando da eseguire e altre proprietà. Questi file vengono generalmente utilizzati per creare collegamenti nei menu delle applicazioni, nei launcher del desktop o nei pannelli nei sistemi basati su Linux.

## Cosa contiene il file DESKTOP?

Un file .desktop segue un formato specifico e contiene diversi campi chiave:

- **[Voce desktop]:** questa è l'intestazione della sezione principale del file .desktop.
- **Nome:** Specifica il nome dell'applicazione.
- **Commento:** Fornisce una breve descrizione o un commento sull'applicazione.
- **Exec:** Definisce il comando da eseguire all'avvio dell'applicazione.
- **Icona:** specifica il percorso del file icona associato all'applicazione.
- **Terminale:** specifica se l'applicazione deve essere eseguita in una finestra di terminale.
- **Tipo:** Specifica il tipo di voce come "Applicazione" o "Link".
- **Categorie:** Specifica le categorie o i gruppi in cui l'applicazione deve essere visualizzata nel menu.
- **StartupNotify:** specifica se l'ambiente desktop deve mostrare una notifica di avvio per l'applicazione.
- **NoDisplay:** Specifica se l'applicazione deve essere nascosta dai menu.
- **Azioni:** definisce azioni aggiuntive che possono essere eseguite sull'applicazione come l'apertura di un file specifico.

## File DESKTOP di esempio

Ecco un esempio di file .desktop per un editor di testo fittizio chiamato "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

In questo esempio, il file .desktop definisce l'applicazione "MyTextEditor" con le sue proprietà associate. Include anche due azioni aggiuntive, "Apri nuova finestra" e "Apri file esistente", a cui è possibile accedere dal menu contestuale dell'avvio dell'applicazione.

Inserendo un file .desktop in directory specifiche come `/usr/share/applications` o `~/.local/share/applications`, l'ambiente desktop lo riconoscerà e visualizzerà l'applicazione di conseguenza nei menu o ne consentirà l'avvio da scrivania.

## Come aprire il file DESKTOP?

Diversi programmi software possono aprire e gestire file .desktop. Questi programmi sono in genere file manager o ambienti desktop su sistemi basati su Linux. Ecco alcuni esempi:

- **Nautilus (File):** Il file manager predefinito per l'ambiente desktop GNOME.
- **Nemo:** il file manager per l'ambiente desktop Cinnamon.
- **Dolphin:** il file manager predefinito per l'ambiente desktop KDE Plasma.
- **Thunar:** il file manager predefinito per l'ambiente desktop Xfce.
- **Editor di menu KDE:** uno strumento specifico per l'ambiente desktop KDE Plasma che ti consente di visualizzare e modificare file .desktop.

Questi file manager e ambienti desktop forniscono un'interfaccia grafica per la gestione dei file .desktop. Permettono di visualizzare e modificare le proprietà dei file .desktop, creare lanciatori di applicazioni e organizzare collegamenti nei menu delle applicazioni o sul desktop.

I file .desktop sono file di semplice testo, quindi puoi anche aprirli e modificarli con un editor di testo a tua scelta. Basta fare clic con il pulsante destro del mouse sul file .desktop e selezionare "Apri con" o "Apri con un'altra applicazione" per scegliere un editor di testo dall'elenco dei programmi installati.

## Qual è il formato del file DESKTOP?

Il formato file .desktop segue una struttura e un formato specifici. È un file di testo semplice con una serie di coppie chiave-valore organizzate in sezioni. Ecco una panoramica del formato:

- **Intestazioni di sezione:** ogni sezione inizia con un'intestazione racchiusa tra parentesi quadre ([]). La sezione primaria è in genere denominata [Voce desktop], che contiene i metadati principali per l'applicazione o il programma di avvio.
- **Coppie di valori-chiave:** all'interno di ciascuna sezione definisci le proprietà utilizzando coppie di valori-chiave. Il formato è "Chiave=Valore". La chiave identifica la proprietà e il valore fornisce i dati corrispondenti.
- **Sintassi della proprietà:** I valori delle proprietà possono essere di diversi tipi tra cui stringhe, valori booleani, percorsi di file o elenchi. Il formato per ciascun valore di proprietà dipende dal tipo.
- **Commenti:** puoi includere commenti nel file .desktop utilizzando il simbolo '#'. Tutto ciò che segue '#' in linea è considerato un commento e viene ignorato.

## Riferimenti
* [File di ingresso del desktop](https://www.baeldung.com/linux/desktop-entry-files)

