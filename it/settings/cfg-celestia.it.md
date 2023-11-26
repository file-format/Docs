{
"data": "27-09-2023",
  "keywords": [
"cfg",
"file CFG",
"file di configurazione cfg celestia",
"cos'è un file cfg",
"come aprire il file CFG",
"file",
"estensione file CFG",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file CFG - File di configurazione Celestia",
  "description":"Informazioni sul formato del file di configurazione CFG Celestia e sulle API in grado di creare e aprire file CFG.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent": "impostazioni"
}
},
"lastmod": "27-09-2023"
}

## Cos'è un file CFG?

Un file di configurazione di Celestia è un file di testo semplice utilizzato da Celestia, un programma di simulazione dell'universo 3D. Questi file sono vitali per personalizzare il comportamento di Celestia, quali oggetti celesti vengono visualizzati e come appare il programma. Tuttavia, la modifica di questi file richiede molta attenzione poiché modifiche improprie possono interrompere il processo di caricamento di Celestia, impedendone il corretto funzionamento.

## Celestia

Celestia è un software di simulazione astronomica 3D gratuito e open source che consente agli utenti di esplorare e visualizzare l'universo in modo altamente realistico e interattivo. È stato sviluppato da Chris Laurel ed è stato rilasciato per la prima volta all'inizio degli anni 2000. Celestia è disponibile per i sistemi operativi Windows, macOS e Linux.

Le caratteristiche e gli aspetti principali di Celestia includono:

- **Visualizzazione 3D realistica:** Celestia fornisce una rappresentazione dettagliata e accurata del nostro sistema solare, nonché di stelle, galassie e altri oggetti celesti. Utilizza modelli 3D e texture di alta qualità per creare un'esperienza visivamente coinvolgente.

- **Ampio database celeste:** il software viene fornito con un vasto database integrato di oggetti celesti conosciuti, tra cui stelle, pianeti, lune, asteroidi, comete e veicoli spaziali. Gli utenti possono facilmente individuare ed esplorare questi oggetti.

- **Precisione scientifica:** Sebbene Celestia sia uno strumento di visualizzazione, mira a rappresentare oggetti e fenomeni celesti nel modo più accurato possibile, sulla base dei dati scientifici disponibili.

## Formati di file utilizzati da Celestia

Celestia utilizza vari formati di file per diversi aspetti della sua simulazione di astronomia 3D. Ecco alcuni dei formati di file chiave utilizzati da Celestia:

1. **File di configurazione (.cel)**
- *Descrizione*: file di testo semplice che consentono agli utenti di personalizzare il comportamento, l'aspetto e il contenuto di Celestia.
- *Scopo*: personalizzare le impostazioni, definire le posizioni e specificare gli oggetti celesti.

2. **Modelli e mesh 3D**
- *Formati*: [.3ds](/it/3d/3ds/), [.obj](/it/3d/obj/), [.dae](/it/3d/dae/), .ac
- *Descrizione*: formati di file di modello 3D supportati utilizzati per il rendering di corpi celesti e veicoli spaziali.
- *Scopo*: visualizzare oggetti 3D all'interno di Celestia.

3. **File di texture**
- *Formati*: [.jpg](/it/image/jpeg/), [.png](/it/image/png/), [.dds](/it/image/dds/)
- *Descrizione*: questi file forniscono texture di superficie per i corpi celesti.
- *Scopo*: mappatura di texture su modelli 3D per un aspetto realistico.

4. **Cataloghi stellari e file di dati**
- *Formati*: formati personalizzati, [.csv](/it/spreadsheet/csv/), [.tsv](/it/spreadsheet/tsv/)
- *Descrizione*: file di dati utilizzati per rappresentare stelle e altri oggetti celesti, garantendo una simulazione accurata.
- *Scopo*: rappresentazione accurata degli oggetti celesti.

5. **Mappe cubiche di texture**
- *Descrizione*: le mappe cubiche vengono utilizzate per simulare l'aspetto di oggetti celesti distanti come le galassie.
- *Scopo*: rendering di oggetti distanti con texture realistiche.

6. **File di script**
- *Descrizione*: Questi file contengono script personalizzati scritti nel linguaggio di scripting di Celestia.
- *Scopo*: consentire agli utenti di creare eventi dinamici e animazioni all'interno dell'universo di Celestia.

## File di configurazione di Celestia

Ecco una panoramica di base di cosa puoi fare con il file di configurazione di Celestia:

1. **Impostazione della tua posizione**: puoi specificare la tua posizione sulla Terra utilizzando i parametri di latitudine, longitudine e altitudine. Ciò consente a Celestia di visualizzare accuratamente il cielo notturno dalla tua posizione.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Personalizzazione delle opzioni di visualizzazione:** puoi regolare varie opzioni di visualizzazione come il campo visivo, le impostazioni dell'ora e le preferenze di rendering.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Caricamento di oggetti celesti:** puoi aggiungere oggetti celesti come stelle, pianeti, asteroidi, veicoli spaziali e altro alla tua simulazione. Ogni oggetto è definito nel file di configurazione con le sue proprietà.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Definizione di astronavi:** puoi creare la tua astronave immaginaria o utilizzare quelle reali specificandone i parametri come posizione, orientamento e modelli 3D.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Creazione di script:** puoi scrivere script nel linguaggio di scripting personalizzato di Celestia per creare eventi dinamici e animazioni.

## Come aprire il file CFG?

Programmi che aprono o fanno riferimento a file CFG

- Celestia (gratuito) per (Windows, Mac, Linux)

## Altri file CFG

Di seguito sono riportati altri tipi di file che utilizzano l'estensione file **.cfg**.

**Impostazioni**
- [CFG - File di configurazione di Celestia](/it/settings/cfg-celestia/)
- [CFG - File di connessione al server Citrix](/it/settings/cfg-citrix/)
- [CFG - File di configurazione MAME](/it/settings/cfg-mame/)
- [CFG - File di configurazione LightWave](/it/settings/cfg-lightwave/)

**Gioco**
- [CFG - File Wesnoth Markup Language](/it/game/cfg-wesnoth/)
- [CFG - File di configurazione MUGEN](/it/game/cfg-mugen/)
- [CFG - File di configurazione del motore di origine](/it/game/cfg-sourceengine/)

**Sistema e varie**
- [CFG - File CFG](/it/system/cfg/)
- [CFG - File di configurazione del modello Cal3D](/it/misc/cfg-cal3d/)

## Riferimenti
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

