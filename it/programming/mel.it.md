{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded language", "file", "estensione", "formato file", "Maya 3D", "Guida alla programmazione" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya Embedded Language File Format",
  "description":"Scopri il formato di file MEL e le API che possono creare e aprire file MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Che cos'è un file MEL?

Un file con estensione .mel (Maya Embedded Language) è un linguaggio di scripting utilizzato da Autodesk Maya per creare interfacce grafiche. Ti consente di automatizzare la creazione di elementi grafici utilizzando script eseguibili oltre all'interfaccia grafica di Maya. MEL ti consente di creare interfacce grafiche senza imparare a programmare. Ciò si ottiene creando macro e azioni personalizzate che velocizzano le attività ripetitive. Queste procedure e script consentono di creare modelli personalizzati, animazioni, dinamiche e rendering di attività. Autodesk Maya 2020 può essere utilizzato per aprire e visualizzare il contenuto di un file EML.

## Formato file MEL - Ulteriori informazioni

Un [manuale di riferimento](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) del programmatore è disponibile per gli sviluppatori nella sezione della documentazione di Maya. MEL si basa su comandi di scripting di shell, simili a UINX, per ottenere risultati. I comandi basati su script lo rendono irrilevante per la programmazione convenzionale e orientata agli oggetti (OOP), risultando in nessun utilizzo di strutture dati, funzioni di chiamata o utilizzo di OOP come in altri linguaggi.

Alcuni punti chiave su MEL sono i seguenti.

`Commenti` - Ogni istruzione in MEL deve terminare con un punto e virgola (;), anche alla fine di un blocco.

`Valori restituiti` - L'affermazione di un'espressione che restituisce un valore non stampa automaticamente il valore in MEL. Invece provoca un errore.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Comandi per creare, modificare ed eliminare` - Lo stesso comando viene utilizzato per creare oggetti, modificare oggetti o richiedere informazioni su oggetti esistenti. Tuttavia, un flag controlla cosa (creare, modificare o interrogare) fa il comando.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Restituisci valore dalla funzione` - La sintassi della funzione restituisce automaticamente un valore. Per ottenere un valore restituito utilizzando la sintassi del comando, è necessario racchiudere il comando tra virgolette.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Riferimenti

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

