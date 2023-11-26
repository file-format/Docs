{
"data": "03-08-2023",
  "keywords": [
"usr",
"file USR",
"cos'è un file usr",
"come aprire il file usr",
"file",
"estensione file usr",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file USR - File di dati GPS Lowrance",
  "description":"Ulteriori informazioni sul formato USR e sulle API in grado di creare e aprire file USR.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
"parent": "gis"
}
},
"lastmod": "2023-08-03"
}

## Cos'è un file USR?

Anche l'estensione del file ".usr" è correlata ai dispositivi GPS Lowrance. In particolare, viene utilizzato per memorizzare i dati GPS in un formato noto come "Formato dati utente" (formato USR) utilizzato dai dispositivi GPS Lowrance.

Quando si utilizza un'unità GPS Lowrance, è possibile salvare waypoint, tracce e percorsi come file ".usr". Questi file in genere contengono informazioni quali latitudine, longitudine, altitudine, timestamp e altri dati relativi alle tue attività GPS.

Ecco alcuni usi comuni dei file .usr con i dispositivi GPS Lowrance:

- **Waypoint:** i waypoint sono posizioni specifiche contrassegnate sul GPS, come punti di riferimento, punti di pesca preferiti o punti di interesse. È possibile salvare queste posizioni come file .usr e importarle, esportarle o condividerle con altri utenti GPS Lowrance.

- **Tracce:** le tracce rappresentano il percorso registrato dei tuoi movimenti GPS. Puoi salvare i registri delle tracce come file .usr, consentendoti di rivedere e analizzare i tuoi percorsi in un secondo momento o condividerli con altri.

- **Percorsi:** i percorsi sono percorsi predefiniti che puoi creare e salvare sul tuo dispositivo GPS. Questi percorsi possono anche essere salvati come file .usr per uso o condivisione futuri.

Per gestire i file .usr sul tuo dispositivo GPS Lowrance, in genere utilizzi software come "Insight Planner" o "Lowrance GPS Utility" di Lowrance per importare, esportare e manipolare i tuoi dati GPS.

## Formato file USR: ulteriori informazioni

Nei dispositivi GPS Lowrance iFinder, i file .usr vengono creati e salvati sulla scheda di memoria MultiMediaCard (MMC) inserita nel dispositivo. Questi file contengono dati utente come waypoint, tracce e rotte.

Per trasferire i file .usr dalla MMC al computer procedere nel seguente modo:

- **Rimuovere la MMC:** Rimuovere con attenzione la MultiMediaCard (MMC) dal dispositivo GPS Lowrance iFinder.

- **Inserisci la MMC nel computer:** utilizza un lettore di schede MMC appropriato per inserire la scheda di memoria nello slot del lettore di schede del computer.

- **Individua file .usr:** una volta riconosciuta la MMC dal tuo computer, dovresti essere in grado di accedere ai file archiviati al suo interno. Cerca i file .usr, che contengono i tuoi dati GPS.

- **Conversione con GPSBabel:** Per convertire i file .usr in un altro formato GPS, puoi utilizzare GPSBabel, che è uno strumento gratuito e open source per lavorare con vari formati di file GPS. GPSBabel supporta un'ampia gamma di formati di input e output, consentendoti di convertire i file .usr in formati compatibili con altri software o dispositivi GPS.

Puoi scaricare GPSBabel dal sito ufficiale (http://www.gpsbabel.org/) e installarlo sul tuo computer. Una volta installato, è possibile utilizzare l'interfaccia della riga di comando o l'interfaccia utente grafica del software (se disponibile) per eseguire la conversione.

Ad esempio, se desideri convertire file .usr in formato GPX, puoi utilizzare un comando come:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Il comando precedente indica a GPSBabel di leggere il file di input "input.usr" nel formato Lowrance USR e di scrivere il file di output "output.gpx" in formato GPX.

- **Importazione/utilizzo di file convertiti:** dopo la conversione, avrai i tuoi dati GPS nel nuovo formato (ad esempio GPX), che potrai utilizzare con altri software o dispositivi GPS che supportano quel formato.

## Come aprire il file USR?

I programmi che aprono o fanno riferimento a file USR includono

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Riferimenti
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

