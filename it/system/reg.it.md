{
"data": "07-03-2023",
  "keywords": [
"file di registro",
"cos'è un file reg",
"file",
"estensione del file di registro",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file REG - File di registro di Windows",
  "description":"Informazioni sul formato REG e sulle API che possono creare e aprire file REG.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent" : "system"
}
},
"lastmod": "2023-03-07"
}

## Cos'è un file REG?

Un file REG è un formato di file utilizzato per importare o esportare i dati del registro di Windows. Il registro di Windows è un database gerarchico che memorizza le impostazioni e le opzioni di configurazione per il sistema operativo Windows e le applicazioni installate. Il registro contiene informazioni quali preferenze dell'utente, impostazioni dell'applicazione, dati di configurazione hardware e software e altro ancora.

Un file REG ha in genere un'estensione di file ".reg" ed è un file di testo semplice che contiene una serie di voci e valori di registro in un formato specifico. Il formato è costituito da una sezione di intestazione che identifica il file come file di registro, seguita da una serie di coppie chiave e valore che rappresentano le voci di registro.

## Formato file REG: ulteriori informazioni

Ecco un esempio di formato di file reg:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

La prima riga del file specifica la versione dell'editor del registro. Le righe seguenti contengono le voci del registro nel formato di un percorso chiave seguito da un nome valore e dati valore. In questo esempio, il file reg contiene due voci: una che aggiunge un programma chiamato "Example.exe" all'elenco di avvio di Windows e un'altra che imposta il valore "Nascosto" nelle impostazioni avanzate di Esplora risorse su "true".

I file Reg possono essere creati e modificati utilizzando un editor di testo come Blocco note. Vengono spesso utilizzati per scopi di backup e ripristino, nonché per configurare più computer con le stesse impostazioni di registro.

## Importa o esporta il registro di Windows

Un file REG è un tipo di file utilizzato per importare o esportare dati dal registro di Windows. Il registro di Windows è un database gerarchico che memorizza le impostazioni e le opzioni di configurazione per il sistema operativo Windows e le applicazioni installate. Il registro contiene informazioni quali preferenze dell'utente, impostazioni dell'applicazione, dati di configurazione hardware e software e altro ancora.

I file Reg possono essere utilizzati per creare o modificare voci di registro e vengono spesso utilizzati per scopi di backup e ripristino, nonché per configurare più computer con le stesse impostazioni di registro. Ecco come utilizzare un file reg per aggiungere una nuova voce di registro al registro di Windows:

1. Crea un nuovo file di testo utilizzando un editor di testo come Blocco note.
2. Digitare la voce di registro nel formato corretto. Il formato è costituito da una sezione di intestazione che identifica il file come file di registro, seguita da una serie di coppie chiave e valore che rappresentano le voci di registro. Ecco un esempio:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Ciò crea una nuova chiave denominata "Esempio" sotto la chiave "Software" nell'hive del registro dell'utente corrente e imposta il valore "Setting1" su "Value1".

3. Salvare il file con estensione .reg.
4. Fare doppio clic sul file .reg per aggiungere la nuova voce di registro al registro di Windows.

Ti verrà richiesto di confermare che desideri aggiungere la voce al registro. Una volta confermata, la nuova voce verrà aggiunta al registro e potrai verificarla utilizzando lo strumento Editor del registro.

## Riferimenti
* [Registro di Windows](https://en.wikipedia.org/wiki/Windows_Registry)

