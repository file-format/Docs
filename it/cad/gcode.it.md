{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"File GCODE: cos'è un file .gcode e come aprirlo?",
   "description":"Scopri il formato file GCODE e le API che possono creare e aprire file GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-it",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Cos'è un file GCODE?

Un **file GCODE** è un file di testo semplice che contiene istruzioni per il controllo di macchine utensili computerizzate e stampanti 3D; Il codice G, o codice geometrico, è un linguaggio utilizzato per controllare i movimenti e le azioni delle macchine **CNC (controllo numerico computerizzato)**; Le macchine CNC includono fresatrici, torni, router e stampanti 3D.

I comandi del codice G sono scritti in una sintassi specifica tipicamente composta da lettere e numeri; ciascun comando istruisce la macchina ad eseguire un'azione specifica come spostare l'utensile in una posizione particolare, cambiare utensile o regolare la velocità.

Il codice G è spesso generato dal software **CAM (Computer-Aided Manufacturing)**; Il software CAM prende il modello 3D o la progettazione 2D e genera percorsi utensile e istruzioni G-code corrispondenti; il file del codice G viene quindi caricato nella macchina CNC o nella stampante 3D per l'esecuzione.

I file G-code in genere hanno l'estensione .nc o .gcode, ad esempio program.nc o print.gcode.

## Struttura del file GCODE:

I file GCODE sono file di testo semplice con ciascuna riga contenente un comando specifico; questi comandi vanno dal controllo del movimento della macchina alla regolazione della temperatura, della velocità e di altri parametri cruciali per la fabbricazione di un oggetto.

La sintassi di GCODE prevede la combinazione di lettere e numeri; ciascuno rappresenta un'azione o un parametro distinto; i comandi comuni includono G0 e G1 per il movimento, M3 e M5 per il controllo del mandrino e S e F rispettivamente per la regolazione della velocità e della velocità di avanzamento.

## Generazione GCODE:

I software di slicing come **Simplify3D** e **Slic3r** traducono i disegni CAD (Computer-Aided Design) in GCODE; Il software CAD viene utilizzato per creare modelli 3D, che vengono poi esportati in formati come STL; il software di slicing prende questi modelli e genera un file GCODE specificando dettagli come altezza dello strato, velocità di stampa e impostazioni di temperatura.

## Esempio GCODE

Ecco un semplice esempio di codice G per lo spostamento della macchina CNC:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Come aprire un file GCODE?

Per aprire un file G-code puoi utilizzare diversi tipi di software a seconda delle tue esigenze.

Se hai generato il codice G per la stampante 3D; puoi aprirlo utilizzando il software fornito con la stampante 3D o un software di slicing dedicato; gli esempi includono **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** o **Repetier-Host**; questi programmi hanno spesso un'interfaccia user-friendly che consente di caricare e visualizzare il G-code.

I file GCODE sono testo semplice quindi puoi aprirli con qualsiasi editor di testo; gli editor di testo più comuni includono **Blocco note (su Windows)**, **TextEdit (su macOS)** o **Gedit (su Linux)**; semplicemente **fai clic con il pulsante destro del mouse** sul file G-code, scegli **Apri con** e seleziona un editor di testo.

